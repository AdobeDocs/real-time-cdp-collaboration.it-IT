---
title: Carica file CSV per Audience Sourcing
description: Scopri come caricare il file CSV come origine dati self-service per acquisire i dati sul pubblico in Real-Time CDP Collaboration.
source-git-commit: 96d3f87cedcfde73ce01c2b53c0b2ce4365fd277
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 0%

---

# Carica file CSV per Audience sourcing

Questa guida descrive i passaggi necessari per caricare un file CSV nell’interfaccia utente di Adobe Real-Time CDP Collaboration per estrarre i dati sul pubblico da utilizzare nei progetti di collaborazione.

## Panoramica {#overview}

Il caricamento di file CSV è uno dei metodi per generare i dati del pubblico primario per i progetti di collaborazione. Alternativa a [connettere il bucket AWS S3](./configure-aws-s3-audience-sourcing.md) o [connettere il pubblico da Experience Platform](./onboard-audiences.md).

Segui questo flusso di lavoro per caricare un file CSV contenente i dati sul pubblico e gestirlo in Collaboration. Puoi mappare i campi di identità per l’analisi di attivazione e sovrapposizione. Una volta caricato ed elaborato il file, il pubblico di origine diventa disponibile nell&#39;area di lavoro **[!UICONTROL I miei tipi di pubblico]**, dove puoi esaminare, attivare e gestire per i tuoi progetti di collaborazione.

>[!IMPORTANT]
>
>* I tipi di pubblico originati dal caricamento CSV sono disponibili per **7 giorni**. Dopo questo periodo, il pubblico scade e deve essere ricaricato per essere utilizzato nei progetti di collaborazione.
>
>* Al momento puoi caricare un file CSV per sessione. Per aggiungere altri tipi di pubblico, completa di nuovo il flusso di lavoro di caricamento per ogni file da sorgente.

## Prerequisiti {#prerequisites}

Prima di poter caricare file CSV per l’audience sourcing, assicurati di disporre di:

