---
title: Panoramica delle designazioni
description: Scopri le destinazioni in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 6%

---

# Panoramica sulle destinazioni

{{limited-availability-release-note}}

Le destinazioni sono integrazioni utilizzate per inviare pubblici mirati a piattaforme esterne. Queste integrazioni consentono di attivare tipi di pubblico su vari canali e piattaforme di marketing da utilizzare nelle campagne e nel coinvolgimento dei clienti.

Attualmente, le destinazioni sono disponibili solo per gli editori in Adobe Real-Time CDP Collaboration. Gli editori possono configurare le destinazioni per inviare tipi di pubblico a piattaforme esterne, come Adobe Experience Platform, da utilizzare nelle campagne. Gli inserzionisti possono quindi [attivare i tipi di pubblico all&#39;interno di un progetto](../collaborate/activate.md), che vengono inviati alla destinazione configurata dell&#39;editore.

>[!IMPORTANT]
>
>Attualmente, quando gli inserzionisti attivano i tipi di pubblico all’interno del progetto, vengono inviati automaticamente alla destinazione configurata dell’editore. In qualità di editore, **devi** configurare una destinazione *prima* che il tuo collaboratore attivi un pubblico. Se non è configurata alcuna destinazione, il pubblico verrà inviato all&#39;utente e sarà visibile nella scheda **[!UICONTROL Attiva]** all&#39;interno di un progetto, ma non verrà attivato.

## Configurare le destinazioni {#configure-destinations}

Per configurare una destinazione, passare a **[!UICONTROL Configurazione]** e selezionare la scheda **[!UICONTROL Designazioni personali]**. Qui puoi visualizzare tutte le destinazioni disponibili.

>[!NOTE]
>
> Attualmente, in Collaboration è disponibile solo Adobe Experience Platform come destinazione self-service. Se ti interessa configurare una destinazione come Amazon S3 o Snowflake, contatta il tuo rappresentante Adobe.

![La scheda Destinazioni personali nell&#39;area di lavoro di installazione mostra le destinazioni disponibili.](/help/assets/destinations/overview/my-destinations-overview.png)

Per iniziare a configurare una destinazione, selezionare l&#39;opzione **[!UICONTROL Configura]** nella destinazione desiderata. Per informazioni sulla configurazione di destinazioni specifiche, consulta le guide nella tabella [destinazioni disponibili](#available-destinations).

![L&#39;area di lavoro Destinazioni personali con l&#39;opzione Configura evidenziata per la destinazione Adobe Experience Platform.](/help/assets/destinations/overview/my-destinations-set-up.png)

### Destinazioni disponibili {#available-destinations}

Le seguenti destinazioni sono disponibili per la configurazione in Collaboration. Per visualizzare la guida alla configurazione per quella destinazione, seleziona il nome della destinazione nella tabella seguente. Se ti interessa configurare una destinazione non attualmente disponibile, contatta il tuo rappresentante Adobe.

| Destinazione | Disponibilità |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Disponibile |
| Amazon S3 | In arrivo. |
| Snowflake | In arrivo. |
| Google Cloud Storage | In arrivo. |
| Archiviazione BLOB di Azure | In arrivo. |

## Passaggi successivi

Dopo aver configurato la destinazione, puoi iniziare a [attivare tipi di pubblico mirati](../collaborate/activate.md) all&#39;interno dei tuoi progetti.
