---
title: Configurare e gestire le destinazioni dell’archiviazione cloud
description: Scopri come configurare, visualizzare ed eliminare una destinazione di archiviazione cloud in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 60124235569ca9b17b3bb1cef502d57d39e82e1f
workflow-type: tm+mt
source-wordcount: 885
ht-degree: 1%

---

# Configurare e gestire le destinazioni dell’archiviazione cloud

Utilizzare questa guida per configurare, visualizzare ed eliminare destinazioni di archiviazione cloud dall&#39;area di lavoro **[!UICONTROL Activation]**. Utilizza la scheda **[!UICONTROL Catalogo]** per configurare le destinazioni, la scheda **[!UICONTROL Destinazioni]** per gestirle e la scheda **[!UICONTROL Tipi di pubblico attivati]** per rivedere i tipi di pubblico attivati nelle destinazioni.

Dopo aver configurato una destinazione, questa diventa disponibile quando attivate i tipi di pubblico. Per visualizzare l&#39;elenco completo delle destinazioni supportate, fare riferimento alla tabella [destinazioni disponibili](./overview.md#available-destinations).

>[!NOTE]
>
> Questa guida utilizza come esempio una destinazione **[!DNL Amazon S3]**. Il flusso di lavoro di configurazione guidata è condiviso tra i tipi di destinazione di archiviazione cloud supportati, ma i metodi di autenticazione, i campi obbligatori e le funzionalità del connettore possono variare. Prima di configurare una destinazione, controlla i [requisiti della destinazione di archiviazione cloud](./cloud-storage-destination-requirements.md), che si collegano alla documentazione della destinazione Adobe Experience Platform corrispondente.
>
> Adobe Experience Platform dispone di un flusso di lavoro di configurazione separato in Real-Time CDP Collaboration. Per configurarlo, vedere [Configurare Adobe Experience Platform come destinazione](./experience-platform.md).

## Prerequisiti {#prerequisites}

Prima di configurare una destinazione, assicurati che:

* Hai accesso all&#39;area di lavoro **[!UICONTROL Activation]**.
* Disponi delle informazioni di connessione richieste dal provider di archiviazione cloud.
* Se devi creare un account, disponi delle credenziali o autorizzazioni necessarie.
* Hai rivisto i [requisiti per la destinazione di archiviazione cloud](./cloud-storage-destination-requirements.md).

## Configurare una destinazione {#configure-destination}

Quando configuri una destinazione, colleghi un account di archiviazione cloud a Real-Time CDP Collaboration e definisci come esportare i dati del pubblico.

Passa a **[!UICONTROL Attivazione]** > **[!UICONTROL Catalogo]**.

Nella scheda **[!UICONTROL Catalogo]** sono visualizzati i provider di destinazione disponibili. Ogni destinazione viene visualizzata come una scheda. A seconda della destinazione, la scheda può visualizzare account configurati e azioni per la visualizzazione di informazioni aggiuntive.

![Scheda Catalogo contenente le schede provider di destinazione.](/help/assets/destinations/manage-destinations/destination-provider-catalog.png)

Individuare il provider di destinazione da configurare e selezionare **[!UICONTROL Configurazione]**.

Viene aperta la configurazione guidata della destinazione e vengono descritti quattro passaggi: **[!UICONTROL Autentica]**, **[!UICONTROL Crea destinazione]**, **[!UICONTROL Mappa campi]** e **[!UICONTROL Rivedi]**.

### Autenticazione {#authenticate}

Il passaggio **[!UICONTROL Autentica]** stabilisce una connessione tra Real-Time CDP Collaboration e l&#39;account di destinazione.

Se è disponibile un account esistente, selezionalo dal selettore account. Per creare un account, selezionare **[!UICONTROL Nuovo account]**.

Seleziona un metodo di autenticazione e fornisci le informazioni necessarie sull’account. I metodi e i campi di autenticazione disponibili dipendono dal provider di destinazione selezionato. Per i requisiti specifici del connettore, consulta [Requisiti della destinazione di archiviazione cloud](./cloud-storage-destination-requirements.md).

Selezionare **[!UICONTROL Connetti ad Amazon S3]**. Per gli altri provider di destinazione, il pulsante visualizza il nome del provider corrispondente.

Dopo la convalida dell&#39;account, selezionare **[!UICONTROL Avanti]**.

