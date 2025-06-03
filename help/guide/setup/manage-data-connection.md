---
title: Gestisci connessioni dati
description: Scopri come gestire le connessioni dati, tra cui le chiavi di corrispondenza, la pianificazione, i casi d’uso e il filtro del pubblico in Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 16%

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

Le chiavi di corrispondenza disponibili includono:

- **E-mail con hash**

![Area di lavoro connessioni dati con la sezione Chiavi di corrispondenza evidenziata.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Pianificazione {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Pianificazione"
>abstract="Questa visualizzazione mostra le opzioni di pianificazione selezionate inizialmente per la connessione dati."

Non è possibile modificare le opzioni di pianificazione selezionate inizialmente per la connessione dati. Per ulteriori informazioni sulle opzioni di pianificazione, visualizzare la [sezione di pianificazione](/help/guide/setup/onboard-audiences.md#schedule) nel documento del flusso di lavoro di importazione del pubblico.

![Area di lavoro connessioni dati con la sezione Pianificazione evidenziata.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

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
