---
title: Arricchisci i profili con segnali multimediali a pagamento da [!DNL The Trade Desk] (Alpha)
description: Scopri come esportare attributi di arricchimento di contenuti multimediali a pagamento, acquisire il CSV consegnato e aggiornare profili di prime parti per la creazione e la personalizzazione del pubblico.
audience: advertiser
hide: true
badge: Alpha
source-git-commit: 303d7185169962ad7398adfffcc732bf86336a74
workflow-type: tm+mt
source-wordcount: '1512'
ht-degree: 0%
---

# Arricchimento del profilo di Trade Desk (Alpha)

Utilizzare il feed di dati del registro delle impression Raw Event Data Stream (REDS) da [!DNL The Trade Desk] per esportare gli attributi di arricchimento e il contesto multimediale a pagamento nei profili di prime parti.

Dopo che il file CSV arriva nella destinazione di esportazione [!DNL Amazon S3], acquisiscilo in [!DNL Adobe Real-Time CDP]. In questa versione, l’esportazione del file non aggiorna automaticamente i profili né attiva le esperienze. L&#39;arricchimento automatico del profilo in [!DNL Adobe Real-Time CDP] è pianificato per una versione successiva.

L’esposizione degli annunci aggiunge contesto ai profili dei clienti. Non conferma il coinvolgimento, l’intento di acquisto o interessi a lungo termine.

## Preparazione all’arricchimento {#prepare-for-enrichment}

Prima di iniziare, rivolgiti all’amministratore, al team multimediale e al team dati per assicurarti di disporre di:

* Accesso a [!DNL Adobe Real-Time CDP Collaboration] e a un contratto di partecipazione firmato.
* Lettera di accesso completata con [!DNL The Trade Desk] per autorizzare il provisioning dei feed REDS.
* Tipi di pubblico di prime parti disponibili in [!DNL Adobe Real-Time CDP Collaboration] che utilizzano indirizzi e-mail con hash o numeri di telefono con hash. Altri identificatori non sono supportati in questa versione.
* Una destinazione [!DNL Amazon S3] configurata per ricevere l&#39;output di arricchimento.
* Processo per acquisire il file consegnato in [!DNL Adobe Real-Time CDP].

### Autorizza il feed di origine {#authorize-source-feed}

Per autorizzare la consegna del registro REDS direttamente ad Adobe, completare la lettera di accesso fornita da [!DNL The Trade Desk].

[!DNL The Trade Desk] esegue il provisioning del feed di origine e Adobe configura l&#39;accesso e l&#39;acquisizione. Prima di creare un progetto, verifica che la connessione sia attiva e che il feed sia pronto.

Dopo l’elaborazione, il file di output dell’arricchimento arriva alla destinazione di esportazione.

### Preparare l’acquisizione a valle {#prepare-downstream-ingestion}

Dopo la consegna, chiedere all&#39;amministratore di [!DNL Adobe Real-Time CDP] o al team di supporto tecnico di acquisire il file.

## Connetti e crea progetti {#connect-create-projects}

Completa la lettera di accesso nella finestra di dialogo della connessione e salva il tuo ID partner. Prima di creare un progetto, attendi che Adobe confermi di aver ricevuto i registri REDS. La creazione di un progetto avvia il processo di arricchimento, che richiede sia l’ID partner che i registri.

### Connettersi con il partner {#connect-partner}

Per connettersi con [!DNL The Trade Desk], apri **[!UICONTROL Individua collaboratori]** in **[!UICONTROL Connetti]** e cerca il partner.

![Il catalogo collaboratori elenca [!DNL The Trade Desk] e la relativa opzione [!UICONTROL Connetti].](../../../assets/collaborate/advertising-platforms/discover-collaborators-trade-desk.png){zoomable="yes"}

Seleziona **[!UICONTROL Connetti]** per [!DNL The Trade Desk] e segui le istruzioni nella finestra di dialogo della connessione.