![Passaggio di autenticazione che mostra la selezione dell&#39;account e la creazione di un nuovo account.](/help/assets/destinations/manage-destinations/authenticate-destination-account.png)

### Creazione destinazione {#create-destination}

Il passaggio **[!UICONTROL Crea destinazione]** definisce dove e come vengono consegnati i file di esportazione del pubblico.

Immettere un nome di destinazione e completare le impostazioni di archiviazione ed esportazione richieste. I campi disponibili dipendono dal provider di destinazione selezionato. Per le definizioni e i requisiti specifici del connettore, consulta la documentazione di destinazione collegata dai [requisiti di destinazione dell&#39;archiviazione cloud](./cloud-storage-destination-requirements.md).

Dopo aver completato tutti i campi obbligatori, seleziona **[!UICONTROL Avanti]**. La configurazione guidata avanza al passaggio di mappatura dei campi.

![Il passaggio Crea destinazione visualizza i campi di configurazione della destinazione.](/help/assets/destinations/manage-destinations/configure-new-destination.png)

### Mappare i campi {#map-fields}

Il passaggio **[!UICONTROL Mappa campi]** definisce il modo in cui le chiavi di corrispondenza del pubblico vengono mappate ai campi di identità previsti dalla destinazione.

A differenza del flusso di lavoro standard delle destinazioni Real-Time CDP, Real-Time CDP Collaboration configura queste mappature durante la creazione della destinazione. Le chiavi di corrispondenza del pubblico vengono visualizzate come campi sorgente. Mappa ciascun campo di origine all’identità di destinazione corrispondente in modo che la destinazione possa riconoscere gli identificatori esportati e associarli agli utenti previsti.

Seleziona **[!UICONTROL Aggiungi campo]** per aggiungere un&#39;altra mappatura chiave di corrispondenza oppure seleziona l&#39;icona Elimina per rimuovere una mappatura. Rivedi e configura tutte le mappature richieste.

Al termine delle mappature, selezionare **[!UICONTROL Avanti]**. La configurazione guidata avanza al passaggio di revisione.

![Il passaggio Mappa campi visualizza l&#39;attivazione corrispondente alla configurazione della mappatura chiave.](/help/assets/destinations/manage-destinations/map-destination-fields.png)

### Rivedi {#review-destination}

Il passaggio **[!UICONTROL Rivedi]** riepiloga la configurazione di destinazione prima che venga creata.

Rivedi le impostazioni di destinazione. Per apportare modifiche, selezionare l&#39;icona della matita ![Icona della matita.](../../assets/icons/edit.png) per la sezione applicabile e aggiorna la configurazione.

Quando la configurazione è corretta, selezionare **[!UICONTROL Completa]**. La destinazione viene creata e diventa disponibile per l’attivazione del pubblico.

![Il passaggio Revisione visualizza il riepilogo della configurazione di destinazione prima del completamento.](/help/assets/destinations/manage-destinations/review-destination-configuration.png)

## Visualizzare le destinazioni configurate {#view-configured-destinations}

Dopo aver configurato una destinazione, questa viene visualizzata nell’inventario di destinazione. Dall’inventario, puoi esaminarne lo stato e i tipi di pubblico ad esso attivati.

Passa a **[!UICONTROL Attivazione]** > **[!UICONTROL Destinazioni]**. Nella scheda **[!UICONTROL Destinazioni]** viene visualizzata una tabella delle destinazioni configurate.

![La scheda Destinazioni visualizza le destinazioni configurate.](/help/assets/destinations/manage-destinations/configured-destinations-list.png)

## Eliminare una destinazione {#delete-destination}

Elimina una destinazione quando non è più necessaria per l&#39;attivazione del pubblico. L’eliminazione di una destinazione la rimuove dall’inventario di destinazione e impedisce che i tipi di pubblico vengano attivati in futuro.

>[!IMPORTANT]
>
>L’eliminazione di una destinazione non rimuove i dati sul pubblico precedentemente esportati. Rimuovi i dati esportati in precedenza direttamente dall’archivio dati di destinazione.

Passa a **[!UICONTROL Attivazione]** > **[!UICONTROL Destinazioni]**.

Individua la destinazione da rimuovere, seleziona l&#39;icona con i puntini di sospensione nella colonna **[!UICONTROL Azione]**, quindi seleziona **[!UICONTROL Elimina]**.

![Scheda Destinazioni dell&#39;area di lavoro Attivazione con l&#39;icona con i puntini di sospensione e l&#39;azione Elimina evidenziata.](/help/assets/destinations/manage-destinations/delete-configured-destination.png)

Viene visualizzata una finestra di dialogo di conferma. Rivedi la destinazione che verrà rimossa, quindi seleziona **[!UICONTROL Elimina]** per confermare.

La destinazione viene rimossa dall’inventario di destinazione e non è più disponibile per l’attivazione del pubblico.

## Passaggi successivi {#next-steps}

Dopo aver configurato una destinazione, puoi iniziare [ad attivare i tipi di pubblico](../collaborate/activate.md) all&#39;interno dei tuoi progetti.
