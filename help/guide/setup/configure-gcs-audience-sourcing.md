---
title: Configura [!DNL Google Cloud Storage] per Audience Sourcing
description: Scopri come connettere un bucket  [!DNL Google Cloud Storage]  come origine del pubblico self-service in Real-Time CDP Collaboration, inclusi prerequisiti, autenticazione, mappatura campi, pianificazione e convalida.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 1875ac192fc36f62a4f4a4f12163d2a2cf28486f
workflow-type: tm+mt
source-wordcount: '2501'
ht-degree: 1%

---


# Configura [!DNL Google Cloud Storage] per audience sourcing

Segui i passaggi descritti in questa guida per connettere il bucket [!DNL Google Cloud Storage] (GCS) ad Adobe Real-Time CDP Collaboration e iniziare a determinare l&#39;origine dei dati del pubblico di prime parti tramite l&#39;interfaccia utente.

Connetti un bucket GCS a Collaboration per acquisire direttamente i dati del pubblico di prime parti senza supporto tecnico. Una volta effettuata la connessione, Collaboration origina il pubblico dal bucket in base a una pianificazione periodica, rendendolo disponibile per l’attivazione e l’analisi di sovrapposizione all’interno dei progetti di collaborazione. L’origine dei tipi di pubblico è un passaggio obbligatorio prima di poterli attivare o utilizzarli nell’analisi di sovrapposizione con i collaboratori.

Questa guida descrive il flusso di lavoro di configurazione end-to-end: preparazione dei prerequisiti, autenticazione del bucket GCS, revisione dei campi di identità mappati automaticamente, pianificazione dell’aggiornamento dei dati e conferma del completamento dell’origine.

I tipi di pubblico originati da [!DNL Google Cloud Storage] seguono le stesse regole di governance e gestione dei dati dei tipi di pubblico originati da Adobe Experience Platform.

Altri metodi di determinazione origine disponibili includono [Experience Platform](./onboard-audiences.md), [Amazon S3](./configure-aws-s3-audience-sourcing.md), [Snowflake](./configure-snowflake-audience-sourcing.md) e [caricamento file CSV](./upload-csv-audience-sourcing.md).

## Prerequisiti {#prerequisites}

Completa tutti gli elementi in questa sezione prima di avviare il flusso di lavoro di configurazione. I prerequisiti incompleti sono il motivo più comune per cui l’impostazione non riesce o i tipi di pubblico non vengono visualizzati dopo la determinazione dell’origine. Prima di seguire questa guida, devi aver completato l&#39;[onboarding e la configurazione dell&#39;account](./onboard-account.md).

Alcuni passaggi in questa sezione richiedono l&#39;intervento di un amministratore [!DNL Google Cloud]. Se non sei l&#39;amministratore [!DNL Google Cloud] per la tua organizzazione, identifica la persona appropriata prima di iniziare.

### Accesso e autorizzazioni GCS {#gcs-access-permissions}

<!-- [LINK REQUIRED: Once the GCS permissions and roles guide is published, replace this NOTE with a direct link to that guide and remove the placeholder instructions below.] -->

>[!NOTE]
>
>Una guida dedicata che copre i ruoli IAM [!DNL Google Cloud] specifici, la configurazione dell&#39;account del servizio e le autorizzazioni a livello di bucket richieste per questa integrazione è in attesa di pubblicazione. Finché tale guida non sarà disponibile, rivolgiti al tuo amministratore [!DNL Google Cloud] per verificare che Adobe disponga delle autorizzazioni necessarie per eseguire l&#39;autenticazione nel bucket e leggere i file di pubblico.

Prima di procedere, confermare quanto segue con l&#39;amministratore [!DNL Google Cloud]:

