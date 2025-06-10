---
title: Gestisci connessioni dati
description: Scopri come gestire le connessioni dati, tra cui le chiavi di corrispondenza, la pianificazione, i casi d’uso e il filtro del pubblico in Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: b28bb5037c25f630059e6e8bc375ce28e0967ac7
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 10%

---

# Gestisci connessioni dati

{{limited-availability-release-note}}

## Panoramica

Utilizza le connessioni dati in Real-Time CDP Collaboration per importare tipi di pubblico da varie sorgenti. Scopri come gestire le chiavi di corrispondenza e pianificare le importazioni di dati per le connessioni dati esistenti. Inoltre, potrai filtrare i tipi di pubblico in base a attributi diversi per ottenere informazioni più granulari.

## Visualizzare connessioni dati

Per visualizzare le connessioni dati esistenti, passare a **[!UICONTROL Configurazione]** e selezionare la scheda **[!UICONTROL Connessioni dati personali]**. Viene visualizzata tutta la connessione dati corrente, con una breve panoramica di ogni connessione. Per una visualizzazione completa delle informazioni di una connessione dati, incluse le chiavi di corrispondenza, i dettagli di pianificazione e i tipi di pubblico, selezionare **[!UICONTROL Visualizza connessione dati]** nella connessione corrispondente.

![Imposta l&#39;area di lavoro con la visualizzazione della scheda Connessioni dati visualizzata ed evidenziata.](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### Chiavi di corrispondenza {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Chiavi di corrispondenza"
>abstract="Le chiavi di corrispondenza determinano il modo in cui verranno abbinati i dati provenienti da origini diverse. Scegli le chiavi di corrispondenza più rilevanti per i tuoi casi d’uso e linee guida sulla privacy."

Le chiavi di corrispondenza sono identificatori utilizzati per riconciliare i membri tra tipi di pubblico di diverse origini dati. Non puoi modificare le chiavi di corrispondenza selezionate inizialmente per la connessione dati.

>[!IMPORTANT]
> 
>Impossibile modificare le chiavi di corrispondenza dopo la creazione della connessione dati. Per aggiornare le chiavi di corrispondenza, è necessario creare una nuova connessione dati.

Le chiavi di corrispondenza disponibili includono:

- **E-mail con hash**

![Area di lavoro connessioni dati con la sezione Chiavi di corrispondenza evidenziata.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Pianificazione {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Pianificazione"
>abstract="Visualizza i dettagli di pianificazione per la connessione dati e, se necessario, modifica la frequenza di aggiornamento."

Visualizza e gestisci le impostazioni di pianificazione per le connessioni dati. La pianificazione determina la frequenza con cui il pubblico viene aggiornato.

Dopo aver creato una connessione dati, è possibile aggiornarne la frequenza di aggiornamento direttamente dalla sezione **[!UICONTROL Pianificazione]** dell&#39;area di lavoro connessione dati.

>[!NOTE]
>
>Quando si selezionano i tipi di pubblico da Adobe Experience Platform, i tipi di pubblico diventano disponibili entro 24 ore dall’impostazione della connessione dati. Dopo l’importazione iniziale, i dati del pubblico vengono aggiornati in base alla frequenza definita.

Per ulteriori informazioni sulla pianificazione, consulta la [sezione pianificazione](/help/guide/setup/onboard-audiences.md#schedule) nella guida ai tipi di pubblico per l&#39;onboarding.

![Area di lavoro di una connessione dati con la sezione Pianificazione evidenziata.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

#### Modifica pianificazione {#edit-scheduling}

Puoi modificare la frequenza di una connessione dati esistente per controllare meglio la frequenza con cui i tipi di pubblico vengono aggiornati. Per modificare la pianificazione, seleziona **[!UICONTROL Modifica]** dalla connessione dati nella scheda di pianificazione.

Nella finestra di dialogo **[!UICONTROL Pianificazione]**, seleziona il menu a discesa per aggiornare la **[!UICONTROL Frequenza]**. Impostare la frequenza di aggiornamento in modo che venga eseguita ogni giorno oppure ogni due o sei giorni. Al termine, seleziona **[!UICONTROL Salva]** per applicare le modifiche.

![Finestra di dialogo Pianificazione, in cui sono visualizzate le opzioni per impostare la frequenza e l&#39;intervallo di date.](../../assets/setup/manage-data-connection/scheduling-dialog.png){zoomable="yes" alt="The Scheduling dialog with editable fields for frequency."}

## Elimina connessione dati

L’eliminazione di una connessione dati rimuoverà tutti i tipi di pubblico sottostanti, le impostazioni associate e l’utilizzo nella piattaforma. Questa azione non può essere annullata.

Per eliminare una connessione dati esistente, selezionare l&#39;icona Elimina (![icona Elimina](/help/assets/common/delete.svg)) nell&#39;area di lavoro di una singola connessione dati.

![Area di lavoro connessioni dati con l&#39;opzione Elimina evidenziata.](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo di conferma. Seleziona **[!UICONTROL Elimina]** per completare l&#39;eliminazione della connessione dati.

![Finestra di dialogo Elimina connessione dati con l&#39;opzione Elimina evidenziata.](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## Gestire i tipi di pubblico {#manage-audiences}

Nella parte inferiore dell’area di lavoro viene visualizzato un elenco di tipi di pubblico associati alla connessione dati. L’elenco presenta una breve panoramica di ciascun pubblico, con il relativo stato, l’origine e l’accesso alla connessione. Per modificare le categorie di un pubblico, l’accesso alla connessione o la visibilità dei metadati, seleziona il nome del pubblico. Per una guida completa sulla gestione di un pubblico, consulta la guida [visualizza i singoli tipi di pubblico](./onboard-audiences.md#view-individual-audiences).

![Un&#39;area di lavoro connessioni dati con i tipi di pubblico evidenziati.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Passaggi successivi

Dopo aver gestito le connessioni dati, puoi [individuare le sovrapposizioni](/help/guide/collaborate/discover.md) tra i tipi di pubblico e quelli che il tuo collaboratore ha reso individuabili.
