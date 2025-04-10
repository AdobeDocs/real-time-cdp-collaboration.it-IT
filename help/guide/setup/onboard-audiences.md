---
title: Importare e gestire i tipi di pubblico
description: Scopri come importare e gestire i tipi di pubblico in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: ff22dde9730fab89481338753b1dc4a0adf1d57e
workflow-type: tm+mt
source-wordcount: '2642'
ht-degree: 2%

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
* [Visualizza dashboard tipi di pubblico](#view-audiences-dashboard)
* [Visualizzare singoli tipi di pubblico](#view-individual-audiences)

>[!ENDSHADEBOX]

## Importare tipi di pubblico in Real-Time CDP Collaboration {#import-audiences}

>[!IMPORTANT]
>
>Per importare dei tipi di pubblico, l’utente deve essere assegnato a un ruolo contenente due autorizzazioni di Gestione profilo: Visualizza profili e Visualizza segmenti. Per informazioni sull&#39;assegnazione delle autorizzazioni necessarie, consultare la [guida all&#39;importazione del pubblico](../permissions/overview.md#audience-importation).

Prima di poter condividere i tipi di pubblico con i collaboratori ed eseguire calcoli di sovrapposizione, è necessario importarli in Real-Time CDP Collaboration. Per importare dei tipi di pubblico, segui i passaggi del flusso di lavoro descritti nella sezione seguente.

![I miei tipi di pubblico vengono visualizzati prima dell&#39;aggiunta di qualsiasi tipo di pubblico all&#39;organizzazione.](/help/assets/setup/add-manage-audiences/org-without-audiences-added.png)

Dalla scheda **[!UICONTROL Tipi di pubblico]**, seleziona il simbolo Più **+** e **Pubblico**.

### Seleziona connessione dati {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Azioni marketing"
>abstract="<p>Utilizza le azioni di marketing per controllare quali dati del pubblico importare in Real-Time CDP Collaboration da Experience Platform. L&#39;azione di marketing <strong>Data Collaboration</strong> supporta le etichette di utilizzo dei dati C4, C5 e C9. L&#39;azione di marketing <strong>Data Science</strong> supporta l&#39;etichetta di utilizzo dati C9.</p> <p> <ul><li> Con la casella di controllo <em>enabled</em>, tutti i dati contrassegnati con le etichette richiamate in precedenza in Experience Platform vengono esclusi e vengono <strong>not</strong> inseriti in Real-Time CDP Collaboration.</li><li> Se la casella di controllo <em>è disabilitata</em>, i dati provenienti da Experience Platform che possono essere importati in Real-Time CDP Collaboration non sono soggetti a restrizioni.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=it" text="Panoramica sulle etichette di utilizzo dei dati"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html" text="Glossario delle etichette di utilizzo dei dati"

>[!IMPORTANT]
>
>Dopo aver effettuato la connessione alla prima connessione dati e aver importato il primo pubblico, puoi scegliere di importare più tipi di pubblico da questa connessione dati esistente. In questo caso, il flusso di lavoro ti porterà direttamente al passaggio [seleziona pubblico](#select-audience), poiché tutte le informazioni sui prerequisiti degli altri passaggi verranno importate dalla connessione esistente.

Una connessione dati è l’origine dei dati da cui si importano i tipi di pubblico in Real-Time CDP Collaboration. Per la prima versione di Real-Time CDP Collaboration, l’unica connessione dati supportata è Adobe Experience Platform.

Tutte le impostazioni, ad esempio la mappatura o la pianificazione delle identità, configurate per la connessione dati vengono applicate a tutti i tipi di pubblico importati da questa connessione dati.

>[!TIP]
>
>Esiste un flusso di lavoro separato in cui è sempre possibile visualizzare e modificare tutte le connessioni dati aggiunte in questo passaggio. Ulteriori informazioni sulla [gestione delle connessioni dati](/help/guide/setup/manage-data-connection.md).

![Seleziona la schermata dell&#39;origine del pubblico con le opzioni per AEP RTCDP, CSV File, Amazon S3 e Snowflake.](/help/assets/setup/add-manage-audiences/Step-Select-Audience-Source.png)

#### Seleziona origine dati

In questo passaggio, scegli l’origine dei dati sul pubblico. Le fonti disponibili includono:

* **Adobe Experience Platform**: seleziona questa opzione per inserire i tipi di pubblico da Adobe Experience Platform Real-Time CDP.
* **File CSV** (versione futura): carica un file CSV contenente i dati del pubblico per acquisire dati in modo rapido e semplice.
* **Amazon Web Services** (versione futura): connettiti all&#39;archiviazione Amazon S3 per importare i dati del pubblico direttamente dai bucket S3.
* **Snowflake** (versione futura): utilizza il data warehouse di Snowflake per estrarre facilmente i dati sul pubblico.

#### Seleziona sandbox

Dopo aver selezionato **Adobe Experience Platform** come origine dati, è necessario selezionare la sandbox che include i tipi di pubblico che verranno importati.

![Seleziona la sandbox per importare i tipi di pubblico](/help/assets/setup/add-manage-audiences/import-audiences-select-sandbox.png)

Seleziona **[!UICONTROL Avanti]** dopo aver selezionato la sandbox desiderata.

#### Criteri di governance e azioni di applicazione {#governance-policy-and-enforcement-actions}

Successivamente, assicurati che le azioni di marketing corrette siano impostate sui dati importati. È inoltre necessario fornire il consenso per i dati importati da Real-Time CDP da utilizzare per la collaborazione sui dati.

Utilizza le azioni di marketing per controllare quali dati del pubblico importare in Real-Time CDP Collaboration da Experience Platform. L&#39;azione di marketing **Data Collaboration** supporta le etichette di utilizzo dei dati C4, C5 e C9. L&#39;azione di marketing **Data Science** supporta l&#39;etichetta di utilizzo dati C9.

Ulteriori informazioni sulle etichette di utilizzo dei dati [C4, C5 e C9](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* Con la casella di controllo *enabled*, tutti i dati contrassegnati con le etichette richiamate in precedenza in Experience Platform vengono esclusi e vengono *not* inseriti in Real-Time CDP Collaboration.
* Se la casella di controllo *è disabilitata*, i dati provenienti da Experience Platform che possono essere importati in Real-Time CDP Collaboration non sono soggetti a restrizioni.

Ulteriori informazioni sulle etichette di utilizzo dei dati nella documentazione di Experience Platform:

* [Panoramica delle etichette di utilizzo dei dati](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Glossario delle etichette di utilizzo dei dati](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference){target="_blank"}

![Azioni di marketing richieste per la collaborazione sui dati.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

### Fornisci dettagli

Quindi, fornisci un nome e una descrizione per riconoscere questa connessione dati in futuro.

<!--

>[!IMPORTANT]
>
>Note a difference in terminology where the sandbox selected from Real-Time CDP is considered a dataset in the UI in Real-Time CDP Collaboration.

-->

### Mappa campi {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Campi di origine"
>abstract="I campi Source sono spazi dei nomi e attributi di identità provenienti dall’implementazione esistente di Real-Time CDP. Puoi mapparli ai campi di destinazione definiti in Real-Time CDP Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Campi di destinazione"
>abstract="I campi di destinazione corrispondono alle chiavi di corrispondenza selezionate al momento dell’onboarding della società. Attualmente, le e-mail con hash sono le uniche chiavi di corrispondenza supportate."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Applicar trasformazione"
>abstract="Durante l&#39;importazione di *campi senza hash* dall&#39;origine, utilizzare questa opzione per fare in modo che Real-Time CDP Collaboration applichi l&#39;hashing e trasformi i campi normali in campi con hashing."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_identity_namespaces"
>title="Spazio dei nomi delle identità"
>abstract="Seleziona uno spazio dei nomi delle identità dagli spazi dei nomi di identità standard e personalizzati disponibili nella tua organizzazione Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#standard" text="Spazi dei nomi standard e di identità in Experience Platform"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_profile_attributes"
>title="Attributi del profilo"
>abstract="Seleziona gli attributi dallo schema di unione per la classe Profilo in Experience Platform. Questa vista mostra gli attributi presenti nello schema di unione e appartenenti alla classe Profilo individuale XDM."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html" text="Schema di unione in Experience Platform"

![Schermata Mappa campi con i campi di origine mappati ai campi di destinazione.](/help/assets/setup/add-manage-audiences/Step-Map-Fields.png)

Nel passaggio Mappa campi puoi selezionare il modo in cui i campi di identità per i profili importati dalla connessione dati devono essere mappati alle chiavi di corrispondenza selezionate nell’organizzazione.

>[!TIP]
>
>Puoi mappare più campi sorgente allo stesso campo di destinazione. Se ad esempio gli indirizzi e-mail sono contenuti in due campi distinti di Experience Platform, è possibile mappare entrambi al campo di destinazione **[!UICONTROL E-mail con hash]** come due righe separate.

>[!BEGINSHADEBOX]

**[!UICONTROL I campi di Source]** indicano il riferimento alle identità nell&#39;origine da cui si importano i dati.

**[!UICONTROL I campi di destinazione]** indicano il riferimento alle identità in Real-Time CDP Collaboration. I valori che puoi selezionare qui corrispondono alle chiavi di corrispondenza impostate nel flusso di lavoro di onboarding della società.

Utilizza l&#39;opzione **[!UICONTROL Applica trasformazione]** quando importi *campi senza hash* dall&#39;origine. In questo caso, Real-Time CDP Collaboration applicherà l’hashing e trasformerà i campi. L’algoritmo di hashing utilizzato da Adobe è SHA256.

>[!ENDSHADEBOX]

Aggiungi tutte le coppie di mappatura necessarie e seleziona **[!UICONTROL Avanti]** per procedere al passaggio successivo.

<!--

In this step, you can also add any identity crosswalks that you would like to use.

Identity crosswalks will be supported after the beta release.

#### Add identity crosswalk

Use identity crosswalks to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. 

TODO add GIF Identity crosswalks screen showing a list of available identity crosswalks with details.

Select **[!UICONTROL Add identity crosswalk]** to see a screen where you can choose from various identity crosswalks that you have previously [imported into Real-Time CDP Collaboration](/help/guide/setup/identity-crosswalk.md#import-crosswalk). Each entry includes details such as the table name, type, description, and creation date.

After selecting the desired crosswalk, use a source field join key to map to the crosswalk table join key. 

>[!NOTE]
>
>After selecting an identity crosswalk, the **[!UICONTROL Add identity crosswalk]** control is greyed out. 

For further reading about identity crosswalks, refer to the [glossary](/help/guide/glossary.md).

-->


<!-- will uncomment this part when Manage use cases part becomes available

### Manage use cases {#manage-use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_usecases"
>title="Use cases for identities"
>abstract="This control is disabled in the initial release of Real-Time CDP Collaboration"

![Manage use cases screen.](/help/assets/setup/add-manage-audiences/Step-manage-use-cases.png)

For every identity selected in the mapping step, select the use cases that you can use the identity for. Available use cases are: 

* Discover
* Share
* Activate
* Measure

Note that this control is disabled in the initial release of Real-Time CDP Collaboration.

After selecting the desired use cases for each identity, proceed to the next step. 

-->

### Pianificazione {#schedule}

Pianifica quando iniziare e finire di popolare e aggiornare i tipi di pubblico. L’iscrizione al pubblico verrà aggiornata in base a questa pianificazione.

![Schermata di pianificazione che mostra le date di inizio e fine per il popolamento dei tipi di pubblico.](/help/assets/setup/add-manage-audiences/Step-Schedule.png)

Seleziona la frequenza di aggiornamento per i tipi di pubblico. Le opzioni disponibili sono tra le frequenze di aggiornamento di uno e sei giorni.

>[!IMPORTANT]
>
>Regolando la frequenza degli aggiornamenti del pubblico sarà possibile gestire l&#39;attività di credito di [Gestione dell&#39;audience](/help/guide/setup/my-activity.md#types-of-activities), calcolata per ogni aggiornamento dell&#39;iscrizione al pubblico. L’impatto di questo potrebbe essere la disponibilità di dati meno recenti per i rapporti di individuazione del pubblico e la condivisione e l’attivazione del pubblico.

![Schermata di pianificazione che mostra intervalli di frequenza diversi per l&#39;aggiornamento dell&#39;iscrizione al pubblico.](/help/assets/setup/add-manage-audiences/Step-Schedule-Set-Frequency.png)

>[!IMPORTANT]
>
>Dopo la data di fine nell’intervallo di date, tutti i tipi di pubblico importati da questa connessione dati cesseranno di essere aggiornati. Per rinnovare la connessione, passare a [Gestisci connessione dati](/help/guide/setup/manage-data-connection.md) e impostare una nuova data di fine.

### Seleziona tipi di pubblico {#select-audience}

Dopo aver selezionato la sorgente del pubblico, scegli tipi di pubblico specifici da includere. Utilizza le opzioni di ricerca e filtro nella pagina per trovare i tipi di pubblico rilevanti dall’origine dati selezionata.

![Seleziona la schermata del pubblico che mostra un elenco dei tipi di pubblico disponibili con caselle di controllo per selezionarli.](/help/assets/setup/add-manage-audiences/Step-Select-Audience.png)

### Rivisione

Rivedi tutte le configurazioni e le impostazioni prima di finalizzare l’aggiunta di pubblico. Verifica che tutti i dettagli siano corretti e seleziona **[!UICONTROL Completa]** per finalizzare il processo.

## Visualizza dashboard tipi di pubblico {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Identità mancanti"
>abstract="Il conteggio delle identità visualizza un `-` per circa le prime 24 ore dopo l&#39;importazione di un pubblico in Real-Time CDP Collaboration. Dopo questo intervallo di tempo, il conteggio delle identità si aggiornerà con il numero di profili presenti nel pubblico."

Dopo aver importato i tipi di pubblico in Real-Time CDP Collaboration, puoi ottenere informazioni su di essi in una vista dashboard. La visualizzazione predefinita nella pagina **[!UICONTROL Tipi di pubblico]** mostra tutti i tipi di pubblico attualmente importati dall&#39;organizzazione in Real-Time CDP Collaboration.

![Pagina panoramica tipi di pubblico che mostra tutti i tipi di pubblico importati da un inserzionista](/help/assets/setup/add-manage-audiences/audiences-overview.png)

Puoi visualizzare le seguenti informazioni rilevanti su ciascun pubblico:

| Elemento | Descrizione |
|----------|---------|
| **[!UICONTROL Identità]** | Indica il numero di identità presenti nel pubblico. Tieni presente che se lo stesso profilo ha due o più identità e queste vengono utilizzate come chiavi di corrispondenza nel progetto, il profilo verrà visualizzato due volte nel conteggio. |
| **[!UICONTROL Stato]** | Indica se il pubblico è attivo e può essere utilizzato nei progetti. Lo stato In sospeso indica che il pubblico è stato importato di recente e che i membri del pubblico devono ancora essere popolati. I tipi di pubblico importati di solito si popolano con profili entro 24 ore. |
| **[!UICONTROL Source]** | Indica l’origine da cui è stato importato il pubblico. Nell’attuale versione di Real-Time CDP Collaboration, Adobe Experience Platform è l’unica origine supportata. |
| **[!UICONTROL Connessione dati]** | Ulteriori informazioni drill-down su da dove è stato importato questo pubblico. Ad esempio, quando importi un pubblico dall’origine di Experience Platform, le singole sandbox a cui la tua organizzazione ha accesso sono considerate connessioni dati. |
| **[!UICONTROL Accesso alla connessione]** | Definisce se questo pubblico è privato o pubblico. I tipi di pubblico sono rilevabili nei rapporti di sovrapposizione e possono essere condivisi con i collaboratori. |
| **[!UICONTROL Creato]** | Indica quando questo pubblico è stato importato in Real-Time CDP Collaboration. |
| **[!UICONTROL Ultimo aggiornamento]** | Indica l’ultima data e ora in cui è stato aggiornato un qualsiasi aspetto di questo pubblico. |

Selezionare **[!UICONTROL Gestisci connessioni dati]** per visualizzare e modificare tutte le connessioni dati configurate.
Seleziona i puntini di sospensione e **[!UICONTROL Elimina]** per rimuovere il pubblico.
Seleziona i puntini di sospensione e **[!UICONTROL Modifica categorie]** per aggiungere al pubblico tag di categoria diversi. Ulteriori informazioni sono disponibili nella sezione [categorie](/#categories) seguente.
Seleziona il nome del pubblico per esaminare o modificare i singoli tipi di pubblico.

## Visualizzare singoli tipi di pubblico {#view-individual-audiences}

La visualizzazione del pubblico mostra ulteriori informazioni sul pubblico.

![Visualizza ed esamina i singoli tipi di pubblico.](/help/assets/setup/add-manage-audiences/view-inspect-audience.png)

Le metriche che puoi visualizzare in questa schermata sono descritte di seguito:

| Elemento | Descrizione |
|----------|---------|
| **[!UICONTROL Stato]** | Indica se il pubblico è attivo e può essere utilizzato nei progetti. |
| **[!UICONTROL Source]** | Indica l’origine da cui è stato importato il pubblico. Nell’attuale versione di Real-Time CDP Collaboration, Adobe Experience Platform è l’unica origine supportata. |
| **[!UICONTROL Connessione dati]** | Ulteriori informazioni drill-down su da dove è stato importato questo pubblico. Ad esempio, quando importi un pubblico dall’origine di Experience Platform, le singole sandbox a cui la tua organizzazione ha accesso sono considerate connessioni dati. |
| **[!UICONTROL Ultimo aggiornamento]** | Indica l’ultima data e ora in cui è stato aggiornato un qualsiasi aspetto di questo pubblico. |
| **[!UICONTROL Ultimo aggiornamento eseguito da]** | Indica l’ultimo utente che ha aggiornato questo pubblico. |
| **[!UICONTROL Creato]** | Indica quando questo pubblico è stato importato in Real-Time CDP Collaboration. |
| **[!UICONTROL Creato da]** | Indica l’utente che ha importato il pubblico in Real-Time CDP Collaboration. |


Puoi utilizzare altri due controlli nella pagina per modificare o rimuovere i tipi di pubblico:

* **[!UICONTROL Elimina]**: rimuovi il pubblico dal tuo inventario
* **[!UICONTROL Modifica]**: modifica i metadati del pubblico, ad esempio il nome o la descrizione.

![Visualizza ed esamina i singoli tipi di pubblico.](/help/assets/setup/add-manage-audiences/audiences-edit-delete-controls.png)

Ulteriori informazioni sul pubblico sono disponibili e parzialmente modificabili nei widget di seguito:

![Visualizza ed esamina i singoli tipi di pubblico.](/help/assets/setup/add-manage-audiences/audiences-further-info-boxes.png)

* [Identità](#identities)
* [Categorie](#categories)
* [Accesso connessione](#connection-access)
* [Visibilità dei metadati](#metadata-visibility)

### Identità {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identità"
>abstract="Ottieni una visualizzazione dettagliata delle identità che compongono il pubblico, nonché un conteggio totale di profili con le rispettive identità."

Questa sezione indica il numero di profili presenti nel pubblico con una qualsiasi delle identità specificate al momento dell’importazione dei tipi di pubblico. La sezione contiene anche un raggruppamento delle identità in modo da poter individuare le identità che compongono il maggior numero possibile di persone appartenenti al pubblico.

### Categorie {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Categorie"
>abstract="Assegna tag ai tipi di pubblico per semplificarne l’organizzazione, il filtraggio e il recupero. Puoi assegnare a un pubblico più categorie di tag, che potrai utilizzare per filtrare i tipi di pubblico desiderati in altre aree del prodotto."

Per facilitare l’organizzazione, il filtraggio e il recupero del pubblico, puoi assegnare tag ai tipi di pubblico. Puoi assegnare tag a un pubblico con più categorie, quindi utilizzare questi tag per filtrare i tipi di pubblico desiderati nell&#39;area di prodotto [discovery](/help/guide/collaborate/discover.md) durante l&#39;esecuzione di report di sovrapposizione pubblico.

### Accesso connessione {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Accesso connessione"
>abstract="<p>Il pubblico può essere di tre tipi: pubblico, privato e personalizzato.</p><p> La loro disponibilità per l’utilizzo in progetti con collaboratori varia in base all’impostazione di accesso alla connessione. È sempre possibile cambiare l’accesso alla connessione da privato a pubblico, ma non è possibile ripristinare tale impostazione una volta che un pubblico viene condiviso con i collaboratori.</p>"

Seleziona se il pubblico deve essere privato per te o utilizzabile e individuabile nelle connessioni. Le tre opzioni disponibili sono:

* **[!UICONTROL Pubblico pubblico]**. Questi tipi di pubblico sono disponibili per l’utilizzo in rapporti di sovrapposizione e per la condivisione e l’attivazione in connessioni con qualsiasi collaboratore.
* **[!UICONTROL Pubblico privato]**. Questi tipi di pubblico sono *non* disponibili per l&#39;utilizzo in report di sovrapposizione e per la condivisione e l&#39;attivazione in connessioni con collaboratori. Anche se i collaboratori non possono visualizzarlo o utilizzarlo, la popolazione di questo pubblico contribuisce comunque alla popolazione totale nella visualizzazione **[!UICONTROL Tutti i tipi di pubblico]** nella sezione [individuazione e sovrapposizioni](/help/guide/collaborate/discover.md#compare-audiences). Modifica l’impostazione su public (pubblico) o custom (personalizzato) per utilizzare i tipi di pubblico nelle connessioni con i collaboratori.
* **[!UICONTROL Pubblico personalizzato]**. Questi tipi di pubblico sono disponibili per l’utilizzo in rapporti di sovrapposizione e per la condivisione e l’attivazione solo in connessioni specifiche. Anche se non disponibile per tutti i collaboratori per la visualizzazione o l&#39;utilizzo, la popolazione di questo pubblico contribuisce comunque alla popolazione totale nella visualizzazione **[!UICONTROL Tutti i tipi di pubblico]** nella sezione [individuazione e sovrapposizioni](/help/guide/collaborate/discover.md).

>[!IMPORTANT]
>
>Indipendentemente dallo stato di accesso (pubblico, privato o personalizzato), la popolazione di qualsiasi pubblico contribuisce alla popolazione **[!UICONTROL Tutti i tipi di pubblico]** nella visualizzazione analisi di sovrapposizione individuazione pubblico. <br> ![Il pubblico **Tutti i tipi di pubblico** generato dal sistema nell&#39;analisi di sovrapposizione di Individuazione pubblico include i tipi di pubblico con tutti gli stati di accesso alla connessione (pubblico, privato, personalizzato).](/help/assets/setup/add-manage-audiences/all-audiences-view.png "Il pubblico generato dal sistema **Tutti i tipi di pubblico** nell&#39;analisi di sovrapposizione **Individuazione pubblico** include i tipi di pubblico con tutti gli stati di accesso alla connessione (pubblico, privato, personalizzato)."){width="100" zoomable="yes"}

La disponibilità del pubblico da utilizzare nei progetti con collaboratori varia in base all’impostazione di accesso alla connessione. È sempre possibile cambiare l’accesso alla connessione da privato a pubblico, ma non è possibile ripristinare tale impostazione una volta che un pubblico viene condiviso con i collaboratori.

### Visibilità dei metadati {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Visibilità dei metadati"
>abstract="<p>Indica quale delle informazioni sui metadati del pubblico è visibile ad altre organizzazioni prima che si connettano all’organizzazione. </p> <p> **Il conteggio delle identità** controlla se il partner può visualizzare i conteggi delle identità per i tipi di pubblico quando visualizza i report di sovrapposizione nella scheda di individuazione. **La sovrapposizione del pubblico %** controlla se i collaboratori sono in grado di individuare percentuali di sovrapposizione tra il proprio pubblico e quello dell&#39;utente."

>[!NOTE]
>
>Se il tuo collaboratore ha tutti i tipi di pubblico impostati su privato, la visualizzazione **[!UICONTROL Tipi di pubblico rilevanti]** in Informazioni sul pubblico sarà vuota. [Ulteriori informazioni](/help/guide/collaborate/discover.md#relevant-audiences).

Indica quale delle informazioni sui metadati del pubblico è visibile ad altre organizzazioni prima che si connettano all’organizzazione o all’interno di diverse visualizzazioni del progetto.

**[!UICONTROL Mostra conteggio identità]**: questa impostazione controlla se il partner può visualizzare i conteggi delle identità per i tipi di pubblico quando [visualizza i report di sovrapposizione nella scheda di individuazione](/help/guide/collaborate/discover.md#discover-overlaps).

![Immagini affiancate con l&#39;opzione Mostra conteggio identità deselezionata e selezionata.](/help/assets/setup/add-manage-audiences/show-identity-count.png)

**[!UICONTROL Mostra sovrapposizione pubblico %]**: se è impostato su true, i collaboratori sono in grado di [individuare percentuali di sovrapposizione](/help/guide/collaborate/discover.md#compare-audiences) tra i propri tipi di pubblico e il pubblico a cui si appartiene. Ad esempio, nella registrazione seguente, il pubblico `agora-advertiser-aud3` ha questa configurazione impostata su true e un collaboratore può visualizzare le percentuali di sovrapposizione con tale pubblico. Il pubblico `agora-advertiser-aud1` ha questa impostazione impostata su false, pertanto il collaboratore non può visualizzare le percentuali di sovrapposizione.

![Percentuale di sovrapposizione del pubblico per due tipi di pubblico diversi.](/help/assets/setup/add-manage-audiences/audience-overlap-percentage.gif)

## Passaggi successivi

Dopo aver importato i tipi di pubblico, utilizza la sezione [Connetti](/help/guide/connect/establishing-connections.md) per individuare gli editori con cui connettersi e iniziare a collaborare ai progetti.