![Nella finestra di dialogo della connessione sono illustrate l&#39;autorizzazione REDS e la configurazione dell&#39;ID partner per [!DNL The Trade Desk].](../../../assets/collaborate/advertising-platforms/trade-desk-connection-instructions.png){zoomable="yes"}

Dopo che la connessione è attiva, apri **[!UICONTROL Impostazioni connessione]** e passa a **[!UICONTROL Informazioni inserzionista]**. Per aggiornare le informazioni esistenti, selezionare **[!UICONTROL Modifica]**. Per immettere nuove informazioni, selezionare **[!UICONTROL Aggiungi]**.

![Le impostazioni di connessione attive mostrano [!UICONTROL Informazioni sull&#39;inserzionista] e il controllo [!UICONTROL Modifica].](../../../assets/collaborate/advertising-platforms/trade-desk-connection-settings.png){zoomable="yes"}

Per salvare le informazioni sull&#39;inserzionista, immetti l&#39;ID e il nome del partner in **[!UICONTROL ID partner]** e **[!UICONTROL Nome partner]**, quindi seleziona **[!UICONTROL Salva]**. L&#39;ID partner viene visualizzato in **[!UICONTROL Identificatori postazione]** nel tuo account [!DNL The Trade Desk].

![La finestra di dialogo Informazioni inserzionista ha richiesto campi ID partner e Nome partner e un controllo [!UICONTROL Salva].](../../../assets/collaborate/advertising-platforms/trade-desk-advertiser-partner-info-dialog.png){zoomable="yes"}

Dopo aver salvato le informazioni dell’inserzionista, attendi che Adobe confermi la ricezione dei registri REDS prima di creare un progetto.

### Creare un progetto {#create-project}

Per creare un progetto, vai a **[!UICONTROL Collabora]** e seleziona **[!UICONTROL Progetti personali]**, quindi **[!UICONTROL Crea un progetto]** o l&#39;icona Aggiungi (![Aggiungi un progetto.](/help/assets/icons/plus.png)).

In **[!UICONTROL Crea progetto]**, selezionare [!DNL The Trade Desk] da **[!UICONTROL Collaborator]**.

![Il modulo [!UICONTROL Crea progetto] elenca [!DNL The Trade Desk] e include i campi relativi al nome del progetto, alla descrizione e all&#39;immagine.](../../../assets/collaborate/advertising-platforms/trade-desk-create-project.png){zoomable="yes"}

Per identificare il progetto, immetti un **[!UICONTROL nome progetto]** e una **[!UICONTROL descrizione]**, quindi seleziona un&#39;immagine. Al termine dei dettagli del progetto, selezionare **[!UICONTROL Crea]**.

Per informazioni generali sulla gestione dei progetti, vedere la [Guida alla creazione e alla gestione dei progetti](/help/guide/collaborate/manage-projects.md).

## Selezionare ed esportare gli attributi {#select-export-attributes}

Per selezionare gli attributi di arricchimento per l&#39;esportazione, aprire il progetto e selezionare **[!UICONTROL Arricchisci]**. Per comprendere la disponibilità del segnale, rivedere i valori di copertura per ciascun attributo prima di selezionare gli attributi che si desidera utilizzare.

![La pagina [!UICONTROL Arricchisci] raggruppa i segnali selezionabili per categoria e visualizza i valori di copertura.](../../../assets/collaborate/advertising-platforms/enrich-attribute-selection.png){zoomable="yes"}

<!-- TODO: Replace the destination screenshot with one showing the [!UICONTROL Export Attributes] action. -->

Selezionare la destinazione di esportazione [!DNL Amazon S3] configurata per l&#39;output di arricchimento. Se devi configurare una destinazione, consulta [Configurare e gestire le destinazioni dell&#39;archiviazione cloud](/help/guide/destinations/manage-destinations.md).

<!-- ![The [!UICONTROL Choose a destination] screen lists a destination and the [!UICONTROL Export Attributes] action.](../../../assets/collaborate/advertising-platforms/enrich-choose-destination.png){zoomable="yes"} -->

Rivedi gli attributi e la destinazione selezionati, quindi seleziona **[!UICONTROL Esporta attributi]**.

<!-- ![The destination screen confirms that enrichment has started.](../../../assets/collaborate/advertising-platforms/enrich-request-confirmation.png){zoomable="yes"} -->

L’invio di un’esportazione avvia la consegna se la destinazione è configurata correttamente. Dopo aver inviato l&#39;esportazione, verificare la corretta consegna del file all&#39;esterno di [!DNL Adobe Real-Time CDP Collaboration].

Adobe elabora gli attributi di arricchimento quando crei un progetto e poi settimanalmente. Ogni esecuzione utilizza gli ultimi 90 giorni di dati disponibili [!DNL The Trade Desk]. Ogni esportazione include gli attributi selezionati dall&#39;esecuzione completata più recente. Per esportare gli attributi aggiornati, richiedi un’altra esportazione al termine di un’esecuzione successiva.

### Segnali di arricchimento disponibili {#available-signals}

Scegli tra 18 segnali curati in quattro categorie. Le espressioni di arricchimento personalizzate non sono supportate.

| Categoria | Segnale | Descrizione |
| --- | --- | --- |
| Core | [!UICONTROL Ultima data esposta] | La data in cui un’identità è stata esposta più di recente a un annuncio. |
| Core | [!UICONTROL Conteggio esposizioni] | Una categoria di frequenza di esposizione, anziché un conteggio delle impression non elaborato. |
| Core | [!UICONTROL Ricerca di potenziali clienti e retargeting] | Classificazione dedotta dell’esposizione come ricerca di potenziali clienti o remarketing. |
| Core | [!UICONTROL Categoria di prodotto visualizzata] | Una categoria dedotta per i prodotti promossi negli annunci. |
| Core | [!UICONTROL Canale inventario dominante] | Il canale di inventario principale associato all’esposizione agli annunci. |
| Core | [!UICONTROL Tipo di dispositivo dominante] | Il tipo di dispositivo principale associato all’esposizione agli annunci. |
| Informazioni geografiche | [!UICONTROL Città] | Informazioni sulla città derivate dal contesto pubblicitario, non una posizione verificata. |
| Informazioni geografiche | [!UICONTROL Regione/Stato] | Informazioni sull’area geografica o sullo stato relative al contesto pubblicitario. |
| Informazioni geografiche | [!UICONTROL DMA] | Informazioni sull’area di mercato designata (DMA) derivate dal contesto pubblicitario. |
| Televisore collegato (CTV) | [!UICONTROL CTV esposto] | Aggiungere l&#39;esposizione su un dispositivo televisivo collegato. |
| Televisore collegato (CTV) | [!UICONTROL Visualizzatore di flussi live] | Esposizione degli annunci nell’inventario live-stream, non prova di visualizzazione o coinvolgimento. |
| Televisore collegato (CTV) | [!UICONTROL PMP/esposizione premium] | Mercato privato (PMP) o esposizione a contratti privati, inventario dei premi non verificato in modo indipendente. |
| Affinità dei contenuti | [!UICONTROL TV collegata / Streaming] | Esposizione annuncio associata a contenuti in streaming. |
| Affinità dei contenuti | [!UICONTROL Giocatore] | Esposizione annuncio associata a contenuti di gioco, siti o app. |
| Affinità dei contenuti | [!UICONTROL Appassionato sportivo] | Esposizione annuncio associata a contenuti sportivi, siti o app. |
| Affinità dei contenuti | [!UICONTROL Segnaposto notizie] | Esposizione annuncio associata a contenuti, siti o app di notizie. |
| Affinità dei contenuti | [!UICONTROL Appassionato di musica] | Esposizione annuncio associata a contenuti musicali, siti o app. |
| Affinità dei contenuti | [!UICONTROL Genere di contenuti] | Il genere di contenuto associato all’esposizione all’annuncio. |

I segnali geografici descrivono il contesto pubblicitario anziché una posizione attuale o domestica verificata. I segnali di affinità dei contenuti non confermano interessi o preferenze personali. Alcuni attributi potrebbero non contenere valori quando le informazioni di origine non sono disponibili.

### Copertura degli attributi {#attribute-coverage}

La copertura descrive la frequenza con cui i record elaborati includono un valore di attributo. Per i segnali sì/no, ad esempio **[!UICONTROL CTV esposto]**, la copertura conta i record con un valore true. La copertura non indica percentuali di corrispondenza di identità o la proporzione di profili di prime parti che ricevono un attributo.

La corrispondenza delle identità, la disponibilità del segnale di origine e l’acquisizione influiscono sugli aggiornamenti del profilo. La copertura non conferma il completamento dell’esportazione o gli aggiornamenti del profilo.

### Ambito flusso di lavoro {#workflow-scope}

Per arricchire i dati da [!DNL The Trade Desk], utilizza il catalogo curato. Non è possibile esportare registri non elaborati o creare espressioni di attributi personalizzati. Non sono supportate altre integrazioni di piattaforme lato domanda (DSP) e piattaforme lato offerta (SSP).

Questo flusso di lavoro non supporta l’individuazione delle opportunità di arricchimento, l’analisi di sovrapposizione del pubblico o la misurazione di attribuzione e incrementalità.

## Acquisire e convalidare i risultati {#ingest-validate-results}

Dopo la consegna, chiedere all&#39;amministratore di [!DNL Adobe Real-Time CDP] o al team di supporto tecnico di acquisire il file.

### File di output {#output-file}

L&#39;esportazione consegna un file CSV alla destinazione [!DNL Amazon S3] configurata.

<!-- 
TODO: replace this placeholder with the engineering-confirmed output specification:
* Required hashing and normalization for each identifier, including whether email requires SHA-256 after trimming and lowercasing.
* Exact CSV headers, the file naming pattern, and the delivery bucket and path.
* Each identifier column in the delivered file and the identity namespace to map that column to during ingestion.
Do not treat example formats or supported input match keys as confirmed output requirements.
-->

Verifica l’esportazione separatamente dagli aggiornamenti del profilo:

1. Verificare che il file CSV sia arrivato nel percorso [!DNL Amazon S3] previsto.
1. Verifica che il file contenga gli identificatori previsti e gli attributi selezionati.
1. Acquisisci il file utilizzando le mappature di identità e schema confermate per la sandbox e il set di dati di destinazione.
1. Rivedi i risultati dell’acquisizione e verifica che un campione dei profili previsti contenga gli attributi di arricchimento.

L’esportazione di un file non conferma che l’acquisizione abbia aggiornato i profili. Per aggiornare i profili, acquisisci separatamente ogni esportazione successiva.

## Risoluzione dei problemi di arricchimento {#troubleshoot-enrichment}

Per risolvere i problemi relativi ai dati di origine, all’esportazione e all’acquisizione, utilizza i controlli seguenti:

| Problema | Cosa controllare |
| --- | --- |
| Connessione o **[!UICONTROL Arricchisci]** non disponibile | Chiedi all’amministratore di confermare la connessione e l’accesso al progetto. Verificare che l&#39;impostazione del feed di origine sia stata completata. |
| Nessuna destinazione di esportazione disponibile | Chiedi all’amministratore di verificare che una destinazione sia configurata e disponibile per l’output di arricchimento. |
| Un attributo ha una copertura limitata | Verifica la disponibilità dei dati di origine con il tuo team multimediale. Non interpretare la copertura come una percentuale di corrispondenza del profilo. |
| È stata richiesta un&#39;esportazione, ma non è presente alcun file | Verifica la destinazione prevista con il tuo team di dati. L’invio della richiesta non conferma la consegna. |
| Un file consegnato non ha aggiornato i profili | Esamina i risultati dell’acquisizione e conferma le mappature di identità e schema. L’esportazione e l’acquisizione sono operazioni separate. |
| Impossibile richiedere un’esportazione | Seleziona almeno un attributo e una destinazione. Se un’esportazione è già in elaborazione, attendi il termine dell’operazione prima di richiederne un’altra. |
| La copertura è elevata, ma pochi profili ricevono gli attributi | La copertura non è una percentuale di corrispondenza identità. Verifica che il feed di origine sia pronto, che il pubblico utilizzi le chiavi di corrispondenza supportate e che la mappatura identità sia corretta durante l’acquisizione. |
| Dopo la creazione di un progetto non vengono visualizzati attributi o code coverage | La configurazione del progetto viene corretta al momento della creazione. Se in quel momento Adobe non aveva ricevuto i registri REDS da [!DNL The Trade Desk], il progetto non potrà utilizzarli in un secondo momento. Dopo che Adobe conferma di aver ricevuto i registri, crea un nuovo progetto. |
| I profili hanno gli attributi, ma un pubblico o un’esperienza non li riflette | Controlla la valutazione del pubblico, l’identità, il consenso e le regole di targeting delle esperienze a valle. |

## Passaggi successivi {#next-steps}

Dopo aver acquisito e convalidato gli attributi, crea tipi di pubblico in [!DNL Adobe Real-Time CDP] combinando segnali di arricchimento con dati di prime parti. Per ulteriori informazioni, consulta la [guida di Audience Builder](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-builder){target="_blank"}.

Per attivare i tipi di pubblico per le destinazioni, la personalizzazione o i percorsi di clienti, consulta la [guida all&#39;attivazione dei tipi di pubblico](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activation-overview){target="_blank"}.