* Ad Adobe sono state concesse le autorizzazioni necessarie per eseguire l’autenticazione nel bucket GCS e leggere i file di pubblico.
* L&#39;origine del pubblico [!DNL Google Cloud Storage] è disponibile nella tua area geografica. La disponibilità varia in base all&#39;area geografica (NA, EMEA, ANZ). Se il sourcing GCS non è ancora disponibile nella tua area geografica, contatta il rappresentante del tuo account Adobe per confermare una timeline.

### Preparare i dati sul pubblico {#prepare-audience-data}

I file del pubblico devono essere conformi alla **[Specifica di origine del pubblico (v1.2)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)** prima dell&#39;inizio dell&#39;origine. Esamina le specifiche per la definizione completa dello schema e gli esempi a livello di campo. I requisiti principali includono:

* **Formato file:** CSV, utilizzando virgole come delimitatori di campo e barre verticali (`|`) come separatori per più valori all&#39;interno di un singolo campo.
* **Campi obbligatori:** Ogni record deve includere una colonna `AUDIENCE_ID` e almeno una colonna chiave di corrispondenza supportata.
* **Chiavi di corrispondenza supportate:** `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID`, `ADFIXUS_ID`.
* **Requisiti di hashing:** tutti i valori chiave di corrispondenza devono essere tagliati, in minuscolo e con hash SHA256 prima del caricamento. Collaboration non esegue l’hashing o la normalizzazione dei dati prima dell’acquisizione.
* **Coerenza colonna:** se il bucket contiene più file di pubblico, tutti i file devono utilizzare strutture di colonna identiche.

