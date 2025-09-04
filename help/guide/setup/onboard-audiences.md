---
title: Source e gestire i tipi di pubblico
description: Scopri come individuare e gestire i tipi di pubblico in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: 4f1582b489d99e9e8257c3808ec5863dbc74ef7a
workflow-type: tm+mt
source-wordcount: '3277'
ht-degree: 15%

---

# Source e gestire i tipi di pubblico

{{limited-availability-release-note}}

I tipi di pubblico sono gruppi specifici di utenti o clienti segmentati in base a vari attributi. Questi consentono ai collaboratori di collaborare su marketing mirato ed esperienze personalizzate per campagne pubblicitarie più efficaci. Questa guida illustra come individuare il pubblico in Real-Time CDP Collaboration, visualizzare la dashboard dei tipi di pubblico e gestire i singoli tipi di pubblico.

## Tipi di pubblico di Source in Collaboration {#source-audiences}

>[!IMPORTANT]
>
>Per originare i tipi di pubblico, l&#39;utente deve essere assegnato a un ruolo contenente due autorizzazioni per la gestione dei profili: **[!UICONTROL Visualizza profili]** e **[!UICONTROL Visualizza segmenti]**. Per informazioni sull&#39;assegnazione delle autorizzazioni necessarie, fare riferimento alla [guida di audience sourcing](../permissions/overview.md#audience-sourcing) in autorizzazioni.

Prima di poter attivare i tipi di pubblico con i collaboratori ed eseguire calcoli di sovrapposizione, è necessario che i tipi di pubblico vengano inseriti in Collaboration. Per sorgente i tipi di pubblico, segui i passaggi del flusso di lavoro descritti nella sezione seguente.

Dalla scheda **[!UICONTROL Tipi di pubblico]** nell&#39;area di lavoro **[!UICONTROL Configurazione]**, selezionare l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) e quindi selezionare **[!UICONTROL Pubblico]**. Se questo è il tuo primo pubblico, puoi anche selezionare l&#39;opzione **[!UICONTROL Aggiungi]**.

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
>Dopo aver stabilito nella prima connessione dati e aver importato il primo pubblico, puoi importare più tipi di pubblico dalla connessione dati esistente. Quando aggiungi altri tipi di pubblico, inizierai dal passaggio [seleziona pubblico](#select-audiences), in quanto la connessione dati è già stata stabilita.

Una connessione dati è l&#39;origine dei dati da cui si estraggono i tipi di pubblico. Attualmente, l’unica connessione dati supportata è Adobe Experience Platform.

Tutte le impostazioni, ad esempio la pianificazione configurata per la connessione dati, vengono applicate a tutti i tipi di pubblico originati da questa connessione dati.

>[!TIP]
>
>È disponibile un flusso di lavoro separato in cui è possibile visualizzare e modificare le connessioni dati. Per ulteriori informazioni, seguire la [guida alla gestione delle connessioni dati](/help/guide/setup/manage-data-connection.md).

Per iniziare ad aggiungere la tua connessione dati, seleziona **[!UICONTROL Aggiungi una nuova connessione dati]**, quindi seleziona **[!UICONTROL Avanti]**.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione Aggiungi una nuova connessione dati evidenziata.](/help/assets/setup/add-manage-audiences/add-data-connection.png)

#### Seleziona origine dati

Scegliere quindi l&#39;origine per la connessione dati. Le fonti disponibili includono:

* **Adobe Experience Platform**: seleziona questa opzione per richiamare i tipi di pubblico da Adobe Experience Platform.
* **File CSV** (versione futura): carica un file CSV contenente i dati del pubblico per acquisire dati in modo rapido e semplice.
* **Amazon Web Services** (versione futura): collegati all&#39;archiviazione Amazon S3 per generare i dati del pubblico direttamente dai bucket S3.
* **Snowflake** (versione futura): utilizza il data warehouse di Snowflake per estrarre facilmente i dati sul pubblico.
* **Piattaforma Google Cloud** (versione futura): connettiti al tuo Google Cloud Storage per sorgente i dati del pubblico direttamente dai bucket GCS.

