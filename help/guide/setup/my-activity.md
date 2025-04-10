---
title: Tracciare l’attività di consumo del credito
description: Scopri come tenere traccia dell’attività di consumo del credito della tua organizzazione in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: 1e8c2fdb3294111562f206ac141cfa39d5193c6c
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Tracciare l’attività di consumo del credito

{{limited-availability-release-note}}

Utilizza la scheda **[!UICONTROL La mia attività]** per monitorare e tenere traccia del consumo di credito stimato della tua organizzazione in tutte le attività di collaborazione. Questa funzione fornisce informazioni dettagliate sull’utilizzo dei crediti in diverse connessioni e attività, consentendoti di gestire le risorse in modo efficace.

>[!IMPORTANT]
>
>La tabella del consumo di credito è arrotondata per eccesso e aggregata per giorno a fini di monitoraggio. Le cifre nel dashboard **[!UICONTROL La mia attività]** rappresentano un consumo di credito *stimato*. Il consumo di credito *effettivo* utilizzato per la fatturazione viene registrato nei sistemi interni ed è disponibile su richiesta. Per ottenere tali informazioni, contatta il rappresentante Adobe.

Per accedere all&#39;attività di consumo del credito stimata, passa a **[!UICONTROL Configurazione]** nella navigazione principale, quindi seleziona la scheda **[!UICONTROL Attività personale]**.

![Il mio dashboard attività mostra i dettagli sul consumo di credito](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>La visualizzazione **[!UICONTROL La mia attività]** non include informazioni sulle azioni dell&#39;utente in parti diverse dell&#39;interfaccia utente di Real-Time Collaboration CDP. Utilizza la funzionalità [registri di controllo](/help/guide/setup/audit-logs.md) per ottenere tali informazioni.

## Comprendere il dashboard delle attività

Il dashboard attività visualizza un elenco completo di tutte le operazioni che richiedono credito all’interno dell’organizzazione. Ogni riga rappresenta un’attività distinta e fornisce informazioni chiave sull’utilizzo del credito:

>[!NOTE]
>
>Le attività di **[!UICONTROL Gestione dell&#39;audience]** non sono associate a un altro collaboratore, pertanto le colonne **[!UICONTROL ID connessione]** e **[!UICONTROL Nome connessione]** per questi tipi di attività indicano un valore **[!UICONTROL N/A]**.

| Colonna | Descrizione |
|--------|-------------|
| **[!UICONTROL Data]** | La data in cui si è verificata l’attività, visualizzata nel formato MM/GG/AAAA. |
| **[!UICONTROL ID connessione]** | Un identificatore univoco per ogni connessione associata a un’attività che consuma credito, rappresentato come stringa alfanumerica. |
| **[!UICONTROL Nome connessione]** | Nome del collaboratore associato alla connessione e all&#39;attività che richiede credito. |
| **[!UICONTROL Attività]** | Tipo di attività eseguita, ad esempio **Attivazione - Condivisione**, **Attivazione - Uscita** o **Gestione dell&#39;audience**. |
| **[!UICONTROL Totale crediti utilizzati]** | Numero totale di crediti utilizzati dall&#39;attività. |
| **[!UICONTROL La mia condivisione di credito]** | Parte dei crediti utilizzati per l&#39;attività della tua organizzazione. |

{style="table-layout:auto"}

## Tipi di attività {#types-of-activities}

La colonna **[!UICONTROL Attività]** mostra diversi tipi di operazioni che richiedono credito.

* **[!UICONTROL Gestione dell&#39;audience]**: i crediti vengono utilizzati quando i tipi di pubblico vengono importati in Real-Time CDP Collaboration. I crediti vengono utilizzati in funzione del numero di ID (in milioni) indicizzati all’interno di Real-Time CDP Collaboration per tutti i tipi di pubblico e della frequenza di tale indicizzazione (giornaliera, ogni tre giorni o settimanale) durante il periodo di fatturazione. Ulteriori informazioni sull&#39;[importazione e gestione dei tipi di pubblico](/help/guide/setup/onboard-audiences.md).
* **[!UICONTROL Attivazione - Condivisione]** - I crediti vengono utilizzati in funzione del numero di ID attivati da Real-Time CDP Collaboration durante il periodo di fatturazione. Ulteriori informazioni su [condivisione](/help/guide/collaborate/share.md) e [attivazione di tipi di pubblico](/help/guide/collaborate/activate.md) in Real-Time CDP Collaboration.
* **[!UICONTROL Attivazione - Uscita]** - I crediti vengono utilizzati in funzione del numero di ID attivati da Real-Time CDP Collaboration durante il periodo di fatturazione. Ulteriori informazioni su [condivisione](/help/guide/collaborate/share.md) e [attivazione di tipi di pubblico](/help/guide/collaborate/activate.md) in Real-Time CDP Collaboration.


<!--

**[!UICONTROL Audience Overlaps]** – Credits are consumed as a function of the number of matched IDs across 2 or more shared audiences throughout the billing period. Read more about [audience overlaps in the discover tab](/help/guide/collaborate/discover.md).

Collaboration Measurement – Credits are consumed as a function of the number of rows existing in campaign reports across all campaigns, and the frequency of that reporting (daily, every three days, or weekly).

-->


## Gestione del consumo di credito {#manage-credit-consumption}

Per gestire in modo efficace il consumo di credito:

1. **Comprendere** il consumo di credito associato a ogni attività. Consultate la [descrizione del prodotto Real-Time CDP Collaboration](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} per una tabella dei crediti di collaborazione utilizzati per ogni attività.
2. **Monitora regolarmente**: controlla spesso il dashboard attività per comprendere i pattern di utilizzo.
3. **Traccia per connessione**: utilizzare il nome della connessione per identificare le relazioni che utilizzano più crediti.

<!--

## Pagination and navigation

The activity list is paginated to improve performance and readability. Use the navigation controls at the bottom of the table to move between pages and adjust how many records you can view at once.

-->
