---
title: Configura [!DNL Databricks Delta Share] per Audience Sourcing
description: Scopri come configurare e connettere  [!DNL Databricks Delta Share] per l'audience sourcing in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 876b7d2996d3027f81159252f714c2305d6d23b4
workflow-type: tm+mt
source-wordcount: '2816'
ht-degree: 1%

---


# Configura [!DNL Databricks Delta Share] per audience sourcing

Utilizzare questa guida per connettere [!DNL Databricks Delta Share] a tipi di pubblico di prime parti Adobe Real-Time CDP Collaboration e source tramite l&#39;interfaccia utente.

Quando connetti [!DNL Databricks Delta Share], Collaboration legge i dati del pubblico direttamente dalla condivisione del catalogo Unity. Al termine della determinazione dell&#39;origine, è possibile utilizzare i tipi di pubblico per l&#39;attivazione e l&#39;analisi di sovrapposizione nei progetti di collaborazione.

Questa guida spiega come preparare i prerequisiti, connettere [!DNL Delta Share], specificare le tabelle di origine, mappare i campi di identità e verificare che l&#39;origine del pubblico venga avviata correttamente.

I tipi di pubblico originati da [!DNL Databricks] seguono le stesse regole di governance e gestione dei dati dei tipi di pubblico originati da Adobe Experience Platform e da altre origini cloud supportate.

Altri metodi di determinazione origine disponibili includono [Experience Platform](./onboard-audiences.md), [Amazon S3](./configure-aws-s3-audience-sourcing.md), [Google Cloud Storage](./configure-gcs-audience-sourcing.md), [Snowflake](./configure-snowflake-audience-sourcing.md), [Azure storage](./configure-azure-storage-audience-sourcing.md) e [caricamento file CSV](./upload-csv-audience-sourcing.md). Per ulteriori informazioni su tutte le origini disponibili in Collaboration, consulta [Panoramica sulle origini](./source-overview.md).

## Prerequisiti {#prerequisites}

Completa i prerequisiti in questa sezione prima di avviare il flusso di lavoro di configurazione. I prerequisiti mancanti sono un motivo comune per gli errori di configurazione o per la mancata visualizzazione dei tipi di pubblico dopo la determinazione dell’origine. Prima di seguire questa guida, completa l&#39;onboarding e la configurazione dell&#39;[account](./onboard-account.md).

Per alcune attività di questa guida è necessario l&#39;intervento dell&#39;amministratore [!DNL Databricks]. Se non amministri [!DNL Databricks] per la tua organizzazione, prima di iniziare rivolgiti all&#39;amministratore appropriato.

### Accesso a [!DNL Databricks Delta Share] {#databricks-delta-share-access}

Prima di procedere, confermare quanto segue con l&#39;amministratore [!DNL Databricks]:

* La tua organizzazione ha pubblicato [!DNL Delta Share] nell&#39;account [!DNL Databricks] di Adobe utilizzando la condivisione nativa da database a database (catalogo Unity). Collaboration non supporta la voce delle credenziali bearer-token o OIDC nell’interfaccia utente per questo flusso di lavoro.
* Conosci il nome del provider registrato nel metastore Unity Catalog di Adobe, il nome della condivisione e lo schema che contiene le tabelle del pubblico.
* L&#39;origine del pubblico [!DNL Databricks Delta Share] è disponibile per il tuo account e area geografica Collaboration. Se l’origine Databricks non è ancora disponibile nella tua area geografica, contatta il rappresentante del tuo account Adobe per confermare una timeline.

