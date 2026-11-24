---
title: Attivare Direttamente I Tipi Di Pubblico (1P Audience Activation) - Beta
description: Scopri come attivare tipi di pubblico di prime parti personalizzati o condivisi senza un progetto, selezionare una destinazione, rivedere le mappature dei campi e impostare una pianificazione di attivazione.
badgeBeta: label="Beta" type="Informative"
source-git-commit: 5f823194a18468b9205f64853551719ae8a3752f
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 1%
---

# Attivare direttamente i tipi di pubblico (1P Audience Activation) {#activate-audiences-directly}

Utilizzare l&#39;attivazione diretta del pubblico di prima parte (1P) in [!DNL Adobe Real-Time CDP Collaboration] per inviare i tipi di pubblico a una destinazione senza creare un progetto. Attiva i tipi di pubblico di cui sei proprietario o che sono condivisi con te per un utilizzo di prime parti.

Inizia da una destinazione configurata o **[!UICONTROL Tipi di pubblico attivati]**, quindi seleziona i tipi di pubblico e imposta la pianificazione dell&#39;attivazione.

Per inviare e attivare tipi di pubblico tramite un progetto di collaborazione, vedere [Inviare e attivare tipi di pubblico in un progetto](/help/guide/collaborate/activate.md).

## Accesso del pubblico per l’attivazione {#audience-access-for-activation}

Controlla l’origine del pubblico per determinare se è necessaria una sovvenzione prima dell’attivazione.

| Origine pubblico | Requisito di accesso |
| --- | --- |
| I tuoi tipi di pubblico | I tipi di pubblico sono tua. |
| Tipi di pubblico condivisi con te | È necessaria una sovvenzione attiva con autorizzazione di attivazione diretta. Il provider mantiene la proprietà. |

{style="table-layout:auto"}

Una sovvenzione per un pubblico virtuale consente di accedere a un pubblico condiviso per riferimento senza spostare i relativi dati. Puoi quindi attivare il pubblico per inviare i dati alla destinazione selezionata.

Per informazioni dettagliate sulle concessioni e sui controlli del provider, vedere [Accesso al pubblico virtuale (concessioni di pubblico)](/help/guide/setup/virtual-audience-access.md).

## Prerequisiti {#prerequisites}

Prima di iniziare, verifica di disporre di:

* Un pubblico di tua proprietà o condiviso tramite una sovvenzione di prima parte (1P) qualificata.
* Una destinazione configurata che controlli e che supporta l&#39;attivazione diretta.
* Almeno una mappatura di campo con chiave di corrispondenza per la destinazione.

Per attivare un pubblico condiviso, verifica che la relativa sovvenzione attiva con ambito di connessione soddisfi le [condizioni di idoneità](#check-shared-audience-access). Utilizza l&#39;area di lavoro **[!UICONTROL Activation]**. Non hai bisogno di un progetto.

### Idoneità al pubblico condiviso {#check-shared-audience-access}

La sovvenzione deve soddisfare ogni condizione per supportare l&#39;attivazione diretta.

| Requisito | Condizione |
| --- | --- |
| Autorizzazione del pubblico | La sovvenzione include l&#39;autorizzazione all&#39;attivazione diretta. |
| Durata dell’accesso | La sovvenzione è attiva, a tempo indeterminato o entro l’intervallo di date specificato. |

{style="table-layout:auto"}

L&#39;autorizzazione **[!UICONTROL Crea nuovo pubblico]** separata consente di utilizzare un pubblico condiviso per la creazione di un pubblico di coorte. Non è necessaria questa autorizzazione per l&#39;attivazione diretta.

### Mappature dei campi di destinazione {#review-destination-field-mappings}

L&#39;attivazione diretta utilizza le mappature con chiave di corrispondenza configurate per la destinazione. Non hai selezionato i tasti di corrispondenza durante l&#39;attivazione.

Per configurare le destinazioni, vedi [panoramica delle destinazioni](../destinations/overview.md).

## Avvia attivazione diretta {#start-direct-activation}

Inizia da una destinazione configurata o dall’elenco dei tipi di pubblico attivati. Le destinazioni Adobe Experience Platform non supportano l’attivazione di prime parti.

### Inizia da una destinazione {#start-from-a-destination}

Per aprire il flusso di lavoro con una destinazione selezionata, inizia da tale destinazione configurata. Aprire innanzitutto l&#39;area di lavoro **[!UICONTROL Activation]** e selezionare **[!UICONTROL Destinations]**.

Quindi, seleziona **[!UICONTROL Attiva pubblico]** dalle azioni per la destinazione che desideri utilizzare.

Viene aperto il flusso di lavoro con la destinazione selezionata. Quindi continuare con [Configurare l&#39;attivazione](#configure-the-activation).

### Inizia da tipi di pubblico attivati {#start-from-activated-audiences}

Per scegliere una destinazione nel flusso di lavoro, inizia dall’elenco dei tipi di pubblico attivati. Apri innanzitutto l&#39;area di lavoro **[!UICONTROL Activation]** e seleziona **[!UICONTROL Tipi di pubblico attivati]**.

Quindi, avvia il flusso di lavoro selezionando **[!UICONTROL Attiva pubblico]** nella pagina o selezionando l&#39;icona Aggiungi (![Aggiungi un&#39;attivazione pubblico.](/help/assets/icons/plus.png)) e quindi **[!UICONTROL Attiva pubblico]**.

Il flusso di lavoro si apre senza una destinazione selezionata. Quindi continuare con [Configurare l&#39;attivazione](#configure-the-activation).

## Configurare l’attivazione {#configure-the-activation}

Seleziona un pubblico per attivazione dai tuoi tipi di pubblico o dai tipi di pubblico condivisi con te. Utilizza la destinazione preselezionata oppure scegli una destinazione configurata, se non è selezionata alcuna destinazione. Il flusso di lavoro applica le [mappature esistenti](#review-destination-field-mappings) configurate per tale destinazione.

Scegli quando eseguire l&#39;attivazione, quindi controlla il pubblico, la destinazione e la pianificazione selezionati prima dell&#39;invio.

## Modifiche di accesso ed esecuzioni pianificate {#access-changes-and-scheduled-runs}

Attiva un pubblico condiviso solo quando il provider concede l’accesso.

| Modifica dell’accesso | Effetto |
| --- | --- |
| La sovvenzione scade | Il sistema elabora ogni ora la scadenza. Il destinatario perde l’accesso al pubblico virtuale dopo l’elaborazione della scadenza. |
| Il provider revoca la sovvenzione | Il destinatario perde immediatamente l’accesso al pubblico virtuale. |
| Viene eseguita un&#39;attivazione pianificata | Il sistema controlla la sovvenzione. I tipi di pubblico con sovvenzioni revocate o scadute non sono idonei all’attivazione. |

{style="table-layout:auto"}

La scadenza o la revoca non rimuove i dati sul pubblico già consegnati a una destinazione.

## Passaggi successivi {#next-steps}

Dopo aver attivato i tipi di pubblico, utilizza queste guide per gestire le destinazioni o le connessioni dei collaboratori.

* [Configurare e gestire le destinazioni](/help/guide/destinations/manage-destinations.md)
* [Gestire le connessioni dei collaboratori](/help/guide/connect/manage-connections.md)
