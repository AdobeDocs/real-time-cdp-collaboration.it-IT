---
title: Panoramica delle designazioni
description: Scopri le destinazioni in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
TQID: https://experienceleague.adobe.com/1VvnSt3Z65dfQBfXnjJJi3H0Oj9BxFStexq3icVKxkY
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7ab1bc21a4d644e2e6a481d8de594d6a509a92a5
workflow-type: tm+mt
source-wordcount: 273
ht-degree: 6%

---

# Panoramica sulle destinazioni

{{limited-availability-release-note}}

>[!NOTE]
>
>Questa pagina descrive le destinazioni per le quali i tipi di pubblico sono attivati da **a**, ad esempio le piattaforme di archiviazione cloud. Per attivare i tipi di pubblico **a un collaboratore** in un progetto condiviso, consulta la guida [attiva tipi di pubblico](/help/guide/collaborate/activate.md).

Le destinazioni sono integrazioni utilizzate per inviare pubblici mirati a piattaforme esterne. Queste integrazioni consentono di attivare tipi di pubblico su vari canali e piattaforme di marketing da utilizzare nelle campagne e nel coinvolgimento dei clienti.

I collaboratori possono configurare le destinazioni per l’invio di tipi di pubblico a piattaforme esterne, ad esempio Adobe Experience Platform o una piattaforma di archiviazione cloud, da utilizzare nelle campagne. I collaboratori possono quindi [attivare i tipi di pubblico all&#39;interno di un progetto](../collaborate/activate.md), che vengono inviati alla destinazione configurata della connessione. L&#39;attivazione può essere eseguita da uno dei collaboratori a seconda delle impostazioni di attivazione del pubblico [configurate nella connessione](/help/guide/connect/establishing-connections.md#configure-connection-settings).

>[!IMPORTANT]
>
>Attualmente, quando i collaboratori attivano i tipi di pubblico all’interno di un progetto, vengono inviati automaticamente alla destinazione configurata della connessione. **devi** configurare una destinazione prima che il tuo collaboratore possa attivare i tipi di pubblico all&#39;interno di un progetto.

## Destinazioni disponibili {#available-destinations}

Le seguenti destinazioni sono disponibili per la configurazione in Collaboration. Per visualizzare la guida alla configurazione per quella destinazione, seleziona il nome della destinazione nella tabella seguente.

| Destinazione | Disponibilità |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Disponibile |
| [[!DNL Amazon S3]](./manage-destinations.md) | Disponibile |
| [[!DNL Snowflake]](./manage-destinations.md) | Disponibile |
| [[!DNL Google Cloud Storage]](./manage-destinations.md) | Disponibile |
| [[!DNL Azure Blob Storage]](./manage-destinations.md) | Disponibile |
| [[!DNL SFTP]](./manage-destinations.md) | Disponibile |
| [[!DNL Data Landing Zone]](./manage-destinations.md) | Disponibile |

>[!NOTE]
>
>**[!DNL Google Cloud Storage]** in questa tabella fa riferimento a **destinazioni** (in cui Collaboration invia tipi di pubblico durante l&#39;attivazione). Per **i tipi di pubblico di origine da** un bucket GCS nell&#39;area di lavoro **[!UICONTROL Configurazione]**, vedere [Configurazione di GCS per l&#39;origine del pubblico](../setup/configure-gcs-audience-sourcing.md).

## Passaggi successivi

Per configurare una destinazione, fare riferimento alla guida [configurare e gestire una destinazione](./manage-destinations.md). Dopo aver configurato la destinazione, puoi iniziare a [attivare tipi di pubblico mirati](../collaborate/activate.md) all&#39;interno dei tuoi progetti.