Tutte le chiavi di corrispondenza presenti nei file del pubblico devono essere abilitate anche per il tuo account Collaboration. Per aggiungere o abilitare le chiavi di corrispondenza, vedere [Configurare le chiavi di corrispondenza](./onboard-account.md#set-up-match-keys).

### Valori richiesti prima di iniziare {#required-values}

Preparare i valori seguenti prima di avviare la configurazione guidata.

| Valore | Descrizione |
| --- | --- |
| **[!UICONTROL Bucket]** | Nome del bucket [!DNL Google Cloud Storage] contenente i file del pubblico. |
| **[!UICONTROL Percorso]** | Il prefisso del percorso all&#39;interno del bucket in cui sono memorizzati i file del pubblico (ad esempio, `sourcing/testdata/path1/`). |

## Configura la connessione [!DNL Google Cloud Storage] {#configure-gcs-connection}

Il flusso di lavoro di configurazione è una procedura guidata in più passaggi all&#39;interno dell&#39;area di lavoro **[!UICONTROL Configurazione]**. Completa ogni passaggio in sequenza. Puoi tornare a qualsiasi passaggio utilizzando l’icona a forma di matita nella schermata di revisione finale prima di creare la connessione.

### Aggiungi una nuova connessione dati {#add-data-connection}

Dalla scheda **[!UICONTROL Tipi di pubblico]** nell&#39;area di lavoro **[!UICONTROL Configurazione]**, selezionare l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) e quindi seleziona **[!UICONTROL Pubblico]**.

Se questo è il tuo primo pubblico, puoi anche selezionare l&#39;opzione **[!UICONTROL Aggiungi]**.

![Scheda Pubblico personale nell&#39;area di lavoro di configurazione con l&#39;icona Aggiungi e l&#39;opzione Aggiungi pubblico visualizzate.](../../assets/setup/add-manage-audiences/add-audiences.png)

Viene visualizzato il flusso di lavoro Aggiungi pubblico. Seleziona **[!UICONTROL Aggiungi una nuova connessione dati]**, quindi seleziona **[!UICONTROL Avanti]**.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione Aggiungi una nuova connessione dati evidenziata.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Seleziona [!DNL Google Cloud Storage] come origine dati {#select-gcs}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sourcing_specifications_gcs"
>title="Preparazione dei dati per l’onboarding"
>abstract="Leggi la guida alle specifiche di Audience Sourcing per scoprire come formattare e strutturare i dati sul pubblico da Google Cloud Storage per Collaboration."
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-audience-sourcing" text="Consulta la guida"

Nella schermata di selezione dell&#39;origine dati sono elencati tutti i tipi di connessione disponibili. Seleziona **[!UICONTROL Google Cloud Storage]**, quindi **[!UICONTROL Next]**.

![Il flusso di lavoro Aggiungi pubblico mostra la schermata di selezione dell&#39;origine dati con Google Cloud Storage selezionato e Next evidenziato.](../../assets/setup/gcs-audience-sourcing/gcs-data-source-selection.png)

Viene visualizzata una finestra di dialogo dei prerequisiti che descrive i passaggi di configurazione richiesti (ad esempio, la configurazione del bucket GCS e l&#39;assegnazione del ruolo IAM) e rileva che i dati devono essere conformi alla **[[!UICONTROL specifica di Audience Sourcing]](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)**. Seleziona **[!UICONTROL Avvia onboarding]** per confermare la conformità prima di procedere.

![Prerequisiti per l&#39;elenco modale &quot;Prepara il bucket GCS per l&#39;onboarding&quot;, tra cui la creazione di un bucket GCS, la configurazione dell&#39;accesso IAM per Adobe e la conformità con le specifiche Audience Sourcing, con le opzioni Annulla e &quot;Avvia onboarding&quot;.](../../assets/setup/gcs-audience-sourcing/gcs-onboarding-prerequisites-dialog.png)

### Immetti i dettagli della connessione a [!DNL Google Cloud Storage] {#authenticate-gcs-connection}

Fornisci i dettagli necessari per consentire a Collaboration di accedere al bucket [!DNL Google Cloud Storage]. Dopo aver immesso le informazioni richieste, seleziona **[!UICONTROL Avanti]**.

| Campo | Descrizione |
| --- | --- |
| **[!UICONTROL Bucket]** | Nome del bucket [!DNL Google Cloud Storage]. Vedi [Valori richiesti prima di iniziare](#required-values). |
| **[!UICONTROL Percorso]** | Il prefisso del percorso all’interno del bucket in cui sono memorizzati i file del pubblico. |

![Il flusso di lavoro Aggiungi pubblico mostra il modulo di autenticazione di Google Cloud Storage con i campi del nome del bucket e del percorso della cartella e il pulsante Avanti disponibile.](../../assets/setup/gcs-audience-sourcing/gcs-data-connection-authentication.png)

### Conferma il consenso e la conferma dell’utilizzo dei dati {#confirm-consent}

Devi confermare che le rinunce al consenso sono state rimosse dai dati del pubblico prima che Collaboration possa elaborarli. Se non sei sicuro che i tuoi dati soddisfino questo requisito, consulta la [guida ai criteri di governance e alle azioni di applicazione](./onboard-audiences.md#governance-policy-and-enforcement-actions) prima di procedere. Selezionare la casella di controllo di conferma, quindi selezionare **[!UICONTROL OK]** per continuare.

### Fornisci dettagli di connessione {#provide-connection-details}

Immettere un nome e una descrizione facoltativa per la connessione dati. Il nome specificato viene visualizzato nella scheda **[!UICONTROL Connessioni dati personali]** e consente di distinguere questa origine se si gestiscono più connessioni dati.

* **[!UICONTROL Nome connessione dati]** (obbligatorio)
* **[!UICONTROL Descrizione connessione dati]** (facoltativo).

Seleziona **[!UICONTROL Avanti]** per continuare.

![Aggiungi flusso di lavoro di pubblico nel passaggio &quot;Fornisci dettagli&quot; che mostra i campi per il nome della connessione dati e la descrizione della connessione dati compilati con valori di esempio, con &quot;Successivo&quot; visibile nell&#39;angolo in alto a destra.](../../assets/setup/gcs-audience-sourcing/gcs-provide-details.png)

### Rivedi campi di identità mappati automaticamente {#auto-mapped-fields}

La schermata **[!UICONTROL Mapping]** è di sola lettura. Collaboration mappa automaticamente i campi di identità di origine dai file del pubblico ai campi di destinazione in base ai nomi di colonna definiti nelle specifiche di Audience Sourcing. In questa fase non è possibile aggiungere, rimuovere o applicare trasformazioni ai campi mappati.

>[!TIP]
>
>Seleziona **[!UICONTROL Anteprima dati di origine]** per rivedere un campione dei tuoi dati di pubblico in formato tabulare, quindi seleziona **[!UICONTROL Chiudi]** per tornare alla schermata di mappatura.

![La finestra di dialogo &quot;Anteprima dati GCS&quot; mostra una tabella di esempio di dati del pubblico con colonne quali AUDIENCE_ID e HASHED_EMAIL_SHA_256 e un pulsante Chiudi nell&#39;angolo in basso a destra.](../../assets/setup/gcs-audience-sourcing/gcs-data-preview.png){zoomable="yes"}

Verifica che le mappature visualizzate riflettano i campi nei file del pubblico. In caso contrario, arrestare e correggere i file in modo che siano conformi alle [specifiche di Audience Sourcing](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf) prima di procedere. Seleziona **[!UICONTROL Avanti]** per continuare.

![Aggiungi il flusso di lavoro del pubblico nel passaggio &quot;Mappa campi&quot; che mostra i campi di origine mappati automaticamente (AUDIENCE\_ID e HASHED\_EMAIL\_SHA\_256) per i campi di identità di destinazione, con l&#39;opzione &quot;Anteprima dati di origine&quot; visibile e il pulsante Avanti nell&#39;angolo in alto a destra.](../../assets/setup/gcs-audience-sourcing/gcs-mapping-auto-fields.png)

### Pianifica aggiornamento dati {#schedule-data-refresh}

Nella visualizzazione **[!UICONTROL Pianificazione]**, imposta la frequenza con cui Collaboration recupera i dati del pubblico aggiornati dal bucket GCS e definisci l&#39;intervallo di date attivo per la determinazione origine.

Utilizza il menu a discesa **[!UICONTROL Frequenza]** per selezionare la frequenza con cui Collaboration recupera i dati del pubblico aggiornati dal bucket GCS. Gli intervalli disponibili sono compresi tra **[!UICONTROL Giornalieri]** e **[!UICONTROL Ogni 6 giorni]**.

Digita un intervallo di date nel campo di input oppure seleziona l&#39;icona del calendario per impostare la **[!UICONTROL data di inizio]** e la **[!UICONTROL data di fine]** per il periodo di determinazione origine attivo. Una volta raggiunta la data di fine, la determinazione dell’origine cessa e i tipi di pubblico creati in precedenza scadono e non sono più disponibili per l’utilizzo in progetti di collaborazione.

>[!IMPORTANT]
>
>Imposta la frequenza di aggiornamento in modo che corrisponda o non superi la frequenza di aggiornamento dei dati del pubblico GCS sottostanti. L&#39;intervallo minimo di aggiornamento supportato è una volta ogni sei giorni. L’aggiornamento più frequente delle modifiche apportate ai dati consuma crediti Collaboration senza produrre risultati aggiornati. Per monitorare l&#39;utilizzo del credito, consulta [Monitorare l&#39;attività di consumo del credito](./my-activity.md).

![Aggiungi il flusso di lavoro del pubblico nel passaggio &quot;Pianificazione&quot; che mostra il menu a discesa Frequenza impostato su un intervallo ricorrente e un selettore di intervallo di date del calendario con date di inizio e fine evidenziate. &quot;Next&quot; è visibile nell&#39;angolo in alto a destra.](../../assets/setup/gcs-audience-sourcing/gcs-schedule-settings.png)

Seleziona **[!UICONTROL Avanti]** per continuare.

### Verifica e completa la connessione {#review-and-complete}

Rivedi il riepilogo della configurazione prima di creare la connessione. Nella schermata di riepilogo vengono visualizzate le sezioni seguenti:

* **[!UICONTROL Connessione dati]**: credenziali del bucket GCS e percorso della cartella configurati.
* **[!UICONTROL Dettagli]**: nome e descrizione facoltativa della connessione dati.
* **[!UICONTROL Mappatura]**: campi di identità di origine e di destinazione mappati automaticamente.
* **[!UICONTROL Pianificazione]**: frequenza di aggiornamento e intervallo di date attivo.

![Aggiungi il flusso di lavoro del pubblico nel passaggio &quot;Revisione&quot; che mostra un riepilogo delle sezioni di connessione dati, dettagli, mappatura e pianificazione con i valori configurati e il pulsante Completa visibile nell&#39;angolo in alto a destra.](../../assets/setup/gcs-audience-sourcing/gcs-review-summary.png)

Seleziona l&#39;icona della matita (![Un&#39;icona della matita.](../../assets/icons/edit.png)) accanto a qualsiasi sezione per tornare a quel passaggio e apportare modifiche. Quando tutte le sezioni sono corrette, selezionare **[!UICONTROL Completa]**.

Viene visualizzata una finestra di dialogo di conferma che indica che Collaboration ha creato la connessione dati e che è in corso la determinazione dell’origine del pubblico.

## Rivedere i tipi di pubblico originati {#review-sourced-audiences}

Dopo aver completato la configurazione guidata, Collaboration inizia a sourcing dei tipi di pubblico dal bucket GCS in modo asincrono. Passa a **[!UICONTROL Configurazione]** > **[!UICONTROL I miei tipi di pubblico]** per monitorare l&#39;avanzamento. Il processo di determinazione origine non viene completato immediatamente; il tempo necessario dipende dalle dimensioni dei dati e dalla frequenza di aggiornamento configurata.

### Monitorare l’avanzamento di audience sourcing {#monitor-sourcing-progress}

Mentre Collaboration recupera i dati del pubblico, un banner nella parte superiore dell&#39;area di lavoro **[!UICONTROL I miei tipi di pubblico]** indica che la determinazione dell&#39;origine è in corso. I singoli tipi di pubblico vengono visualizzati nell’elenco solo dopo il completamento della determinazione dell’origine per ciascun pubblico.

![Imposta l&#39;area di lavoro nella scheda &quot;I miei tipi di pubblico&quot; con un banner &quot;Origine pubblico in corso&quot; che indica che i tipi di pubblico provengono da una connessione dati di Google Cloud Storage, con l&#39;elenco dei tipi di pubblico visualizzato di seguito.](../../assets/setup/gcs-audience-sourcing/gcs-sourcing-in-progress.png)

>[!TIP]
>
>Il tempo di Audience sourcing varia in base alle dimensioni dei dati GCS e alla frequenza di aggiornamento configurata. Set di dati più grandi o pianificazioni di aggiornamento meno frequenti potrebbero richiedere più tempo per essere visualizzati nell&#39;area di lavoro **[!UICONTROL I miei tipi di pubblico]**.

### Visualizzare i dettagli del pubblico di origine {#view-audience-details}

Una volta completato il sourcing, i tipi di pubblico [!DNL Google Cloud Storage] vengono visualizzati nella scheda **[!UICONTROL Tipi di pubblico personali]** insieme ai tipi di pubblico ottenuti da altre connessioni. Seleziona un elemento riga o **[!UICONTROL Visualizza pubblico]** per aprire la visualizzazione dettagli per un pubblico specifico.

![La scheda &quot;I miei tipi di pubblico&quot; nell&#39;area di lavoro di configurazione mostra una tabella di tipi di pubblico, incluso un pubblico ottenuto da Google Cloud Storage, con caselle di controllo e azioni di riga selezionabili disponibili.](../../assets/setup/gcs-audience-sourcing/gcs-audience-list-view.png)

La vista dei dettagli mostra lo stato del pubblico, l’origine e il nome della connessione dati, insieme ai pannelli seguenti:

* **[!UICONTROL Identità]**: il conteggio e il raggruppamento delle identità totali per il pubblico, una volta che i dati diventano disponibili.
* **[!UICONTROL Categorie]**: qualsiasi tag applicato per organizzare o filtrare il pubblico.
* **[!UICONTROL Accesso alla connessione]**: pubblico privato, pubblico o condiviso con collaboratori specifici.
* **[!UICONTROL Visibilità metadati]**: quali informazioni sul pubblico, ad esempio il conteggio delle identità, la percentuale di sovrapposizione e l&#39;indice, sono visibili ai collaboratori.

![Visualizzazione dei dettagli dei singoli tipi di pubblico con Stato: Attivo, sistema di origine e nome della connessione dati nella parte superiore. Di seguito sono riportati i quattro pannelli: Identità che mostrano il conteggio e il raggruppamento delle identità, Categorie che mostrano i tag applicati, Accesso alla connessione che mostra il tipo e la visibilità dei metadati che mostrano le impostazioni per il conteggio delle identità, la percentuale di sovrapposizione e l&#39;indice del pubblico.](../../assets/setup/gcs-audience-sourcing/gcs-audience-details.png)

Esamina queste impostazioni prima di utilizzare il pubblico in un progetto di collaborazione. Per aggiornare le categorie, l&#39;accesso alla connessione o la visibilità dei metadati, consulta [Visualizzare e gestire singoli tipi di pubblico](./onboard-audiences.md#view-individual-audiences).

### Modificare le impostazioni del pubblico {#edit-audience-settings}

Puoi modificare i metadati del pubblico direttamente dalla visualizzazione elenco **[!UICONTROL Tipi di pubblico]** senza aprire la visualizzazione dettagli. Seleziona la casella di controllo di un pubblico per visualizzare la barra degli strumenti delle azioni, quindi seleziona un&#39;azione: **[!UICONTROL Modifica visibilità metadati]**, **[!UICONTROL Modifica accesso connessione]**, **[!UICONTROL Modifica nome e descrizione]**, **[!UICONTROL Modifica categorie]** o **[!UICONTROL Elimina]**.

![La visualizzazione elenco I miei tipi di pubblico mostra due tipi di pubblico, uno proveniente da Adobe Experience Platform e uno proveniente da Google Cloud Storage, con una riga selezionata utilizzando una casella di controllo, che mostra una barra degli strumenti inferiore con opzioni per Modifica visibilità metadati, Modifica accesso connessione, Modifica nome e descrizione, Modifica categorie ed Elimina.](../../assets/setup/gcs-audience-sourcing/gcs-audience-list-view-edit-options.png)

### Visualizzare la connessione dati GCS {#view-gcs-connection}

Per rivedere o gestire la connessione stessa, incluse le chiavi di corrispondenza e la pianificazione, passare a **[!UICONTROL Configurazione]** > **[!UICONTROL Connessioni dati personali]**. La nuova connessione GCS è immediatamente disponibile. L&#39;origine del pubblico viene visualizzata come **[!UICONTROL Google Cloud Storage]**.

## Limitazioni note {#known-limitations}

Tieni presente i seguenti vincoli durante la configurazione e l&#39;utilizzo di [!DNL Google Cloud Storage] audience sourcing:

* **Vincoli chiave di corrispondenza:** Una volta abilitata una chiave di corrispondenza per una connessione dati, non è possibile rimuoverla. È possibile aggiungere le chiavi di corrispondenza a una connessione esistente, ma non disattivarle o eliminarle. Per modificare le chiavi di corrispondenza attive, è necessario [eliminare la connessione dati](./manage-data-connection.md#delete-data-connection) e crearne una nuova.
* **Una connessione dati attiva per origine:** È supportata una sola connessione dati attiva [!DNL Google Cloud Storage] alla volta. Se devi creare l&#39;origine dei tipi di pubblico da un bucket diverso, [elimina la connessione esistente](./manage-data-connection.md#delete-data-connection) e creane una nuova che punti al nuovo bucket.
* **Supporto sottocartelle:** i file del pubblico devono trovarsi direttamente nel percorso della cartella specificato. Collaboration non attraversa le sottocartelle all’interno di tale percorso.

## Risoluzione dei problemi {#troubleshooting}

Utilizzare questa sezione per risolvere i problemi che si verificano dopo la connessione iniziale. Per gli errori che si verificano durante l’autenticazione, controlla le credenziali e le autorizzazioni del bucket o contatta l’amministratore.

**I tipi di pubblico non vengono visualizzati o l&#39;origine richiede più tempo del previsto**

* Il tempo di determinazione origine viene scalato in base al volume dei dati e alla frequenza di aggiornamento configurata. Per i set di dati di grandi dimensioni è previsto un tempo di elaborazione esteso.
* Se i tipi di pubblico non vengono visualizzati entro 24 ore, verifica che i file del pubblico siano presenti nel percorso della cartella specificato durante l’installazione e siano conformi alle specifiche di Audience Sourcing.
* Controllare la scheda **[!UICONTROL Le mie connessioni dati]** per verificare la presenza di indicatori di errore sulla connessione.
* Se il problema persiste dopo aver completato questi passaggi, contatta l’Assistenza clienti di Adobe e fornisci il nome della connessione dati e i dettagli del bucket.

**La connessione dati mostra uno stato di errore dopo l&#39;esecuzione iniziale**

* Verifica che le autorizzazioni e le credenziali del bucket GCS non siano state modificate dopo la creazione della connessione. Qualsiasi modifica che rimuova l’accesso di Adobe al bucket causa un errore nelle esecuzioni successive dell’origine.
* Verifica che i file del pubblico esistano ancora nel percorso della cartella configurato e siano conformi alle specifiche di Audience Sourcing.
* Se il problema persiste dopo aver confermato le autorizzazioni e la disponibilità dei file, [elimina la connessione](./manage-data-connection.md#delete-data-connection) e creane una nuova, oppure contatta l&#39;assistenza clienti Adobe.

**Errori di formato del file del pubblico durante un aggiornamento pianificato**

* Conferma che i file aggiornati nel bucket siano conformi ai requisiti relativi alla struttura delle colonne e ai campi nella [Specifica di origine pubblico](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf).
* Assicurati che tutti i file nel percorso della cartella configurata utilizzino strutture di colonna identiche. I file in formato misto nello stesso percorso possono causare errori di sourcing parziali.

## Passaggi successivi {#next-steps}

[!DNL Google Cloud Storage] è stato configurato come origine dati in Collaboration. Al termine dell&#39;origine, i tipi di pubblico sono disponibili nell&#39;area di lavoro **[!UICONTROL Tipi di pubblico]** e pronti per essere utilizzati nei progetti di collaborazione.

Da qui, puoi:

* [Creare e gestire progetti di collaborazione](../collaborate/manage-projects.md)
* [Attivare i tipi di pubblico all’interno di un progetto](../collaborate/activate.md)
* [Verifica le sovrapposizioni e misura le prestazioni](../collaborate/measure.md)
* [Gestire le impostazioni e la visibilità del pubblico](./onboard-audiences.md#view-individual-audiences)
* [Gestisci le chiavi e la pianificazione della connessione dati](./manage-data-connection.md)

Per altri metodi di determinazione dell&#39;origine del pubblico, vedi:

* [Configura [!DNL Amazon S3] per audience sourcing](./configure-aws-s3-audience-sourcing.md)
* [Configura [!DNL Snowflake] per audience sourcing](./configure-snowflake-audience-sourcing.md)
* [Tipi di pubblico di Source da Experience Platform](./onboard-audiences.md)
* [Caricare un file CSV per l’audience sourcing](./upload-csv-audience-sourcing.md)
