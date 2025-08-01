---
title: Flusso di lavoro end-to-end
description: Comprendi il flusso di lavoro end-to-end dell’utilizzo di Real-Time CDP Collaboration in base al tuo modello di collaborazione.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
source-git-commit: 8745d6d8da389b552af3da6612bf693230dfb538
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 0%

---

# Flusso di lavoro end-to-end

{{limited-availability-release-note}}

Ad Adobe Real-Time CDP Collaboration, il flusso di lavoro end-to-end varia in base al modello di collaborazione scelto. Il flusso di lavoro illustra i passaggi necessari per la configurazione e l&#39;esecuzione di un progetto di collaborazione, dalla creazione di account e di tipi di pubblico, alla creazione di connessioni e alla creazione di progetti. Comprendere questo flusso di lavoro è essenziale per sfruttare in modo efficace le funzionalità della piattaforma per raggiungere i tuoi obiettivi di marketing.

## Introduzione

Prima di iniziare, assicurati di avere una solida comprensione di questi concetti chiave:

- **Modelli Collaboration**: questi modelli definiscono il modo in cui i collaboratori collaborano. Esistono due modelli distinti: [inserzionista-editore](./collaboration-patterns.md#advertiser-to-publisher) e [da marchio a marchio](./collaboration-patterns.md#brand-to-brand).
- **Ruoli account**: i ruoli account determinano le funzionalità all&#39;interno della piattaforma. Devono allinearsi agli obiettivi, al marchio e agli obiettivi della tua organizzazione. Sono disponibili due ruoli account: [inserzionista](./roles.md#advertiser) e [editore](./roles.md#publisher).
- **Casi d&#39;uso**: i casi d&#39;uso definiscono i modi in cui puoi sfruttare Collaboration per raggiungere i tuoi obiettivi di marketing. Esistono tre casi di utilizzo di collaborazione: [Discover](./use-cases.md#discover), [Activate](./use-cases.md#activate) e [Measure](./use-cases.md#measure).

Questa guida utilizza tre collaboratori fittizi per illustrare il flusso di lavoro end-to-end:

- **[!UICONTROL Luma]**: un marchio di abbigliamento sportivo. Sono un inserzionista che vuole raggiungere tipi di pubblico specifici tramite campagne di marketing mirate.
- **[!UICONTROL Tubo TV]**: provider di streaming digitale. Sono un editore che fornisce dati sul pubblico per l’utilizzo da parte degli inserzionisti.
- **[!UICONTROL Abbigliamento adatto]**: altra marca di abbigliamento sportivo. Si tratta di un secondo inserzionista che desidera collaborare per condividere i dati sul pubblico e le informazioni per migliorare le attività di marketing.

## Flusso di lavoro da inserzionista a editore {#advertiser-to-publisher-workflow}

[!UICONTROL Luma], una società di vendita al dettaglio di atletica, desidera stabilire una connessione con [!UICONTROL TV Tube], un provider di streaming digitale, per raggiungere tipi di pubblico specifici tramite campagne di marketing mirate.

Per iniziare, [!UICONTROL Luma] deve [creare un account](../setup/onboard-account.md) con il ruolo di inserzionista, mentre [!UICONTROL TV Tube] crea un account con il ruolo di editore.

Dopo aver stabilito i propri account, sia [!UICONTROL Luma] che [!UICONTROL TV Tube] devono [creare una connessione dati e i tipi di pubblico di origine](../setup/onboard-audiences.md). Solo [!UICONTROL TV Tube] attiverà i tipi di pubblico per le campagne di marketing, pertanto è necessario [configurare una destinazione](../setup/manage-destinations.md).

Una volta che entrambi i collaboratori hanno configurato i loro account, sono pronti a [creare una connessione](../connect/establishing-connections.md) all&#39;interno della piattaforma. [!UICONTROL Luma] utilizza la funzionalità [scopri editori](../connect/discover-publishers.md) per trovare [!UICONTROL TV Tube] e avviare una richiesta di connessione. Dopo che [!UICONTROL TV Tube] ha accettato la richiesta di connessione, [!UICONTROL Luma] configura le impostazioni di connessione per definire la modalità di collaborazione. [!UICONTROL TV Tube] accetta la richiesta di connessione per stabilire un collegamento sicuro tra i due marchi.

Una volta stabilita la connessione, [!UICONTROL Luma] [crea un progetto](../collaborate/manage-projects.md) per avviare la collaborazione con [!UICONTROL TV Tube]. Durante la configurazione del progetto, scelgono i casi di utilizzo di collaborazione più adatti ai loro obiettivi: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md) e [Measure](../collaborate/measure.md).