Per istruzioni dettagliate sulla pubblicazione di una condivisione in Adobe, consulta la sezione [Pubblicare la condivisione Delta in Adobe](#publish-delta-share) in questa guida.

### Preparare i dati sul pubblico {#prepare-audience-data}

Struttura le tabelle dei tipi di pubblico in modo che Collaboration possa individuare i tipi di pubblico e mappare correttamente le identità.

* **Tabella di appartenenza (obbligatoria):** Tabella all&#39;interno dello schema condiviso contenente una riga per coppia profilo-pubblico. Questa tabella deve includere una colonna mappabile a `AUDIENCE_ID` e almeno una colonna chiave di corrispondenza supportata. Collaboration utilizza questa tabella per l’anteprima dei dati sorgente e la mappatura dei campi.
* **Tabella metadati (facoltativa):** Se si gestisce un catalogo separato di tipi di pubblico (una riga per pubblico con ID pubblico, nome, conteggi o metadati simili), è possibile fornire questa tabella in modo che Collaboration legga le definizioni dei tipi di pubblico da essa invece di dedurre ID di pubblico distinti dalla sola tabella appartenenze.
* **Chiavi di corrispondenza supportate:** `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID`, `ADFIXUS_ID` e altre chiavi di corrispondenza abilitate per il tuo account Collaboration.
* **Requisiti di hashing:** tutti i valori chiave di corrispondenza devono essere tagliati, in minuscolo e con hash SHA256 prima di essere archiviati in [!DNL Databricks]. Collaboration non esegue l’hashing o la normalizzazione dei dati prima dell’acquisizione.
* **Coerenza colonna:** La tabella di appartenenza deve esporre nomi di colonna stabili che Collaboration può mappare alle chiavi di corrispondenza abilitate.

Tutte le chiavi di corrispondenza presenti nella tabella di appartenenza devono essere abilitate anche per l’account Collaboration. Per aggiungere o abilitare le chiavi di corrispondenza, vedere [Configurare le chiavi di corrispondenza](./onboard-account.md#set-up-match-keys).

### Valori richiesti prima di iniziare {#required-values}

Preparare i valori seguenti prima di avviare la configurazione guidata.


| Valore | Descrizione |
| ----- | ----------- |
| Nome provider | Identificatore del provider utilizzato da Adobe nel catalogo Unity per accedere a [!DNL Delta Share]. Questo valore può essere fornito dall&#39;amministratore [!DNL Databricks] o dal contatto per l&#39;onboarding di Adobe. Questo valore non corrisponde all&#39;URL dell&#39;area di lavoro [!DNL Databricks]. |
| Nome condivisione | Nome di [!DNL Delta Share] pubblicato in Adobe. |
| Schema | Lo schema all’interno della condivisione che contiene le tabelle del pubblico. |
| Tabella di appartenenza | Il nome della tabella all’interno dello schema che contiene le righe di appartenenza al pubblico (una riga per profilo in un pubblico). |
| Tabella metadati (facoltativa) | Il nome della tabella all’interno dello schema che elenca i tipi di pubblico (una riga per pubblico), se utilizzi un catalogo di pubblico basato sui metadati. |

{style="table-layout:auto"}

## Configura la connessione [!DNL Databricks] {#configure-databricks-connection}

Il flusso di lavoro di configurazione è una procedura guidata in più passaggi all&#39;interno dell&#39;area di lavoro **[!UICONTROL Configurazione]**. Completa ogni passaggio in sequenza.

### Aggiungi una nuova connessione dati {#add-data-connection}

Dalla scheda **[!UICONTROL Tipi di pubblico]** nell&#39;area di lavoro **[!UICONTROL Configurazione]**, selezionare l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) e quindi seleziona **[!UICONTROL Pubblico]**.

Se questo è il tuo primo pubblico, puoi anche selezionare l&#39;opzione **[!UICONTROL Aggiungi]**.

![Scheda Pubblico personale nell&#39;area di lavoro di configurazione con l&#39;icona Aggiungi e l&#39;opzione Aggiungi pubblico visualizzate.](../../assets/setup/add-manage-audiences/add-audiences.png)

Viene visualizzato il flusso di lavoro Aggiungi pubblico. Seleziona **[!UICONTROL Aggiungi una nuova connessione dati]**, quindi seleziona **[!UICONTROL Avanti]**.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione Aggiungi una nuova connessione dati evidenziata.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Seleziona [!DNL Databricks Delta Share] come origine dati {#select-databricks-delta-share}

Nella schermata di selezione dell&#39;origine dati sono elencati tutti i tipi di connessione disponibili. Selezionare **[!UICONTROL Condivisione Delta database]**, quindi selezionare **[!UICONTROL Avanti]**.

![Il flusso di lavoro Aggiungi pubblico visualizza la schermata di selezione dell&#39;origine dati con Condivisione Delta database selezionata e Successivo evidenziato.](../../assets/setup/databricks-audience-sourcing/databricks-data-source-selection.png)

### Connetti [!DNL Delta Share] {#connect-delta-share}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sharing_databricks"
>title="Experience League"
>abstract="Consulta la guida all&#39;origine di [!DNL Databricks Delta Share] per istruzioni su come configurare la condivisione per l&#39;origine del pubblico"

Fornisci i dettagli necessari per consentire a Collaboration di accedere a [!DNL Delta Share]. Immettere il provider, la condivisione, lo schema e i dettagli della tabella da [!DNL Databricks Delta Share]. La tabella di appartenenza richiesta deve essere disponibile nello schema condiviso. Se utilizzi una tabella di metadati, questa deve essere disponibile anche nello stesso schema condiviso.
Dopo aver immesso le informazioni richieste, selezionare **[!UICONTROL Connetti]**.

Collaboration convalida la condivisione e la monta nell’area di lavoro di Adobe. Questo passaggio può richiedere fino a un minuto. Durante l&#39;impostazione della connessione viene visualizzato un indicatore di avanzamento.

| Campo | Descrizione |
| --- | --- |
| **[!UICONTROL Nome provider]** | Il nome del provider di Unity Catalog utilizzato da Adobe per utilizzare la condivisione. Vedi [Valori richiesti prima di iniziare](#required-values). |
| **[!UICONTROL Nome condivisione]** | Nome di [!DNL Delta Share] pubblicato in Adobe. |
| **[!UICONTROL Schema]** | Lo schema all’interno della condivisione che contiene le tabelle del pubblico. |
| **[!UICONTROL Tabella dati]** | Il nome della tabella all’interno dello schema che contiene le righe di appartenenza al pubblico (una riga per profilo in un pubblico). |
| **[!UICONTROL Tabella metadati]** | La tabella che elenca i tipi di pubblico (una riga per pubblico). |


![Il flusso di lavoro Aggiungi pubblico mostra il modulo di condivisione connessione dei database con il nome del provider, il nome della condivisione, lo schema, la tabella dati e i campi della tabella metadati e il pulsante Avanti disponibile.](../../assets/setup/databricks-audience-sourcing/databricks-connect-share-successful.png)

Se non è possibile trovare la condivisione o se lo schema non è ancora visibile, viene visualizzato un messaggio di errore. Verificare i valori con l&#39;amministratore [!DNL Databricks] e riprovare.

### Conferma il consenso e la conferma dell’utilizzo dei dati {#confirm-consent}

Prima di procedere, verifica di aver applicato le rinunce previste dalla legge ai dati sul pubblico inviati a Collaboration. Se non sei sicuro che i tuoi dati soddisfino questo requisito, consulta la [guida ai criteri di governance e alle azioni di applicazione](./onboard-audiences.md#governance-policy-and-enforcement-actions) prima di procedere. Selezionare la casella di controllo di conferma, quindi selezionare **[!UICONTROL OK]** per continuare.

![La finestra di dialogo per la conferma della rinuncia al consenso richiede conferma prima di procedere.](../../assets/setup/aws-audience-sourcing/consent-optout-acknowledgment.png)

### Fornisci dettagli di connessione {#provide-connection-details}

Immettere un nome e una descrizione facoltativa per la connessione dati. Il nome specificato viene visualizzato nella scheda **[!UICONTROL Connessioni dati personali]** e consente di distinguere questa origine se si gestiscono più connessioni dati.

* **[!UICONTROL Nome connessione dati]** (obbligatorio)
* **[!UICONTROL Descrizione connessione dati]** (facoltativo)

Seleziona **[!UICONTROL Avanti]** per continuare.

![Aggiungi il flusso di lavoro del pubblico nel passaggio &quot;Fornisci dettagli&quot; che mostra i campi per il nome della connessione dati e la descrizione della connessione dati, con &quot;Successivo&quot; visibile nell&#39;angolo in alto a destra.](../../assets/setup/databricks-audience-sourcing/databricks-connection-details.png)

### Mappa campi di identità {#map-identity-fields}

La schermata **[!UICONTROL Mapping]** mostra come Collaboration esegue il mapping delle colonne di origine dalla tabella di appartenenza ai campi di identità di destinazione. Collaboration mappa automaticamente i campi in base ai nomi delle colonne e alle chiavi di corrispondenza abilitate per il tuo account.

>[!TIP]
>
>Seleziona **[!UICONTROL Anteprima dati di origine]** per rivedere un campione della tua tabella di appartenenza in formato tabulare, quindi seleziona **[!UICONTROL Chiudi]** per tornare alla schermata di mappatura.

![La finestra di dialogo &quot;Anteprima dati di Databricks&quot; mostra una tabella di esempio di dati sul pubblico con colonne quali AUDIENCE_ID e HASHED_EMAIL_SHA_256 e un pulsante Chiudi nell&#39;angolo in basso a destra.](../../assets/setup/databricks-audience-sourcing/databricks-source-data-preview.png)

Verificare che i mapping visualizzati riflettano le colonne della tabella di appartenenza. Seleziona **[!UICONTROL Avanti]** per continuare.

![Aggiungi il flusso di lavoro del pubblico nel passaggio &quot;Mappa campi&quot; che mostra i campi di origine mappati ai campi di identità di destinazione, con l&#39;opzione &quot;Anteprima dati di origine&quot; visibile e il pulsante Avanti nell&#39;angolo in alto a destra.](../../assets/setup/databricks-audience-sourcing/databricks-field-mapping.png)

### Pianificazione della frequenza di aggiornamento e dell’intervallo di date {#schedule-refresh}

Viene visualizzata la visualizzazione **[!UICONTROL Pianificazione]**. Utilizza il menu a discesa per selezionare una frequenza di aggiornamento compresa tra uno e sei giorni, quindi imposta l’intervallo di date attivo. Utilizza l’icona del calendario per specificare le date di inizio e fine.

>[!IMPORTANT]
>
>Per gestire in modo efficace i crediti Collaboration, impostare la frequenza di aggiornamento in modo che corrisponda o superi la frequenza di aggiornamento dei dati sottostanti.

![Schermata delle impostazioni di pianificazione con le opzioni di frequenza di aggiornamento e la configurazione dell&#39;intervallo di date.](../../assets/setup/databricks-audience-sourcing/databricks-schedule-refresh-frequency.png)

### Verifica e completa la connessione {#review-and-complete}

Rivedi il riepilogo della configurazione prima di creare la connessione. Nella schermata di riepilogo vengono visualizzate le sezioni seguenti:

* **[!UICONTROL Connessione dati]**: nome della connessione, nome del provider, nome della condivisione e schema configurati.
* **[!UICONTROL Mapping]**: mapping dei campi di identità di origine e di destinazione.
* **[!UICONTROL Pianificazione]**: frequenza di aggiornamento e intervallo di date attivo.

![Aggiungi il flusso di lavoro del pubblico nel passaggio &quot;Revisione&quot; che mostra un riepilogo della connessione di condivisione, dei dettagli e delle sezioni di mappatura con i valori configurati e il pulsante Completa visibile nell&#39;angolo in alto a destra.](../../assets/setup/databricks-audience-sourcing/databricks-review.png)

Verificare che tutte le sezioni siano corrette, quindi selezionare **[!UICONTROL Completa]**.

Viene visualizzata una finestra di dialogo di conferma che indica che Collaboration ha creato la connessione dati e che è in corso la determinazione dell’origine del pubblico.

## Rivedere i tipi di pubblico originati {#review-sourced-audiences}

Dopo aver completato la configurazione guidata, Collaboration inizia a determinare l&#39;origine dei tipi di pubblico dalle tabelle [!DNL Databricks] in modo asincrono. Passa a **[!UICONTROL Configurazione] > [!UICONTROL I miei tipi di pubblico]** per monitorare l&#39;avanzamento. Il processo di determinazione origine non viene completato immediatamente. Il tempo necessario dipende dalle dimensioni dei dati.

### Monitorare l’avanzamento di audience sourcing {#monitor-sourcing-progress}

Mentre Collaboration recupera i dati del pubblico, un banner nella parte superiore dell&#39;area di lavoro **[!UICONTROL I miei tipi di pubblico]** indica che la determinazione dell&#39;origine è in corso. I singoli tipi di pubblico vengono visualizzati nell’elenco solo dopo il completamento della determinazione dell’origine per ciascun pubblico.

![Imposta l&#39;area di lavoro nella scheda Pubblico personale con un banner &quot;Audience sourcing in progress&quot; che indica che i tipi di pubblico vengono originati da una connessione dati Database, con l&#39;elenco dei tipi di pubblico visualizzato di seguito.](../../assets/setup/databricks-audience-sourcing/databricks-audience-sourcing-in-progress-banner.png)

>[!TIP]
>
>Il tempo di Audience sourcing varia in base alle dimensioni della tabella di appartenenza e all’utilizzo di una tabella di metadati per l’individuazione del pubblico. I set di dati più grandi potrebbero richiedere più tempo per essere visualizzati nell&#39;area di lavoro **[!UICONTROL Tipi di pubblico]**.

### Visualizzare i dettagli del pubblico di origine {#view-audience-details}

Una volta completato il sourcing, i tipi di pubblico [!DNL Databricks] vengono visualizzati nella scheda **[!UICONTROL Tipi di pubblico personali]** insieme ai tipi di pubblico ottenuti da altre connessioni. Seleziona un elemento riga o **[!UICONTROL Visualizza pubblico]** per aprire la visualizzazione dettagli per un pubblico specifico.

![La scheda &quot;I miei tipi di pubblico&quot; nell&#39;area di lavoro Impostazione mostra una tabella di tipi di pubblico, incluso un pubblico ottenuto da Condivisione Delta database, con caselle di controllo e azioni di riga selezionabili disponibili.](../../assets/setup/databricks-audience-sourcing/databricks-my-audiences-row-actions.png)

La vista dei dettagli mostra lo stato del pubblico, l’origine e il nome della connessione dati, insieme ai pannelli seguenti:

* **[!UICONTROL Identità]**: il conteggio e il raggruppamento delle identità totali per il pubblico, una volta che i dati diventano disponibili.
* **[!UICONTROL Categorie]**: qualsiasi tag applicato per organizzare o filtrare il pubblico.
* **[!UICONTROL Accesso alla connessione]**: pubblico privato, pubblico o condiviso con collaboratori specifici.
* **[!UICONTROL Visibilità metadati]**: quali informazioni sul pubblico, ad esempio il conteggio delle identità, la percentuale di sovrapposizione e l&#39;indice, sono visibili ai collaboratori.

![Visualizzazione dei dettagli dei singoli tipi di pubblico con Stato: Attivo, sistema di origine e nome della connessione dati nella parte superiore, con i quattro pannelli seguenti: Identità, Categorie, Accesso alla connessione e Visibilità metadati.](../../assets/setup/databricks-audience-sourcing/databricks-audience-detail-view.png)

Esamina queste impostazioni prima di utilizzare il pubblico in un progetto di collaborazione. Per aggiornare le categorie, l&#39;accesso alla connessione o la visibilità dei metadati, consulta [Visualizzare e gestire singoli tipi di pubblico](./onboard-audiences.md#view-individual-audiences).

### Modificare le impostazioni del pubblico {#edit-audience-settings}

Puoi modificare i metadati del pubblico direttamente dalla visualizzazione elenco **[!UICONTROL Tipi di pubblico]** senza aprire la visualizzazione dettagli. Seleziona la casella di controllo di un pubblico per visualizzare la barra degli strumenti delle azioni, quindi seleziona un&#39;azione: **[!UICONTROL Modifica visibilità metadati]**, **[!UICONTROL Modifica accesso connessione]**, **[!UICONTROL Modifica nome e descrizione]**, **[!UICONTROL Modifica categorie]** o **[!UICONTROL Elimina]**.

![La visualizzazione elenco Pubblico personale mostra i tipi di pubblico provenienti da sistemi diversi, con una riga selezionata mediante una casella di controllo che mostra una barra degli strumenti inferiore con opzioni di modifica ed eliminazione.](../../assets/setup/databricks-audience-sourcing/databricks-edit-audience-settings.png)

### Visualizza connessione dati [!DNL Databricks] {#view-databricks-connection}

Per esaminare la connessione stessa, incluse le relative chiavi di corrispondenza, passare a **[!UICONTROL Configurazione]** > **[!UICONTROL Connessioni dati personali]**. La nuova connessione [!DNL Databricks] è disponibile. L&#39;origine del pubblico viene visualizzata come **[!UICONTROL Condivisione delta database]**.

![La scheda Le mie connessioni dati mostra la connessione dati [!DNL Databricks Delta Share] con le informazioni sullo stato dell&#39;origine.](../../assets/setup/databricks-audience-sourcing/databricks-my-data-connections-tab.png)

## Limitazioni note {#known-limitations}

Tieni presente i seguenti vincoli durante la configurazione e l&#39;utilizzo di [!DNL Databricks Delta Share] audience sourcing:

* **Solo condivisione nativa:** L&#39;interfaccia utente supporta solo la condivisione nativa da database a database [!DNL Delta Sharing]. I flussi di autenticazione Bearer-token e OIDC non sono disponibili nella configurazione guidata.
* **Nessun browser di tabelle nella procedura guidata:** Immettere manualmente i nomi delle tabelle. Collaboration convalida i nomi delle tabelle durante l&#39;anteprima delle tabelle, ma non elenca automaticamente tutte le tabelle della condivisione.
* **Limite righe tabella metadati:** Quando utilizzi una tabella metadati per l&#39;individuazione del pubblico, Collaboration importa fino a 100.000 righe di pubblico da tale tabella. Se il catalogo supera questo limite, contatta il supporto Adobe.
* **Vincoli chiave di corrispondenza:** Una volta abilitata una chiave di corrispondenza per una connessione dati, non è possibile rimuoverla. È possibile aggiungere le chiavi di corrispondenza a una connessione esistente, ma non disattivarle o eliminarle. Per modificare le chiavi di corrispondenza attive, è necessario [eliminare la connessione dati](./manage-data-connection.md#delete-data-connection) e crearne una nuova.
* **Tabella di appartenenza richiesta:** Anche quando si utilizza una tabella di metadati per l&#39;individuazione del pubblico, è necessario specificare una tabella di appartenenza. Collaboration legge le righe di identità dalla tabella delle appartenenze durante l’acquisizione.

## Risoluzione dei problemi {#troubleshooting}

Utilizzare questa sezione per risolvere i problemi che si verificano durante o dopo la configurazione. Per gli errori durante la connessione di condivisione, verificare il nome del provider, il nome della condivisione e lo schema con l&#39;amministratore [!DNL Databricks].

**Connessione di condivisione non riuscita o timeout**

* Verifica che [!DNL Delta Share] sia pubblicato nell&#39;account [!DNL Databricks] di Adobe e che il nome del provider, il nome della condivisione e lo schema siano corretti.
* Conferma che lo schema sia visibile nella condivisione. La propagazione delle nuove condivisioni pubblicate può richiedere del tempo.
* Se la connessione non riesce ancora dopo alcuni minuti, riavvia la configurazione e riprova, oppure contatta l’assistenza clienti Adobe e indica il nome del provider, il nome della condivisione, lo schema e tutti i dettagli dell’errore rilevanti. Non includere credenziali riservate.

**Anteprima tabella non riuscita**

* Verificare che il nome della tabella sia digitato correttamente ed esista nello schema specificato.
* Assicurarsi che la tabella sia inclusa in [!DNL Delta Share] pubblicato in Adobe.
* Per l&#39;individuazione basata sui metadati, visualizzare in anteprima sia la tabella di appartenenza che la tabella di metadati prima di continuare.

**Stato dei blocchi di convalida della mappatura dei campi**

* Verificare che la tabella di appartenenza includa una colonna mappabile a **`AUDIENCE_ID`**.
* Assicurati che almeno due campi di identità siano completamente mappati (sorgente e destinazione).
* Utilizza **[!UICONTROL Anteprima dati di origine]** per verificare che i nomi delle colonne corrispondano alle chiavi di corrispondenza abilitate.

**I tipi di pubblico non vengono visualizzati o l&#39;origine richiede più tempo del previsto**

* Il tempo di determinazione origine viene scalato in base al volume dei dati. È previsto un tempo di elaborazione esteso per le tabelle di appartenenza di grandi dimensioni.
* Se i tipi di pubblico non vengono visualizzati entro 24 ore, controllare la scheda **[!UICONTROL Le mie connessioni dati]** per verificare la presenza di indicatori di errore sulla connessione.
* Verifica che la struttura della tabella di appartenenza e le mappature dei campi corrispondano ai requisiti in [Prepara i dati del pubblico](#prepare-audience-data).
* Se il problema persiste, contatta l’Assistenza clienti di Adobe e fornisci il nome della connessione dati e i dettagli della tabella.

**La connessione dati mostra uno stato di errore dopo l&#39;esecuzione iniziale**

* Verificare che [!DNL Delta Share] e le tabelle non siano state rimosse o rinominate in [!DNL Databricks] dopo la creazione della connessione.
* Verifica che l’accesso di Adobe alla condivisione non sia stato revocato.
* Se il problema persiste, contatta l’assistenza clienti Adobe.

## Pubblica [!DNL Delta Share] in Adobe {#publish-delta-share}

[!DNL Databricks] Unity Catalog [!DNL Delta Sharing] consente di condividere le tabelle in modo sicuro con altri account [!DNL Databricks] senza copiare i dati. Per consentire a Collaboration di leggere i dati sul pubblico, l&#39;amministratore di [!DNL Databricks] deve pubblicare un [!DNL Delta Share] sull&#39;account consumer di Adobe [!DNL Databricks].

### Prima della pubblicazione {#before-you-publish}

Rivolgiti al rappresentante del tuo account Adobe o al contatto per l’onboarding per ottenere:

* Conferma che Adobe è pronto a ricevere la tua condivisione nella tua area geografica.
* Il nome del provider utilizzato da Adobe nel metastore Unity Catalog per identificare l&#39;organizzazione come provider di condivisione.

Prepara quanto segue nell&#39;area di lavoro [!DNL Databricks]:

* Un [!DNL Delta Share] contenente lo schema e le tabelle che Collaboration leggerà.
* Una tabella di appartenenza con una riga per coppia profilo-pubblico e colonne per **`AUDIENCE_ID`** e chiavi di corrispondenza.
* Una tabella di metadati facoltativa se intendi utilizzare l’individuazione del pubblico basata sui metadati.

### Pubblicare la condivisione {#publish}

Segui le [!DNL Databricks Delta Sharing] procedure della tua organizzazione per concedere all&#39;account consumer di Adobe l&#39;accesso alla condivisione. I passaggi esatti dipendono dal modello di distribuzione e governance di [!DNL Databricks]. In generale:

1. In Unity Catalog, crea o identifica la condivisione contenente lo schema e le tabelle del pubblico.
2. Aggiungi lo schema (o singole tabelle) alla condivisione.
3. Concedi la condivisione all&#39;account consumer [!DNL Databricks] di Adobe utilizzando la condivisione nativa da database a database.
4. Verifica con il tuo contatto Adobe che la condivisione sia visibile sul lato consumer e annota il nome del provider e il nome della condivisione per la configurazione guidata di Collaboration.
5. Per la documentazione del prodotto [!DNL Databricks] in [!DNL Delta Sharing], consulta la [documentazione sulla condivisione Delta dei databrick](https://docs.databricks.com/aws/en/delta-sharing).

### Raccogliere i dettagli di [!DNL Databricks] per Collaboration {#collect-databricks-details}

Dopo aver pubblicato la condivisione, accertati di avere a disposizione il nome del provider, il nome della condivisione, lo schema e i nomi delle tabelle per il flusso di lavoro di configurazione di Collaboration.

Raccogli i dettagli riportati di seguito prima di avviare la configurazione guidata di Collaboration.

| Campo | Descrizione | Esempio |
| ------| ----------- | ------- |
| Nome provider | Identificatore del provider nel metastore Unity Catalog di Adobe (dall’onboarding di Adobe) | `your_org_provider` |
| Nome condivisione | Nome del [!DNL Delta Share] pubblicato | `audience_share_prod` |
| Schema | Schema | `collaboration_audiences` |
| Tabella di appartenenza | Tabella con righe di appartenenza profilo-pubblico | `audience_members` |
| Tabella metadati (facoltativa) | Tabella in cui sono elencati i tipi di pubblico (una riga per pubblico) | `audience_catalog` |

{style="table-layout:auto"}

## Passaggi successivi {#next-steps}

[!DNL Databricks Delta Share] è stato configurato come origine dati in Collaboration. Al termine dell&#39;origine, i tipi di pubblico sono disponibili nell&#39;area di lavoro **[!UICONTROL Tipi di pubblico]** e pronti per essere utilizzati nei progetti di collaborazione.

Da qui, puoi:

* [Creare e gestire progetti di collaborazione](../collaborate/manage-projects.md)
* [Attivare i tipi di pubblico all’interno di un progetto](../collaborate/activate.md)
* [Verifica le sovrapposizioni e misura le prestazioni](../collaborate/measure.md)
* [Gestire le impostazioni e la visibilità del pubblico](./onboard-audiences.md#view-individual-audiences)
* [Visualizzare e gestire le connessioni dati](./manage-data-connection.md)

Per altri metodi di determinazione dell&#39;origine del pubblico, vedi:

* [Configura [!DNL Google Cloud Storage] per audience sourcing](./configure-gcs-audience-sourcing.md)
* [Configura [!DNL Amazon S3] per audience sourcing](./configure-aws-s3-audience-sourcing.md)
* [Configura [!DNL Snowflake] per audience sourcing](./configure-snowflake-audience-sourcing.md)
* [Tipi di pubblico di Source da Experience Platform](./onboard-audiences.md)
* [Caricare un file CSV per l’audience sourcing](./upload-csv-audience-sourcing.md)
