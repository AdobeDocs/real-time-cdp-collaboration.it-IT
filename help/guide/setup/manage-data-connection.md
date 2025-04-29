---
title: Gestisci connessioni dati
description: Scopri come gestire le connessioni dati, tra cui le chiavi di corrispondenza, la pianificazione, i casi d’uso e il filtro del pubblico in Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 17%

---

# Gestisci connessioni dati

{{limited-availability-release-note}}

## Panoramica

Utilizza le connessioni dati in Real-Time CDP Collaboration per importare tipi di pubblico da varie sorgenti. Scopri come gestire le chiavi di corrispondenza e pianificare le importazioni di dati per le connessioni dati esistenti. Inoltre, potrai filtrare i tipi di pubblico in base a attributi diversi per ottenere informazioni più granulari.

Prima di gestire le connessioni dati qui, devi impostarle inizialmente durante il [flusso di lavoro di onboarding del pubblico](./onboard-audiences.md). In questo modo le origini dati corrette verranno connesse per l&#39;utilizzo in Real-Time CDP Collaboration.

## Visualizzare connessioni dati

>[!IMPORTANT]
>
>L’eliminazione di una connessione dati non è attualmente supportata nell’interfaccia utente di Real-Time CDP Collaboration. Per eliminare una connessione dati, contatta il tuo rappresentante Adobe o [crea un ticket di assistenza clienti](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=open-ticket#support){target="_blank"}.

Per visualizzare le connessioni dati esistenti, passa a **[!UICONTROL Configurazione]** > **[!UICONTROL Tipi di pubblico]** e seleziona **[!UICONTROL Gestisci connessioni dati]**.

![Area di lavoro di installazione con l&#39;opzione Gestisci connessioni dati evidenziata.](/help/assets/setup/manage-data-connection/manage-data-connection-highlighted.png){zoomable="yes"}

Viene visualizzata una visualizzazione di tutte le connessioni dati attualmente impostate, con informazioni sul numero di tipi di pubblico in ciascuno di essi, l’origine della connessione dati e altro ancora. Selezionare **[!UICONTROL Visualizza connessione dati]** per visualizzare informazioni sulle chiavi di corrispondenza, la pianificazione e i tipi di pubblico che fanno parte di questa connessione dati.

![Gestione delle connessioni dati nell&#39;area di lavoro con connessioni Visualizza connessioni dati evidenziate. ](/help/assets/setup/manage-data-connection/view-data-connection-highlighted.png){zoomable="yes"}

### Chiavi di corrispondenza {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Chiavi di corrispondenza"
>abstract="Le chiavi di corrispondenza determinano il modo in cui verranno abbinati i dati provenienti da origini diverse. Scegli le chiavi di corrispondenza più rilevanti per i tuoi casi d’uso e linee guida sulla privacy."

Le chiavi di corrispondenza sono identificatori utilizzati per riconciliare i membri tra tipi di pubblico di diverse origini dati. Le chiavi di corrispondenza disponibili includono:

- **E-mail con hash**

Impossibile modificare le chiavi di corrispondenza utilizzate in questa connessione dati.

![Area di lavoro connessioni dati con la sezione Chiavi di corrispondenza evidenziata.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Pianificazione {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Pianificazione"
>abstract="Questa visualizzazione mostra le opzioni di pianificazione selezionate inizialmente per la connessione dati."

Non è possibile modificare le opzioni di pianificazione selezionate inizialmente per la connessione dati. Per ulteriori informazioni sulle opzioni di pianificazione, visualizzare la [sezione di pianificazione](/help/guide/setup/onboard-audiences.md#schedule) nel documento del flusso di lavoro di importazione del pubblico.

![Area di lavoro connessioni dati con la sezione Pianificazione evidenziata.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Gestire i tipi di pubblico {#manage-audiences}

Quando visualizzi l’elenco dei tipi di pubblico dalla connessione dati, puoi scegliere di visualizzarli, modificarne le categorie o rimuoverli dalla connessione dati.

![Un&#39;area di lavoro connessioni dati con i tipi di pubblico evidenziati.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Passaggi successivi

Dopo aver gestito le connessioni dati, puoi [individuare le sovrapposizioni](/help/guide/collaborate/discover.md) tra i tipi di pubblico e quelli che il tuo collaboratore ha reso individuabili.
