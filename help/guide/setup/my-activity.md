---
title: Tracciare le attività che consumano crediti
description: Scopri come visualizzare il Portafoglio di credito della tua organizzazione e tenere traccia dell’attività di consumo del credito in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
TQID: https://experienceleague.adobe.com/hDvkKFUCBYvsX8wntcYFrL6qZTxOo5CZOWAbxNwk7mw
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 681f4af47a58a2ce66b25b09d793d0b5b127df39
workflow-type: tm+mt
source-wordcount: 726
ht-degree: 2%

---

# Tracciare le attività che consumano crediti {#track-credit-consumption-activity}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_my_activity"
>title="Maggiori informazioni"
>abstract=""

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**Periodo di non eccedenza di 90 giorni**: i clienti delle aree idonee usufruiscono di un periodo di non eccedenza di 90 giorni a partire dalla data di disponibilità nella propria area geografica. Durante questo periodo, i clienti non devono sostenere commissioni per il superamento del loro diritto al credito.

>[!ENDSHADEBOX]

Per accedere al tuo portafoglio crediti e all&#39;attività relativa al consumo di crediti, passa a **[!UICONTROL Configurazione]** nella navigazione principale, quindi seleziona la scheda **[!UICONTROL Attività personale]**.

![La scheda Attività personali mostra il wallet di credito con i crediti assegnati, i crediti utilizzati, i crediti disponibili e la tabella delle attività di consumo credito.](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>La visualizzazione **[!UICONTROL La mia attività]** non include le azioni dell&#39;utente da altre aree dell&#39;interfaccia di Real-Time CDP Collaboration. Utilizza la funzionalità [registri di controllo](/help/guide/setup/audit-logs.md) per ottenere tali informazioni.

## Comprendere la vista Attività personale {#understand-dashboard}

Utilizza la visualizzazione **[!UICONTROL La mia attività]** per monitorare l&#39;utilizzo del credito e rivedere le attività che utilizzano crediti. La visualizzazione include il Portafoglio crediti e una tabella attività.

Il Portafoglio crediti mostra i crediti con provisioning, i crediti consumati e i crediti disponibili.

| Metrica | Descrizione |
|---------|-------------|
| **[!UICONTROL Crediti con provisioning]** | Il numero di crediti di cui è stato effettuato il provisioning per il tuo account. |
| **[!UICONTROL Crediti utilizzati]** | Il numero di crediti utilizzati dal tuo account al momento dell’ultimo aggiornamento giornaliero. |
| **[!UICONTROL Crediti disponibili]** | Il numero di crediti disponibili per il tuo account, calcolato dai crediti con provisioning meno i crediti consumati. |

{style="table-layout:auto"}

Nella tabella delle attività sono elencati i record del consumo di credito giornaliero per data, tipo di attività, input elaborati e crediti utilizzati:

>[!NOTE]
>
>Le attività di **[!UICONTROL Gestione dell&#39;audience]** non sono associate a un altro collaboratore, pertanto le colonne **[!UICONTROL ID connessione]** e **[!UICONTROL Nome connessione]** per questi tipi di attività mostrano un valore **[!UICONTROL -]**.

| Colonna | Descrizione |
|------------|--------------|
| **[!UICONTROL Data]** | La data in cui si è verificata l’attività, visualizzata nel formato MM/GG/AAAA. |
| **[!UICONTROL ID connessione]** | Un identificatore univoco per ogni connessione associata a un’attività che consuma credito, rappresentato come stringa alfanumerica. |
| **[!UICONTROL Nome connessione]** | Nome del collaboratore associato alla connessione e all&#39;attività che richiede credito. |
| **[!UICONTROL Attività]** | Tipo di attività eseguita, ad esempio **[!UICONTROL Activation - Audience Access (Once)]**, **[!UICONTROL Activation - Audience Access (Recurring)]**, **[!UICONTROL Activation - Audience Egress (Once)]**, **[!UICONTROL Activation - Audience Egress (Recurring)]** o **[!UICONTROL Audience Management]**. |
| **[!UICONTROL Input elaborati]** | Il numero totale di input (ad esempio, ID o righe) elaborati per l’attività. |
| **[!UICONTROL Totale crediti utilizzati]** | Il totale dei crediti utilizzati dall&#39;attività. |
| **[!UICONTROL La mia condivisione di credito]** | La porzione del tuo account dei crediti utilizzati per l&#39;attività. |

{style="table-layout:auto"}

## Tipi di attività {#types-of-activities}

La colonna **[!UICONTROL Attività]** mostra diversi tipi di operazioni che richiedono credito.

* **[!UICONTROL Gestione dell&#39;audience]**: i crediti vengono utilizzati quando i tipi di pubblico provengono da Collaboration. I crediti vengono utilizzati in funzione del numero di ID indicizzati all’interno di Collaboration in tutti i tipi di pubblico e della frequenza di tale indicizzazione, ad esempio giornaliera, ogni tre giorni o settimanale. Per ulteriori informazioni, consulta la guida [sourcing e gestione dei tipi di pubblico](/help/guide/setup/onboard-audiences.md).
* **[!UICONTROL Attivazione - Accesso al pubblico (una volta)]**: i crediti vengono utilizzati quando l&#39;accesso al pubblico viene elaborato una volta tramite il flusso di lavoro di attivazione. Per ulteriori informazioni, consulta la guida [attivazione di tipi di pubblico](/help/guide/collaborate/activate.md).
* **[!UICONTROL Attivazione - Accesso al pubblico (ricorrente)]**: i crediti vengono utilizzati quando l&#39;accesso al pubblico viene elaborato in base a una pianificazione ricorrente tramite il flusso di lavoro di attivazione. Per ulteriori informazioni, consulta la guida [attivazione di tipi di pubblico](/help/guide/collaborate/activate.md).
* **[!UICONTROL Attivazione - Uscita del pubblico (una volta)]**: i crediti vengono utilizzati quando l&#39;uscita del pubblico verso una destinazione viene elaborata una volta tramite il flusso di lavoro di attivazione. Questa attività è a carico del collaboratore che riceve il pubblico. Per ulteriori informazioni, consulta la guida [attivazione di tipi di pubblico](/help/guide/collaborate/activate.md).
* **[!UICONTROL Attivazione - Uscita del pubblico (ricorrente)]**: i crediti vengono utilizzati quando l&#39;uscita del pubblico verso una destinazione viene elaborata in base a una pianificazione ricorrente tramite il flusso di lavoro di attivazione. Questa attività è a carico del collaboratore che riceve il pubblico. Per ulteriori informazioni, consulta la guida [attivazione di tipi di pubblico](/help/guide/collaborate/activate.md).
* **[!UICONTROL Misurazione]**: i crediti vengono utilizzati quando generi rapporti sulle prestazioni delle campagne e informazioni in Collaboration. I crediti vengono utilizzati in base al numero di righe nei rapporti sulle campagne in tutte le campagne e alla frequenza di reporting, ad esempio giornaliero, ogni tre giorni o settimanale.

## Gestione del consumo di credito {#manage-credit-consumption}

Per gestire in modo efficace il consumo di credito:

1. **Comprendere** il consumo di credito associato a ogni attività. Consultate la [descrizione del prodotto Collaboration](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} per una tabella dei crediti utilizzati per ogni attività.
2. **Monitora l&#39;utilizzo regolarmente**: controlla i crediti e la tabella delle attività disponibili per comprendere i modelli di utilizzo nelle attività di gestione dell&#39;audience, accesso all&#39;audience, uscita dall&#39;audience e misurazione.
3. **Traccia per connessione**: utilizzare il nome della connessione per identificare le connessioni che utilizzano più crediti.
