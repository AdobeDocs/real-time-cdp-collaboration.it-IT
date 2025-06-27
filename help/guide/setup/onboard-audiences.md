---
title: Importare e gestire i tipi di pubblico
description: Scopri come importare e gestire i tipi di pubblico in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: fda414120decc0c76712616ff85b83febede53e9
workflow-type: tm+mt
source-wordcount: '2961'
ht-degree: 20%

---

# Importare e gestire i tipi di pubblico

{{limited-availability-release-note}}

I tipi di pubblico sono gruppi specifici di utenti o clienti segmentati in base a vari attributi. Questi consentono agli inserzionisti e agli editori di collaborare a marketing mirato ed esperienze personalizzate per campagne pubblicitarie più efficaci.

Utilizza questa pagina come collegamento per comprendere tutte le metriche rilevanti che puoi visualizzare in relazione ai tipi di pubblico, nonché i passaggi del flusso di lavoro per importare un pubblico in Adobe Real-Time CDP Collaboration.

>[!TIP]
>
>Utilizza le informazioni in questa schermata per ottenere tutte le informazioni necessarie sui tipi di pubblico e le [schermate di individuazione e sovrapposizione](/help/guide/collaborate/discover.md) per ottenere informazioni su quali tipi di pubblico funzionerebbero meglio per diversi tipi di campagna, se confrontate con l&#39;inventario di publisher.

>[!BEGINSHADEBOX]

Cosa troverai in questa pagina della documentazione:

