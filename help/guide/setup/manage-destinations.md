---
title: Configurare e gestire le destinazioni
description: Scopri come configurare e gestire le destinazioni in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b4b26761-46ac-420f-b9f7-6e829d67aec9
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 1%

---

# Configurare e gestire le destinazioni

{{limited-availability-release-note}}

Le destinazioni sono integrazioni utilizzate per inviare pubblici mirati a piattaforme esterne. Queste integrazioni consentono di attivare tipi di pubblico su vari canali e piattaforme di marketing da utilizzare nelle campagne e nel coinvolgimento dei clienti.

Attualmente, le destinazioni sono disponibili solo per gli editori in Real-Time CDP Collaboration. Gli editori possono configurare le destinazioni per attivare i tipi di pubblico su piattaforme esterne, come Adobe Experience Platform, da utilizzare nelle campagne. Gli inserzionisti possono quindi [inviare tipi di pubblico all&#39;interno di un progetto](../collaborate/activate.md), che vengono inviati alla destinazione configurata dell&#39;editore.

![La scheda Destinazioni personali nell&#39;area di lavoro di installazione mostra le destinazioni di Adobe Experience Platform attive.](/help/assets/setup/manage-destinations/my-destinations-overview.png)

Per ulteriori informazioni sulle destinazioni, consulta la guida [panoramica sulle destinazioni](../destinations/overview.md).

## Configurare le destinazioni {#configure-destinations}

Le designazioni sono configurate nella sezione **[!UICONTROL Configurazione]** di Collaboration. Per configurare una destinazione, passare a **[!UICONTROL Configurazione]** e selezionare la scheda **[!UICONTROL Destinazioni personali]**. Qui puoi visualizzare tutte le destinazioni disponibili.

>[!IMPORTANT]
>
>Per configurare e gestire le destinazioni, all&#39;utente deve essere assegnato un ruolo con l&#39;autorizzazione **Gestisci dati pubblico**. Per ulteriori informazioni sulla gestione dei ruoli, fare riferimento alla guida [gestione ruoli](../permissions/manage-roles.md).

![La scheda Destinazioni personali nell&#39;area di lavoro di installazione mostra le destinazioni disponibili.](/help/assets/setup/manage-destinations/my-destinations.png)

Il processo di configurazione per le destinazioni dipende dalla destinazione che si sta configurando. Consulta il catalogo [destinazioni disponibili](../destinations/overview.md#available-destinations) per visualizzare le destinazioni disponibili e le relative guide alla configurazione.

>[!NOTE]
>
>Attualmente, in Real-Time CDP Collaboration è disponibile solo Adobe Experience Platform come destinazione self-service. Se ti interessa configurare una destinazione diversa, contatta il tuo rappresentante Adobe.

## Elimina destinazioni {#delete-destinations}

L’eliminazione di una destinazione la rimuove dall’organizzazione, rimuove dalla destinazione eventuali tipi di pubblico inviati in precedenza e impedisce l’invio di eventuali tipi di pubblico futuri a tale destinazione.

Per eliminare una destinazione, passare alla scheda **[!UICONTROL Destinazioni personali]** nella sezione **[!UICONTROL Configurazione]**. Selezionare l&#39;opzione **[!UICONTROL Elimina]** per la destinazione da rimuovere.

![Area di lavoro Destinazioni personali con l&#39;opzione Elimina evidenziata per la destinazione Adobe Experience Platform.](/help/assets/setup/manage-destinations/delete-destination.png)

Viene visualizzata una finestra di dialogo di conferma, in cui è possibile confermare l’eliminazione della destinazione. Selezionare **[!UICONTROL Elimina]** per rimuovere la destinazione.

![Finestra di dialogo Elimina destinazione con l&#39;opzione Elimina evidenziata.](/help/assets/setup/manage-destinations/delete-destination-confirmation.png)

## Passaggi successivi

Dopo aver configurato la destinazione, puoi iniziare a collaborare con gli inserzionisti per [attivare tipi di pubblico mirati](../collaborate/activate.md) nei tuoi progetti.