* Onboarding dell’account completato in Real-Time CDP Collaboration. Per istruzioni dettagliate, consulta [Eseguire l&#39;onboarding dell&#39;account](./onboard-account.md).
* Le autorizzazioni necessarie per aggiungere tipi di pubblico all’interno dell’organizzazione.
* Un file CSV contenente i dati sul pubblico con campi di identità come e-mail o telefono.

## Caricare un file CSV {#upload-csv-file}

Dalla scheda **[!UICONTROL Tipi di pubblico]** nell&#39;area di lavoro **[!UICONTROL Configurazione]**, selezionare l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) e quindi selezionare **[!UICONTROL Pubblico]**.

Se questo è il tuo primo pubblico, puoi anche selezionare l&#39;opzione **[!UICONTROL Aggiungi]**.

![Scheda Pubblico personale nell&#39;area di lavoro di configurazione con l&#39;icona Aggiungi e l&#39;opzione Aggiungi pubblico visualizzate.](../../assets/setup/add-manage-audiences/add-audiences.png)

Viene visualizzato il flusso di lavoro Aggiungi pubblico. Seleziona **[!UICONTROL Aggiungi una nuova connessione dati]**, quindi seleziona **[!UICONTROL Avanti]**.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione Aggiungi una nuova connessione dati evidenziata.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Seleziona File CSV come connessione dati {#select-csv-file}

Seleziona **[!UICONTROL File CSV]** come connessione dati, seguito da **[!UICONTROL Avanti]**.

![La schermata di selezione della connessione dati con il file CSV disponibile come opzione selezionabile.](../../assets/setup/csv-audience-sourcing/select-csv-data-connection.png)

### Seleziona file {#select-file}

Scegli **[!UICONTROL Seleziona dal computer]** per caricare un file CSV dal sistema locale. In alternativa, puoi trascinare e rilasciare il file CSV da caricare nel pannello [!UICONTROL Trascina e rilascia un file CSV].

>[!IMPORTANT]
>
>Sono supportati solo i file CSV. La dimensione massima del file è **2 GB**.

![Seleziona un file CSV contenente i dati del pubblico del sistema locale.](../../assets/setup/csv-audience-sourcing/select-file.png)

Una volta caricata, l’interfaccia utente mostra un riepilogo che include il numero di colonne, un conteggio stimato delle righe, la struttura del file e un’anteprima delle prime 10 righe di dati.

Rivedi il riepilogo, quindi seleziona **[!UICONTROL Successivo]**.

![Visualizza in anteprima i dati del pubblico di esempio dal file CSV.](../../assets/setup/csv-audience-sourcing/preview-sample-data.png)

#### Sostituisci file {#replace-file}

Se devi caricare un file CSV diverso, scegli **[!UICONTROL Sostituisci il file]** e seleziona il nuovo file. L’interfaccia viene quindi aggiornata per visualizzare un riepilogo aggiornato dei nuovi dati.

Dopo aver rivisto il riepilogo rivisto, seleziona **[!UICONTROL Successivo]**.

![Selezionare l&#39;opzione Sostituisci file per caricare un altro file CSV.](../../assets/setup/csv-audience-sourcing/replace-file.png)

### Conferma la conferma del consenso {#confirm-consent}

Prima di procedere, devi riconoscere che le rinunce al consenso sono state rimosse dai dati del pubblico. Collaboration richiede dati sul pubblico puliti senza che gli utenti abbiano rinunciato alla condivisione dei dati.

Seleziona la casella di conferma seguita da **[!UICONTROL OK]** per confermare. La finestra di dialogo si chiude e si passa alla schermata dei campi mappa.

![La finestra di dialogo per la conferma della rinuncia al consenso richiede conferma prima di procedere.](../../assets/setup/csv-audience-sourcing/consent-optout-acknowledgment.png)

### Mappare i campi di identità sorgente {#map-fields}

La mappatura dei campi determina il modo in cui Collaboration utilizza i dati sul pubblico per l’analisi di attivazione e sovrapposizione. Nella schermata **[!UICONTROL Mappa campi]**, utilizza i menu a discesa per mappare ogni campo dell&#39;identità di origine dal file CSV al campo di destinazione appropriato in Collaboration.

Se sono necessari ulteriori dettagli su un campo di destinazione, inclusi il tipo di dati o la descrizione, selezionare **[!UICONTROL Dettagli campi di destinazione]** per ulteriori informazioni.

![Elenco a discesa per mappare un campo dell&#39;identità di origine dai dati del pubblico CSV al campo di destinazione in Collaboration.](../../assets/setup/csv-audience-sourcing/map-fields.png)

Rivedere quindi i campi mappati e selezionare **[!UICONTROL Avanti]**.

![Schermata di mappatura campi che mostra i campi di identità di origine e di destinazione mappati.](../../assets/setup/csv-audience-sourcing/confirm-mapped-fields.png)

### Rivedi e completa il caricamento {#review-and-complete}

Viene visualizzata la schermata **[!UICONTROL Rivedi]** con un riepilogo delle impostazioni del pubblico dal file CSV. Esamina le informazioni nelle sezioni seguenti:

* **[!UICONTROL Informazioni sul file]**: visualizza il nome del file, il numero di colonne e il numero di righe stimato.
* **[!UICONTROL Mappatura]**: elenca il modo in cui i campi di origine del file del pubblico caricato (ad esempio, `email`) vengono mappati sui campi di destinazione utilizzati in Collaboration (ad esempio, e-mail con hash).

Se devi modificare una sezione, fai clic sull’icona a forma di matita. Seleziona **[!UICONTROL Completa]** per confermare tutte le sezioni.

![Rivedi il riepilogo delle impostazioni di caricamento, incluse le informazioni sul file CSV e i dettagli di mappatura dei campi.](../../assets/setup/csv-audience-sourcing/review-upload-summary.png)

Sotto le sezioni di riepilogo viene visualizzata una barra di avanzamento per indicare l’avanzamento del caricamento. Al termine del caricamento, una finestra di dialogo di conferma conferma conferma che il pubblico CSV è stato creato e che è in corso la determinazione dell’origine del pubblico.

![Dopo aver caricato il file, viene visualizzata una finestra di dialogo di conferma che informa che il pubblico CSV è stato creato e che il sourcing del pubblico è in corso.](../../assets/setup/csv-audience-sourcing/upload-success-sourcing-in-progress.png)

## Rivedere i tipi di pubblico originati {#review-sourced-audiences}

Dopo aver caricato il file CSV, Collaboration inizia a raccogliere i tipi di pubblico dal file. Questo processo può richiedere alcuni minuti. Al termine dell&#39;operazione di sourcing, i tipi di pubblico sono disponibili nella scheda **[!UICONTROL Tipi di pubblico]** con le stesse caratteristiche e informazioni dei tipi di pubblico di Experience Platform.

![La scheda Tipi di pubblico mostra un elenco dei tipi di pubblico di origine nella visualizzazione griglia.](../../assets/setup/csv-audience-sourcing/csv-audiences-list.png)

In visualizzazione griglia o tabella, selezionare un elemento riga o **[!UICONTROL Visualizza pubblico]** per visualizzare una panoramica di un pubblico specifico. Mostra lo stato del pubblico, l’origine e il nome della connessione dati, insieme a pannelli dettagliati per:

**[!UICONTROL Identità]**: visualizza il conteggio e il raggruppamento delle identità totali quando i dati diventano disponibili.
**[!UICONTROL Categorie]**: visualizza i tag utilizzati per organizzare o filtrare il pubblico.
**[!UICONTROL Accesso alla connessione]**: indica se il pubblico è privato, pubblico o condiviso con collaboratori specifici.
**[!UICONTROL Visibilità metadati]**: visualizza le informazioni sul pubblico (ad esempio il conteggio delle identità, la percentuale di sovrapposizione e l&#39;indice) visibili ai collaboratori.

Utilizza questa visualizzazione per confermare la configurazione del pubblico e le impostazioni di visibilità prima di utilizzarlo nei progetti di collaborazione. Per ulteriori informazioni, consulta [come visualizzare un singolo pubblico](./onboard-audiences.md#view-individual-audiences).

## Passaggi successivi {#next-steps}

Hai caricato correttamente il file CSV in Collaboration. Al termine della determinazione origine, puoi:

* Crea progetti di collaborazione con i tuoi tipi di pubblico di origine. Consulta [Individuare i tipi di pubblico](../../guide/collaborate/discover.md).
* Attiva i tipi di pubblico nelle destinazioni collegate. Consulta [Attivare i tipi di pubblico](../../guide/collaborate/activate.md).
* Controlla la sovrapposizione dei tipi di pubblico e informazioni approfondite. Consulta [Misurare le prestazioni della campagna](../../guide/collaborate/measure.md).
* Gestisci le impostazioni del pubblico e la visibilità. Consulta [Source e gestisci i tipi di pubblico](./onboard-audiences.md).

Per informazioni su altri metodi di audience sourcing, vedere [Configurare AWS S3 per audience sourcing](./configure-aws-s3-audience-sourcing.md) o [Tipi di pubblico Source da Experience Platform](./onboard-audiences.md).