* [Importare tipi di pubblico in Real-Time CDP Collaboration](#import-audiences)
* [Visualizza dashboard dei tipi di pubblico](#view-audiences-dashboard)
* [Visualizzare singoli tipi di pubblico](#view-individual-audiences)

>[!ENDSHADEBOX]

## Importare tipi di pubblico in Real-Time CDP Collaboration {#import-audiences}

>[!IMPORTANT]
>
>Per importare dei tipi di pubblico, l’utente deve essere assegnato a un ruolo contenente due autorizzazioni di Gestione profilo: Visualizza profili e Visualizza segmenti. Per informazioni sull&#39;assegnazione delle autorizzazioni necessarie, consultare la [guida all&#39;importazione del pubblico](../permissions/overview.md#audience-importation).

Prima di poter attivare i tipi di pubblico con i collaboratori ed eseguire calcoli di sovrapposizione, è necessario importarli in Real-Time CDP Collaboration. Per importare dei tipi di pubblico, segui i passaggi del flusso di lavoro descritti nella sezione seguente.

Dalla scheda **[!UICONTROL I miei tipi di pubblico]** nell&#39;area di lavoro **[!UICONTROL Configurazione]**, seleziona l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) o l&#39;opzione **[!UICONTROL Aggiungi]**, quindi seleziona **Pubblico**.

![Area di lavoro Tipi di pubblico personali con le opzioni Aggiungi e Tipi di pubblico evidenziate.](/help/assets/setup/add-manage-audiences/add-audiences.png)

### Selezionare la connessione dati {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Azioni di marketing"
>abstract="<p>Utilizza le azioni di marketing per controllare quali dati del pubblico importare in Real-Time CDP Collaboration da Experience Platform. L’azione di marketing <strong>Collaborazione sui dati</strong> supporta le etichette di utilizzo dei dati C4, C5 e C9. L’azione di marketing <strong>Data science</strong> supporta l’etichetta di utilizzo dati C9.</p> <p> <ul><li> Quando la casella di controllo è <em>abilitata</em>, tutti i dati contrassegnati con le etichette richiamate in precedenza in Experience Platform vengono esclusi e <strong>non</strong> vengono inseriti in Real-Time CDP Collaboration.</li><li> Se la casella di controllo è <em>disabilitata</em>, i dati provenienti da Experience Platform che possono essere importati in Real-Time CDP Collaboration non sono soggetti a restrizioni.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=it" text="Panoramica sulle etichette di utilizzo dei dati"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=it" text="Glossario delle etichette di utilizzo dei dati"

>[!IMPORTANT]
>
>Dopo aver stabilito nella prima connessione dati e aver importato il primo pubblico, puoi importare più tipi di pubblico dalla connessione dati esistente. Quando aggiungi altri tipi di pubblico, inizierai dal passaggio [seleziona pubblico](#select-audience), poiché tutte le informazioni sui prerequisiti degli altri passaggi verranno importate dalla connessione esistente.

Una connessione dati è l’origine dei dati da cui si importano i tipi di pubblico in Real-Time CDP Collaboration. Attualmente, l’unica connessione dati supportata è Adobe Experience Platform.

Tutte le impostazioni, ad esempio la pianificazione configurata per la connessione dati, vengono applicate a tutti i tipi di pubblico importati da questa connessione dati.

>[!TIP]
>
>È disponibile un flusso di lavoro separato in cui è possibile visualizzare e modificare le connessioni dati. Per ulteriori informazioni, seguire la [guida alla gestione delle connessioni dati](/help/guide/setup/manage-data-connection.md).

Per iniziare ad aggiungere la connessione dati, selezionare **[!UICONTROL Aggiungi una nuova connessione dati]**, quindi selezionare **[!UICONTROL Avanti]**.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione Aggiungi una nuova connessione dati evidenziata.](/help/assets/setup/add-manage-audiences/add-data-connection.png)

#### Seleziona origine dati

Scegliere quindi l&#39;origine per la connessione dati. Le fonti disponibili includono:

* **Adobe Experience Platform**: seleziona questa opzione per inserire i tipi di pubblico da Adobe Experience Platform Real-Time CDP.
* **File CSV** (versione futura): carica un file CSV contenente i dati del pubblico per acquisire dati in modo rapido e semplice.
* **Amazon Web Services** (versione futura): connettiti all&#39;archiviazione Amazon S3 per importare i dati del pubblico direttamente dai bucket S3.
* **Snowflake** (versione futura): utilizza il data warehouse di Snowflake per estrarre facilmente i dati sul pubblico.

Seleziona la tua origine dati, quindi seleziona **[!UICONTROL Avanti]**.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione Adobe Experience Platform evidenziata.](/help/assets/setup/add-manage-audiences/select-data-connection-source.png)

#### Seleziona sandbox

Dopo aver selezionato l’origine dati, devi selezionare la sandbox che include i tipi di pubblico da importare. Seleziona la sandbox dall&#39;elenco delle sandbox disponibili, quindi seleziona **[!UICONTROL Successivo]**

![L&#39;area di lavoro Aggiungi tipi di pubblico con una sandbox selezionata.](/help/assets/setup/add-manage-audiences/select-sandbox.png)

#### Criteri di governance e azioni di applicazione {#governance-policy-and-enforcement-actions}

Successivamente, assicurati che le azioni di marketing corrette siano impostate sui dati importati. È inoltre necessario fornire il consenso per i dati importati da Real-Time CDP da utilizzare per la collaborazione sui dati.

Utilizza le azioni di marketing per controllare quali dati del pubblico importare in Real-Time CDP Collaboration da Experience Platform. L’azione di marketing **Collaborazione sui dati** supporta le etichette di utilizzo dei dati C4, C5 e C9. L’azione di marketing **Data science** supporta l’etichetta di utilizzo dati C9.

Ulteriori informazioni sulle etichette di utilizzo dei dati [C4, C5 e C9](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* Quando la casella di controllo è *abilitata*, tutti i dati contrassegnati con le etichette richiamate in precedenza in Experience Platform vengono esclusi e *non* vengono inseriti in Real-Time CDP Collaboration.
* Se la casella di controllo è *disabilitata*, i dati provenienti da Experience Platform che possono essere importati in Real-Time CDP Collaboration non sono soggetti a restrizioni.

Ulteriori informazioni sulle etichette di utilizzo dei dati nella documentazione di Experience Platform:

* [Panoramica delle etichette di utilizzo dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Glossario delle etichette di utilizzo dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/reference){target="_blank"}

Inoltre, seleziona le regole di predefinito da applicare ai dati importati in Real-Time CDP Collaboration.

![L&#39;area di lavoro Aggiungi tipi di pubblico nella sezione Criteri di governance e azioni efficaci.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

Dopo aver selezionato le azioni di marketing e le regole di consenso, seleziona **[!UICONTROL Successivo]** per procedere al passaggio successivo. Viene visualizzata una finestra di dialogo di conferma in cui viene richiesto di accettare i termini. Selezionare la casella di controllo, quindi selezionare **[!UICONTROL OK]** per confermare.

![Finestra di dialogo Criteri di governance e azioni efficaci con la casella di controllo e l&#39;opzione OK evidenziate.](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png)

### Fornisci dettagli

Quindi, fornisci un nome e una descrizione per la connessione dati. Queste informazioni ti aiuteranno a identificare la connessione dati in un secondo momento.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione di fornire un nome e una descrizione.](/help/assets/setup/add-manage-audiences/data-connection-details.png)

### Mappare i campi {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Campi origine"
>abstract="I campi origine sono spazi dei nomi e attributi di identità provenienti dall’implementazione esistente di Real-Time CDP. Puoi mapparli ai campi di destinazione definiti in Real-Time CDP Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Campi di destinazione"
>abstract="Attualmente, gli indirizzi e-mail con hash sono le uniche chiavi di corrispondenza supportate."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Applica trasformazione"
>abstract="Se importi dall’origine dei campi *senza hash*, utilizza questa opzione affinché Real-Time CDP Collaboration possa applicare l’hashing e trasformare i campi normali in campi con hash."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_identity_namespaces"
>title="Spazi dei nomi delle identità"
>abstract="Seleziona uno spazio dei nomi delle identità tra quelli standard e personalizzati disponibili nella tua organizzazione Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html?lang=it#standard" text="Spazi dei nomi standard e di identità in Experience Platform"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_profile_attributes"
>title="Attributi del profilo"
>abstract="Seleziona gli attributi dallo schema di unione per la classe Profilo in Experience Platform. Questa vista mostra gli attributi presenti nello schema di unione e appartenenti alla classe Profilo individuale XDM."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=it" text="Schema di unione in Experience Platform"

Quindi, seleziona i campi sorgente da mappare ai campi di destinazione in Real-Time CDP Collaboration.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione di mappare i campi di origine ai campi di destinazione.](/help/assets/setup/add-manage-audiences/add-map-fields.png)

>[!TIP]
>
>Puoi mappare più campi sorgente allo stesso campo di destinazione. Se ad esempio gli indirizzi e-mail sono contenuti in due campi distinti di Experience Platform, è possibile mappare entrambi al campo di destinazione **[!UICONTROL E-mail con hash]** come due righe separate.

>[!BEGINSHADEBOX]

I **[!UICONTROL campi Source]** sono spazi dei nomi di identità e attributi dell&#39;implementazione esistente di Real-Time CDP. Queste sono le identità presenti nell&#39;origine da cui stai importando i dati. I campi Source vengono mappati sui campi target definiti in Real-Time CDP Collaboration.

**[!UICONTROL I campi di destinazione]** indicano il riferimento alle identità in Real-Time CDP Collaboration. Attualmente, gli indirizzi e-mail con hash sono le uniche chiavi di corrispondenza supportate.

Utilizza l&#39;opzione **[!UICONTROL Applica trasformazione]** quando importi *campi senza hash* dall&#39;origine. In questo caso, Real-Time CDP Collaboration applicherà l’hashing e trasformerà i campi. L’algoritmo di hashing utilizzato da Adobe è SHA256.

>[!ENDSHADEBOX]

Seleziona il campo di origine vuoto accanto al campo di destinazione. Verrà visualizzata la finestra di dialogo **[!UICONTROL Seleziona campo di origine]**. Seleziona tra le opzioni **[!UICONTROL Spazi dei nomi identità]** e **[!UICONTROL Attributi profilo]** per trovare il campo di origine desiderato, quindi seleziona il campo di origine dall&#39;elenco, utilizzando l&#39;opzione di ricerca per trovare il campo desiderato.

![Finestra di dialogo Seleziona campo di origine con le opzioni e-mail visualizzate.](/help/assets/setup/add-manage-audiences/select-source-field.png)

Per gestire più campi e-mail, mappa il campo dell&#39;origine e-mail senza hash utilizzando **[!UICONTROL Applica trasformazione]**.

![L&#39;area di lavoro Aggiungi tipi di pubblico con i campi di origine e-mail mappati al campo di destinazione, con Applica trasformazione attivata per uno.](/help/assets/setup/add-manage-audiences/apply-transformation.png)

Continua ad aggiungere coppie di mappatura in base alle esigenze, quindi seleziona **[!UICONTROL Avanti]**.

### Pianificazione {#schedule}

Successivamente, pianifica quando iniziare e finire di popolare i tipi di pubblico. Il pubblico verrà aggiornato in base a questa pianificazione.

![L&#39;area di lavoro Aggiungi pubblico con le opzioni di pianificazione visualizzate.](/help/assets/setup/add-manage-audiences/audience-scheduling.png)

>[!IMPORTANT]
>
>Regolando la frequenza degli aggiornamenti del pubblico sarà possibile gestire l&#39;attività di credito di [Gestione dell&#39;audience](/help/guide/setup/my-activity.md#types-of-activities), calcolata per aggiornamento dell&#39;audience. La selezione di una frequenza più elevata può influire sull’aggiornamento dei dati disponibili per i rapporti di individuazione del pubblico e l’attivazione del pubblico.

Seleziona la frequenza di aggiornamento del pubblico dal menu a discesa **[!UICONTROL Frequenza]**.

![L&#39;area di lavoro Aggiungi pianificazione tipi di pubblico con il menu a discesa Frequenza aperto.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png)

Selezionare quindi l&#39;**[!UICONTROL intervallo di date]**. La data di inizio è la data in cui il pubblico inizierà a essere popolato con profili e la data di fine è la data in cui il pubblico smetterà di aggiornarsi.

![L&#39;area di lavoro Aggiungi pianificazione tipi di pubblico con l&#39;opzione Intervallo date visualizzata.](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png)

>[!IMPORTANT]
>
>Dopo la data di fine nell’intervallo di date, tutti i tipi di pubblico importati da questa connessione dati cesseranno di essere aggiornati. Per rinnovare la connessione, passare a [Gestisci connessione dati](/help/guide/setup/manage-data-connection.md) e impostare una nuova data di fine.

### Seleziona tipi di pubblico {#select-audience}

Dopo aver selezionato la sorgente del pubblico, scegli tipi di pubblico specifici da includere. Utilizza le opzioni di ricerca e filtro per trovare i tipi di pubblico rilevanti dall’origine dati. Seleziona i tipi di pubblico desiderati, quindi seleziona **[!UICONTROL Successivo]**.

![Area di lavoro Aggiungi tipi di pubblico con un elenco dei tipi di pubblico disponibili.](/help/assets/setup/add-manage-audiences/select-audience.png)

### Rivedi

Rivedi tutte le configurazioni e le impostazioni prima di finalizzare l’aggiunta di pubblico. Verifica che tutti i dettagli siano corretti, quindi seleziona **[!UICONTROL Completa]** per completare la creazione della connessione dati.

![Area di lavoro Aggiungi tipi di pubblico con tutte le configurazioni selezionate visualizzate.](/help/assets/setup/add-manage-audiences/review-connection.png)

## Visualizza dashboard dei tipi di pubblico {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Identità mancanti"
>abstract="Il conteggio delle identità sarà disponibile dopo il successivo aggiornamento della connessione dati dopo la pianificazione configurata. L’aggiornamento iniziale si verifica in genere entro 24 ore dalla configurazione della connessione dati. Gli aggiornamenti ricorrenti seguiranno la pianificazione configurata. "

Dopo aver importato i tipi di pubblico in Real-Time CDP Collaboration, nell&#39;area di lavoro **[!UICONTROL Tipi di pubblico personali]** vengono visualizzati tutti i tipi di pubblico attualmente importati in Real-Time CDP Collaboration dall&#39;organizzazione.


Ogni pubblico contiene una panoramica delle seguenti informazioni:

| Elemento | Descrizione |
|----------|---------|
| **[!UICONTROL Identità]** | Indica il numero di identità presenti nel pubblico. Tieni presente che se lo stesso profilo ha due o più identità e queste vengono utilizzate come chiavi di corrispondenza nel progetto, il profilo verrà visualizzato due volte nel conteggio. |
| **[!UICONTROL Stato]** | Indica se il pubblico è attivo e può essere utilizzato nei progetti. Lo stato **[!UICONTROL In sospeso]** indica che il pubblico è stato importato di recente e che i membri del pubblico devono ancora essere popolati. I tipi di pubblico importati verranno compilati con profili dopo l’aggiornamento iniziale, che in genere si verifica entro 24 ore dalla configurazione della connessione dati. |
| **[!UICONTROL Source]** | Indica l’origine da cui è stato importato il pubblico. Nell’attuale versione di Real-Time CDP Collaboration, Adobe Experience Platform è l’unica origine supportata. |
| **[!UICONTROL Connessione dati]** | La connessione dati da cui proviene il pubblico. Puoi selezionare il nome per visualizzare la connessione dati. |
| **[!UICONTROL Accesso alla connessione]** | Definisce se il pubblico è privato o pubblico. I tipi di pubblico sono rilevabili nei rapporti di sovrapposizione e possono essere attivati all’interno di un progetto. |
| **[!UICONTROL Creato]** | Indica quando il pubblico è stato importato in Real-Time CDP Collaboration. |
| **[!UICONTROL Ultimo aggiornamento]** | Indica la data e l’ora dell’ultimo aggiornamento di un qualsiasi aspetto del pubblico. |

![L&#39;area di lavoro Il mio pubblico mostra tutti i tipi di pubblico importati.](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

Per eseguire azioni rapide su un pubblico, seleziona i puntini di sospensione **...** accanto al nome del pubblico. Sono disponibili le seguenti opzioni:

* **[!UICONTROL Modifica categorie]** ti consente di aggiungere al pubblico tag di categoria diversi. Per ulteriori informazioni, consulta la sezione [categorie](#categories) di seguito.
* **[!UICONTROL Elimina]** eliminerà il pubblico dalla connessione dati.

![Nell&#39;area di lavoro I miei tipi di pubblico è aperta l&#39;area di lavoro con il menu con i puntini di sospensione e sono evidenziate le opzioni Modifica categorie ed Elimina.](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png)

## Visualizzare singoli tipi di pubblico {#view-individual-audiences}

Per visualizzare ulteriori informazioni e modificare le configurazioni per un singolo pubblico, seleziona il pubblico dall&#39;area di lavoro **[!UICONTROL Tipi di pubblico]**. L’area di lavoro pubblico visualizza informazioni dettagliate sul pubblico selezionato, inclusi dettagli, identità, categorie, accesso alla connessione e impostazioni di visibilità dei metadati.

### Dettagli del pubblico

Per ogni singolo pubblico vengono visualizzate le seguenti informazioni:

| Elemento | Descrizione |
|----------|---------|
| **[!UICONTROL Stato]** | Indica se il pubblico è attivo e può essere utilizzato nei progetti. |
| **[!UICONTROL Source]** | Indica l’origine da cui è stato importato il pubblico. Nell’attuale versione di Real-Time CDP Collaboration, Adobe Experience Platform è l’unica origine supportata. |
| **[!UICONTROL Connessione dati]** | La connessione dati da cui proviene il pubblico. |
| **[!UICONTROL Ultimo aggiornamento]** | Indica la data e l’ora dell’ultimo aggiornamento del pubblico. |
| **[!UICONTROL Ultimo aggiornamento eseguito da]** | Indica l’ultimo utente che ha aggiornato il pubblico. |
| **[!UICONTROL Creato]** | Indica quando il pubblico è stato importato in Real-Time CDP Collaboration. |
| **[!UICONTROL Creato da]** | Indica l’utente che ha importato il pubblico in Real-Time CDP Collaboration. |

![Area di lavoro di un singolo pubblico.](/help/assets/setup/add-manage-audiences/audience-details.png)

Inoltre, nell’area di lavoro del pubblico sono disponibili i seguenti controlli:

* **[!UICONTROL Elimina]**: rimuovi il pubblico dalla connessione dati.
* **[!UICONTROL Modifica]**: modifica il nome o la descrizione del pubblico.

![Area di lavoro di un singolo pubblico con l&#39;opzione Modifica ed Elimina evidenziata.](/help/assets/setup/add-manage-audiences/audience-details-edit-delete.png)

Successivamente, puoi aggiornare le seguenti sezioni all’interno dell’area di lavoro del pubblico:

* [Identità](#identities)
* [Categorie](#categories)
* [Accesso connessione](#connection-access)
* [Visibilità dei metadati](#metadata-visibility)

### Identità {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identità"
>abstract="Una vista con raggruppamenti delle identità che compongono il pubblico, nonché un conteggio totale dei profili con le rispettive identità."

La sezione **[!UICONTROL Identità]** indica il numero di profili presenti nel pubblico con una qualsiasi delle identità selezionate al momento dell&#39;importazione del pubblico. La sezione contiene anche un raggruppamento delle identità in modo da poter individuare le identità che compongono il maggior numero possibile di persone appartenenti al pubblico.

![Sezione Identità dell&#39;area di lavoro di un singolo pubblico.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

### Categorie {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Categorie"
>abstract="Assegna tag ai tipi di pubblico per semplificarne l’organizzazione, il filtraggio e il recupero. Puoi assegnare a un pubblico i tag di più categorie, e utilizzare quindi tali categorie per filtrare i tipi di pubblico desiderati in altre aree del prodotto."

Per facilitare l’organizzazione, il filtraggio e il recupero del pubblico, puoi assegnare tag ai tipi di pubblico. Puoi assegnare tag a un pubblico con più categorie, quindi utilizzare questi tag per filtrare i tipi di pubblico desiderati nell&#39;area di prodotto [discovery](/help/guide/collaborate/discover.md) durante l&#39;esecuzione di report di sovrapposizione pubblico.

Per aggiungere categorie, selezionare l&#39;opzione **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Categorie]**.

![Sezione Categorie dell&#39;area di lavoro di un singolo pubblico.](/help/assets/setup/add-manage-audiences/audience-details-categories.png)

Verrà visualizzata la finestra di dialogo **[!UICONTROL Categorie]**, che consente di selezionare le categorie da aggiungere al pubblico. Per selezionare una singola categoria, selezionare la casella di controllo accanto al nome della categoria.

![Viene visualizzata la finestra di dialogo Categorie con le categorie disponibili.](/help/assets/setup/add-manage-audiences/audience-details-categories-select.png)

### Accesso connessione {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Accesso connessione"
>abstract="<p>I tipi di pubblico possono essere di tre tipi: pubblico, privato e personalizzato.</p><p> La relativa disponibilità per l’utilizzo in progetti con collaboratori varia in base alle impostazioni di accesso della connessione. È sempre possibile cambiare l’accesso della connessione da privato a pubblico, ma non è possibile ripristinare tale impostazione una volta che un pubblico viene attivato con i collaboratori.</p>"

La disponibilità di un pubblico da utilizzare nei progetti con collaboratori varia in base all’impostazione di accesso alla connessione. Nella sezione **[!UICONTROL Accesso alla connessione]**, puoi selezionare se il pubblico deve essere privato o utilizzabile e individuabile nelle connessioni.

Per aggiornare l&#39;accesso alla connessione del pubblico, seleziona l&#39;opzione **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Accesso alla connessione]**.

![Sezione di accesso alla connessione dell&#39;area di lavoro di un singolo pubblico.](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Accesso connessione]**, con tre opzioni di accesso alla connessione disponibili:

* **[!UICONTROL Pubblico privato]**. Questi tipi di pubblico sono *non* disponibili per l&#39;utilizzo in report di sovrapposizione o per l&#39;attivazione in connessioni con collaboratori. Anche se i tipi di pubblico non sono disponibili per i collaboratori per la visualizzazione o l&#39;utilizzo, la popolazione dei tipi di pubblico contribuisce comunque alla popolazione totale nella visualizzazione **[!UICONTROL Tutti i tipi di pubblico]** nella sezione [confronta tipi di pubblico](/help/guide/collaborate/discover.md#compare-audiences). Modifica l’impostazione su public (pubblico) o custom (personalizzato) per utilizzare i tipi di pubblico nelle connessioni con i collaboratori.
* **[!UICONTROL Pubblico pubblico]**. Questi tipi di pubblico sono disponibili per l’utilizzo in rapporti di sovrapposizione e per l’attivazione in connessioni con qualsiasi collaboratore.
* **[!UICONTROL Pubblico personalizzato]**. Questi tipi di pubblico sono disponibili per l’utilizzo in rapporti di sovrapposizione e per l’attivazione solo in connessioni specifiche. Anche se i tipi di pubblico non sono disponibili per i collaboratori per la visualizzazione o l&#39;utilizzo, la popolazione dei tipi di pubblico contribuisce comunque alla popolazione totale nella visualizzazione **[!UICONTROL Tutti i tipi di pubblico]** nella sezione [confronta tipi di pubblico](/help/guide/collaborate/discover.md#compare-audiences).

Seleziona l&#39;opzione di accesso alla connessione desiderata, quindi seleziona **[!UICONTROL Salva]** per applicare le modifiche.

![Viene visualizzata la finestra di dialogo Accesso alla connessione con le opzioni disponibili.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

>[!IMPORTANT]
>
>Indipendentemente dallo stato di accesso (pubblico, privato o personalizzato), la popolazione di qualsiasi pubblico contribuisce alla popolazione **[!UICONTROL Tutti i tipi di pubblico]** nella sezione **[!UICONTROL Confronta tipi di pubblico]** all&#39;interno di un progetto.<br>

La disponibilità del pubblico da utilizzare nei progetti con collaboratori varia in base all’impostazione di accesso alla connessione. È sempre possibile cambiare l’accesso alla connessione da privato a pubblico, ma non è possibile ripristinare tale impostazione dopo l’attivazione di un pubblico.

### Visibilità dei metadati {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Visibilità dei metadati"
>abstract="<p>Indica quali metadati del pubblico sono visibili ad altre organizzazioni prima che si connettano alla tua organizzazione. </p> <p> Il **conteggio delle identità** controlla se il partner può visualizzare i conteggi delle identità per i tipi di pubblico quando visualizza i report di sovrapposizione nella scheda di individuazione. La **% di sovrapposizione del pubblico** controlla se i collaboratori sono in grado di individuare percentuali di sovrapposizione tra i propri tipi di pubblico e e il tuo."

>[!NOTE]
>
>Se tutti i tipi di pubblico del tuo collaboratore sono impostati su privato, la sezione **[!UICONTROL Tipi di pubblico rilevanti]** di un progetto nell&#39;area di lavoro **[!UICONTROL Discover]** sarà vuota. Per ulteriori informazioni, leggere [individuazione](/help/guide/collaborate/discover.md#relevant-audiences). guida.

La visibilità dei metadati indica la visibilità dei metadati di un pubblico per altre organizzazioni prima che si connettano all’organizzazione o in diverse visualizzazioni del progetto. Per aggiornare la visibilità dei metadati del pubblico, seleziona l&#39;opzione **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Visibilità metadati]**.

![Sezione visibilità metadati dell&#39;area di lavoro di un singolo pubblico.](/help/assets/setup/add-manage-audiences/audience-details-metadata.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Visibilità metadati]**, che consente di configurare le impostazioni di visibilità per il pubblico. È possibile configurare due impostazioni di visibilità dei metadati per ogni pubblico:

**[!UICONTROL Mostra conteggio identità]**: questa impostazione controlla se il tuo collaboratore può visualizzare i conteggi delle identità per i tuoi tipi di pubblico quando [visualizzi i report di sovrapposizione nella scheda di individuazione](/help/guide/collaborate/discover.md#discover-overlaps) all&#39;interno di un progetto.

**[!UICONTROL Mostra sovrapposizione pubblico %]**: se è impostato su true, i collaboratori sono in grado di [individuare percentuali di sovrapposizione](/help/guide/collaborate/discover.md#compare-audiences) tra i propri tipi di pubblico e quelli dell&#39;utente.

![Viene visualizzata la finestra di dialogo Visibilità metadati con le opzioni disponibili.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

## Passaggi successivi

Dopo aver importato i tipi di pubblico, è ora di individuare gli editori che si connettono a [connect](/help/guide/connect/establishing-connections.md) e iniziare a collaborare ai progetti.