Seleziona la tua origine dati, quindi seleziona **[!UICONTROL Avanti]**.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione Adobe Experience Platform evidenziata.](/help/assets/setup/add-manage-audiences/select-data-connection-source.png)

#### Seleziona sandbox

Dopo aver selezionato l’origine dati, devi selezionare la sandbox che include i tipi di pubblico da utilizzare in Collaboration. Seleziona la sandbox dall&#39;elenco delle sandbox disponibili, quindi seleziona **[!UICONTROL Successivo]**

![L&#39;area di lavoro Aggiungi tipi di pubblico con una sandbox selezionata.](/help/assets/setup/add-manage-audiences/select-sandbox.png)

#### Criteri di governance e azioni di applicazione {#governance-policy-and-enforcement-actions}

Successivamente, assicurati che le azioni di marketing corrette siano impostate sui dati di origine. È inoltre necessario fornire il consenso per i dati provenienti da Experience Platform da utilizzare per la collaborazione sui dati.

Utilizza le azioni di marketing per controllare quali dati del pubblico inserire in Collaboration da Experience Platform. L’azione di marketing **[!UICONTROL Collaborazione sui dati]** supporta le etichette di utilizzo dei dati C4, C5 e C9. L’azione di marketing **[!UICONTROL Data science]** supporta l’etichetta di utilizzo dati C9.

Ulteriori informazioni sulle etichette di utilizzo dei dati [C4, C5 e C9](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* Quando la casella di controllo è ***enabled***, tutti i dati etichettati in Experience Platform come descritto in precedenza vengono esclusi e **not** vengono portati in Collaboration.
* Se la casella di controllo ***è disabilitata***, i dati originati da Experience Platform non sono soggetti a restrizioni.

Ulteriori informazioni sulle etichette di utilizzo dei dati nella documentazione di Experience Platform:

* [Panoramica delle etichette di utilizzo dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Glossario delle etichette di utilizzo dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/reference){target="_blank"}

Inoltre, seleziona le regole di consenso da applicare ai dati originati in Collaboration.

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
>abstract="I campi di origine sono spazi dei nomi e attributi di identità provenienti dalla tua implementazione di Experience Platform. Puoi mapparli ai campi di destinazione definiti in Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Campi di destinazione"
>abstract="Attualmente, gli indirizzi e-mail con hash sono le uniche chiavi di corrispondenza supportate."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Applica trasformazione"
>abstract="Se si ottengono campi *senza hash*, utilizza questa opzione affinché Collaboration possa applicare l’hashing e trasformare i campi normali in campi con hash."

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

Quindi, seleziona i campi sorgente da mappare ai campi di destinazione in Collaboration.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione di mappare i campi di origine ai campi di destinazione.](/help/assets/setup/add-manage-audiences/add-map-fields.png)

>[!TIP]
>
>Puoi mappare più campi sorgente allo stesso campo di destinazione. Se ad esempio gli indirizzi e-mail sono contenuti in due campi separati di Experience Platform, è possibile mappare ciascuno di essi nel campo di destinazione **[!UICONTROL E-mail con hash]** come due righe separate.

>[!BEGINSHADEBOX]

**[!UICONTROL I campi di Source]** sono spazi dei nomi di identità e attributi di Experience Platform. Queste sono le identità esistenti nella piattaforma da cui stai estraendo i dati. I campi Source vengono mappati sui campi target definiti in Collaboration.

**[!UICONTROL I campi di destinazione]** indicano il riferimento alle identità in Collaboration. Attualmente, gli indirizzi e-mail con hash sono le uniche chiavi di corrispondenza supportate.

Utilizza l&#39;opzione **[!UICONTROL Applica trasformazione]** quando importi *campi senza hash* dall&#39;origine. In questo caso, Collaboration applicherà l’hashing e trasformerà i campi. L’algoritmo di hashing utilizzato da Adobe è SHA256.

>[!ENDSHADEBOX]

Seleziona il campo di origine vuoto accanto al campo di destinazione. Verrà visualizzata la finestra di dialogo **[!UICONTROL Seleziona campo di origine]**. Seleziona tra le opzioni **[!UICONTROL Spazi dei nomi identità]** e **[!UICONTROL Attributi profilo]** per trovare il campo di origine desiderato, quindi seleziona il campo dall&#39;elenco. Puoi anche utilizzare l’opzione di ricerca per trovare il campo desiderato.

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
>Dopo la data di fine nell’intervallo di date, tutti i tipi di pubblico originati da questa connessione dati cesseranno di essere aggiornati. Per rinnovare la connessione, seguire la [guida alla gestione della connessione dati](/help/guide/setup/manage-data-connection.md).

### Seleziona tipi di pubblico {#select-audiences}

Dopo aver selezionato la sorgente del pubblico, scegli tipi di pubblico specifici da includere. Utilizza le opzioni di ricerca e filtro per trovare i tipi di pubblico rilevanti dall’origine dati. Seleziona il pubblico desiderato, quindi seleziona **[!UICONTROL Successivo]**.

![Area di lavoro Aggiungi tipi di pubblico con un elenco dei tipi di pubblico disponibili.](/help/assets/setup/add-manage-audiences/select-audience.png)

### Rivedi

Rivedi tutte le configurazioni e le impostazioni prima di finalizzare l’aggiunta di pubblico. Verifica che tutti i dettagli siano corretti, quindi seleziona **[!UICONTROL Completa]** per completare la creazione della connessione dati.

![Area di lavoro Aggiungi tipi di pubblico con tutte le configurazioni selezionate visualizzate.](/help/assets/setup/add-manage-audiences/review-connection.png)

## Visualizza dashboard dei tipi di pubblico {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Identità mancanti"
>abstract="Il conteggio delle identità sarà disponibile dopo il successivo aggiornamento della connessione dati dopo la pianificazione configurata. L’aggiornamento iniziale si verifica in genere entro 24 ore dalla configurazione della connessione dati. Gli aggiornamenti ricorrenti seguiranno la pianificazione configurata."

Dopo aver determinato l&#39;origine dei tipi di pubblico, nell&#39;area di lavoro **[!UICONTROL Tipi di pubblico personali]** vengono visualizzati tutti i tipi di pubblico attualmente assegnati a Collaboration.

![L&#39;area di lavoro I miei tipi di pubblico visualizza tutti i tipi di pubblico originati.](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

Ogni pubblico contiene una panoramica delle seguenti informazioni:

| Elemento | Descrizione |
|----------|---------|
| **[!UICONTROL Nome]** | Il nome del pubblico. |
| **[!UICONTROL Identità]** | Indica il numero di identità presenti nel pubblico. Tieni presente che se lo stesso profilo ha due o più identità e queste vengono utilizzate come chiavi di corrispondenza nel progetto, il profilo verrà visualizzato due volte nel conteggio. |
| **[!UICONTROL Stato]** | Indica se il pubblico è attivo e può essere utilizzato nei progetti. Uno stato **[!UICONTROL In sospeso]** indica che il pubblico è stato originato di recente e che le identità non sono ancora state popolate. I tipi di pubblico di origine verranno compilati con profili dopo l’aggiornamento iniziale, che in genere si verifica entro 24 ore dalla configurazione della connessione dati. |
| **[!UICONTROL Source]** | Indica da dove è stato originato il pubblico. Nell’attuale versione di Collaboration, Experience Platform è l’unica origine supportata. |
| **[!UICONTROL Connessione dati]** | La connessione dati da cui proviene il pubblico. Puoi selezionare il nome per visualizzare la connessione dati. |
| **[!UICONTROL Accesso alla connessione]** | Definisce se il pubblico è privato o pubblico. I tipi di pubblico sono rilevabili nei rapporti di sovrapposizione e possono essere attivati all’interno di un progetto. |
| **[!UICONTROL Creato]** | Indica quando il pubblico è stato inizialmente originato in Collaboration. |
| **[!UICONTROL Ultimo aggiornamento]** | Indica la data e l’ora dell’ultimo aggiornamento del pubblico in Collaboration. Non si riferisce all’ultimo aggiornamento del pubblico, ma piuttosto all’ultima modifica della configurazione o dei metadati del pubblico. |

Per eseguire azioni rapide su un pubblico, seleziona i puntini di sospensione **...** accanto al nome del pubblico. Sono disponibili le seguenti opzioni:

* **[!UICONTROL Modifica categorie]** ti consente di aggiungere al pubblico tag di categoria diversi. Per ulteriori informazioni, consulta la sezione [categorie](#categories) di seguito.
* **[!UICONTROL Elimina]** eliminerà il pubblico dalla connessione dati.

![Nell&#39;area di lavoro I miei tipi di pubblico è aperta l&#39;area di lavoro con il menu con i puntini di sospensione e sono evidenziate le opzioni Modifica categorie ed Elimina.](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png)

## Visualizzare singoli tipi di pubblico {#view-individual-audiences}

Per visualizzare e aggiornare le informazioni per un singolo pubblico, seleziona il pubblico dall&#39;area di lavoro **[!UICONTROL Tipi di pubblico]**. L’area di lavoro pubblico visualizza informazioni dettagliate sul pubblico selezionato, inclusi dettagli, identità, categorie, accesso alla connessione e impostazioni di visibilità dei metadati.

### Dettagli del pubblico

Per ogni singolo pubblico vengono visualizzate le seguenti informazioni:

| Elemento | Descrizione |
|----------|---------|
| **[!UICONTROL Stato]** | Indica se il pubblico è attivo e può essere utilizzato nei progetti. |
| **[!UICONTROL Source]** | Indica da dove è stato originato il pubblico. Nell’attuale versione di Collaboration, Experience Platform è l’unica origine supportata. |
| **[!UICONTROL Connessione dati]** | La connessione dati da cui proviene il pubblico. |
| **[!UICONTROL Ultimo aggiornamento]** | Indica la data e l’ora dell’ultimo aggiornamento del pubblico in Collaboration. Non si riferisce all’ultimo aggiornamento del pubblico, ma piuttosto all’ultima modifica della configurazione o dei metadati del pubblico |
| **[!UICONTROL Ultimo aggiornamento eseguito da]** | Indica l’ultimo utente che ha aggiornato il pubblico. |
| **[!UICONTROL Creato]** | Indica quando il pubblico è stato inizialmente originato in Collaboration. |
| **[!UICONTROL Creato da]** | Indica l’utente che ha originato il pubblico in Collaboration. |

![Area di lavoro di un singolo pubblico.](/help/assets/setup/add-manage-audiences/audience-details.png)

#### Identità {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identità"
>abstract="Una vista di raggruppamento delle identità che compongono il pubblico, separate da una chiave di corrispondenza."

La sezione **[!UICONTROL Identità]** indica il numero di identità presenti nel pubblico. La sezione contiene anche una suddivisione delle identità per chiave di corrispondenza per aiutarti a comprendere la composizione del pubblico.

![Sezione Identità dell&#39;area di lavoro di un singolo pubblico.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

Passando il puntatore del mouse sulle singole sezioni del raggruppamento della chiave di corrispondenza si ottiene un conteggio accurato delle identità per la chiave pertinente.

![Sezione Identità dell&#39;area di lavoro di un singolo pubblico con raggruppamento di chiave di corrispondenza visualizzato.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

#### Categorie {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Categorie"
>abstract="Assegna tag ai tipi di pubblico per semplificarne l’organizzazione, il filtraggio e il recupero. Puoi assegnare a un pubblico i tag di più categorie, e utilizzare quindi tali categorie per filtrare i tipi di pubblico desiderati in altre aree del prodotto."

Per facilitare l’organizzazione, il filtraggio e il recupero del pubblico, puoi assegnare tag ai tipi di pubblico. Puoi assegnare tag a un pubblico con più categorie, quindi utilizzare questi tag per filtrare i tipi di pubblico desiderati nell&#39;area di prodotto [discovery](/help/guide/collaborate/discover.md) durante l&#39;esecuzione di report di sovrapposizione pubblico.

Per aggiungere categorie, selezionare l&#39;opzione **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Categorie]**.

![Sezione Categorie dell&#39;area di lavoro di un singolo pubblico.](/help/assets/setup/add-manage-audiences/audience-details-categories.png)

Verrà visualizzata la finestra di dialogo **[!UICONTROL Categorie]**, che consente di selezionare le categorie da aggiungere al pubblico. Per selezionare una singola categoria, selezionare la casella di controllo accanto al nome della categoria.

![Viene visualizzata la finestra di dialogo Categorie con le categorie disponibili.](/help/assets/setup/add-manage-audiences/audience-details-categories-select.png)

#### Accesso connessione {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Accesso connessione"
>abstract="<p>I tipi di pubblico possono essere di tre tipi: pubblico, privato e personalizzato.</p><p> La loro disponibilità per l’utilizzo in progetti con collaboratori varia in base all’impostazione di accesso alla connessione.</p>"

La disponibilità di un pubblico da utilizzare nei progetti con collaboratori varia in base all’impostazione di accesso alla connessione. Nella sezione **[!UICONTROL Accesso alla connessione]**, puoi selezionare se il pubblico deve essere privato, pubblico o disponibile solo per connessioni specifiche. Il pubblico pubblico è utilizzabile e individuabile nelle connessioni.

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
>Indipendentemente dallo stato di accesso (pubblico, privato o personalizzato), la popolazione di qualsiasi pubblico contribuisce alla popolazione **[!UICONTROL Tutti i tipi di pubblico]** nella sezione **[!UICONTROL Confronta tipi di pubblico]** all&#39;interno di un progetto.

La disponibilità del pubblico da utilizzare nei progetti con collaboratori varia in base all’impostazione di accesso alla connessione.

#### Visibilità dei metadati {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Visibilità dei metadati"
>abstract="<p>Indica quali metadati del pubblico devono essere visibili ad altri collaboratori prima che si connettano con te o nelle viste dei progetti.</p> <p> **Conteggio identità** controlla se il collaboratore può visualizzare i conteggi delle identità per il tuo pubblico nei rapporti di sovrapposizione nella scheda Individuazione.</p><p> **Sovrapposizione pubblico (% )** controlla se i collaboratori possono individuare le percentuali di sovrapposizione tra il loro pubblico e il tuo.</p><p> **[!UICONTROL Indice del pubblico]** controlla se i collaboratori possono vedere l’indice del pubblico all’interno di un progetto. Questa funzionalità è disponibile solo se sono presenti almeno tre tipi di pubblico attivi.</p> <br> Affinché le impostazioni di visibilità dei metadati diventino effettive, il pubblico deve essere impostato su pubblico o personalizzato."

>[!NOTE]
>
>Se tutti i tipi di pubblico del tuo collaboratore sono impostati su privato, la sezione **[!UICONTROL Tipi di pubblico rilevanti]** di un progetto nell&#39;area di lavoro **[!UICONTROL Discover]** sarà vuota. Per ulteriori informazioni, leggere la guida di [individuazione](/help/guide/collaborate/discover.md#relevant-audiences).

La visibilità dei metadati indica la visibilità dei metadati di un pubblico per altri collaboratori prima che si connettano con te o all’interno di diverse visualizzazioni del progetto. Per aggiornare la visibilità dei metadati del pubblico, seleziona l&#39;opzione **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Visibilità metadati]**.

![Sezione visibilità metadati dell&#39;area di lavoro di un singolo pubblico.](/help/assets/setup/add-manage-audiences/audience-details-metadata-visibility.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Visibilità metadati]**, che consente di configurare le impostazioni di visibilità per il pubblico. È possibile configurare due impostazioni di visibilità dei metadati per ogni pubblico:

**[!UICONTROL Mostra conteggio identità]**: questa impostazione controlla se il tuo collaboratore può visualizzare i conteggi delle identità per i tuoi tipi di pubblico quando [visualizzi i report di sovrapposizione nella scheda di individuazione](/help/guide/collaborate/discover.md#discover-overlaps) all&#39;interno di un progetto.

**[!UICONTROL Mostra sovrapposizione pubblico %]**: questa impostazione controlla se i collaboratori sono in grado di [individuare percentuali di sovrapposizione](/help/guide/collaborate/discover.md#compare-audiences) tra i propri tipi di pubblico e i tipi di pubblico.

**[!UICONTROL Indice pubblico]**: se è impostato su true, i collaboratori possono visualizzare il [indice pubblico](/help/guide/collaborate/discover.md#audience-index-score) all&#39;interno di un progetto. Questa funzionalità è disponibile solo se sono presenti almeno tre tipi di pubblico attivi.

>[!NOTE]
>
>Affinché le impostazioni di visibilità dei metadati diventino effettive, il pubblico deve essere impostato su pubblico o personalizzato.

![Viene visualizzata la finestra di dialogo Visibilità metadati con le opzioni disponibili.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

## Modificare più tipi di pubblico {#edit-audiences}

Puoi modificare più tipi di pubblico alla volta dal dashboard Pubblico. A questo scopo, seleziona i tipi di pubblico da modificare selezionando le caselle accanto ai relativi nomi. Dopo aver selezionato i tipi di pubblico, puoi eseguire azioni utilizzando le opzioni disponibili nel menu Modifica.

![Area di lavoro I miei tipi di pubblico con due tipi di pubblico selezionati e il menu Modifica evidenziato.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit.png)

### Visibilità della modifica in blocco dei metadati {#bulk-edit-metadata-visibility}

Con i tipi di pubblico selezionati nel dashboard del pubblico, seleziona **[!UICONTROL Modifica visibilità metadati]** dal menu Modifica.

![Area di lavoro I miei tipi di pubblico con l&#39;opzione Modifica visibilità metadati evidenziata.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-metadata.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Visibilità metadati]**, che consente di configurare le impostazioni di visibilità per i tipi di pubblico selezionati. Per impostazione predefinita, non viene selezionata alcuna opzione. Scegli le opzioni da applicare a tutti i tipi di pubblico selezionati, quindi seleziona **[!UICONTROL Salva]**.

![Viene visualizzata la finestra di dialogo Visibilità metadati con le opzioni disponibili.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

### Accesso alla connessione per modifica in blocco {#bulk-edit-connection-access}

Con i tipi di pubblico selezionati nel dashboard del pubblico, seleziona **[!UICONTROL Modifica accesso alla connessione]** dal menu Modifica.

![L&#39;area di lavoro I miei tipi di pubblico con l&#39;opzione Modifica accesso alla connessione evidenziata.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-connection-access.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Accesso alla connessione]**, che consente di configurare le impostazioni di accesso per i tipi di pubblico selezionati. Per impostazione predefinita, verrà selezionata l&#39;opzione **[!UICONTROL Pubblico privato]**. Scegli le opzioni da applicare a tutti i tipi di pubblico selezionati, quindi seleziona **[!UICONTROL Salva]**.

![Viene visualizzata la finestra di dialogo Accesso alla connessione con le opzioni disponibili.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

### Modifica in blocco di nomi e descrizioni del pubblico {#bulk-edit-audience-names-descriptions}

Con i tipi di pubblico selezionati nel dashboard del pubblico, seleziona **[!UICONTROL Modifica nome e descrizione]** dal menu Modifica.

![Area di lavoro I miei tipi di pubblico con l&#39;opzione Modifica nome e descrizione evidenziata.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Nome e descrizione]**, che consente di configurare il nome e la descrizione per ogni pubblico selezionato. Per impostazione predefinita, i nomi e le descrizioni correnti vengono visualizzati per ogni pubblico. Apporta le modifiche e seleziona **[!UICONTROL Salva]**.

![Viene visualizzata la finestra di dialogo Nome e descrizione con le opzioni disponibili.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description-dialog.png)

### Categorie di modifica in blocco {#bulk-edit-categories}

Con i tipi di pubblico selezionati nel dashboard del pubblico, seleziona **[!UICONTROL Modifica categorie]** dal menu Modifica.

![Area di lavoro I miei tipi di pubblico con l&#39;opzione Modifica categorie evidenziata.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Categorie]**, che consente di configurare le categorie per ogni pubblico selezionato. Per impostazione predefinita, non viene selezionata alcuna categoria. Per selezionare una categoria, selezionare innanzitutto la categoria principale, quindi selezionare le sottocategorie che si desidera includere. Apporta le modifiche e seleziona **[!UICONTROL Salva]**.

![Viene visualizzata la finestra di dialogo Categorie con le opzioni disponibili.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories-dialog.png)

## Passaggi successivi

Dopo aver individuato i tipi di pubblico, è ora di scoprire gli editori con cui [connettersi](/help/guide/connect/establishing-connections.md) per collaborare ai progetti.