[!UICONTROL Luma] sfrutta il caso d&#39;uso [Discover](../collaborate/discover.md) per ottenere informazioni approfondite sui dati del pubblico di [!UICONTROL TV Tube]. Una volta che [!UICONTROL Luma] ha identificato i segmenti del pubblico di destinazione, [attiva](../collaborate/activate.md) questi tipi di pubblico.

Dopo aver attivato i tipi di pubblico, [!UICONTROL TV Tube] esegue campagne di marketing mirate e carica i dati in [Misura](../collaborate/measure.md) i risultati per valutare l&#39;efficacia della campagna.

## Flusso di lavoro da marchio a marchio {#brand-to-brand-workflow}

[!UICONTROL Fit Apparel], un marchio di abbigliamento sportivo, desidera collaborare con [!UICONTROL Luma], un altro marchio di abbigliamento sportivo, per condividere dati e approfondimenti sul pubblico per attività di marketing avanzate.

Dopo aver stabilito i propri account, sia [!UICONTROL Adatta abbigliamento] che [!UICONTROL Luma] devono [creare una connessione dati e i tipi di pubblico di origine](../setup/onboard-audiences.md). Sia [!UICONTROL Adatta abbigliamento] che [!UICONTROL Luma] attiveranno i tipi di pubblico per le campagne di marketing, pertanto entrambi devono [configurare una destinazione](../setup/manage-destinations.md).

Dopo aver ottenuto i tipi di pubblico, [!UICONTROL Adatta abbigliamento] e [!UICONTROL Luma] [formano una connessione](../connect/establishing-connections.md) all&#39;interno della piattaforma per condividere in modo sicuro i dati sul pubblico. A tale scopo, è necessario utilizzare la funzionalità [invito alla connessione privata](../connect/establishing-connections.md#private-connection-invite). [!UICONTROL Luma] condivide il proprio codice di connessione con [!UICONTROL Adatta abbigliamento], che lo utilizza per avviare una richiesta di connessione. Dopo che [!UICONTROL Luma] ha accettato la richiesta di connessione, [!UICONTROL Adatta abbigliamento] configura le impostazioni di connessione per definire la modalità di collaborazione. Nella configurazione, [!UICONTROL Adatta abbigliamento] specifica che entrambi i collaboratori possono attivare i tipi di pubblico per le campagne di marketing. Per completare la connessione, [!UICONTROL Luma] accetta la richiesta di stabilire un collegamento sicuro tra i due brand.

Una volta stabilita la connessione, [!UICONTROL Adatta abbigliamento] [crea un progetto](../collaborate/manage-projects.md) per avviare la collaborazione con [!UICONTROL Luma]. Durante la configurazione del progetto, scelgono i casi di utilizzo di collaborazione più adatti ai loro obiettivi: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md) e [Measure](../collaborate/measure.md).

Sia [!UICONTROL Abbigliamento adatto] che [!UICONTROL Luma] possono utilizzare il caso d&#39;uso [Discover](../collaborate/discover.md) per ottenere informazioni approfondite sui dati del pubblico dell&#39;altra parte. Dopo aver identificato segmenti di pubblico importanti, [Attiva](../collaborate/activate.md) i tipi di pubblico scelti per le campagne di marketing.

Infine, dopo aver eseguito le campagne, entrambi i brand caricano i dati in [Misura](../collaborate/measure.md) i risultati e valutano l&#39;efficacia della loro collaborazione.
