---
title: Flusso di lavoro end-to-end
description: Comprendi il flusso di lavoro end-to-end dell’utilizzo di Real-Time CDP Collaboration in base al tuo modello di collaborazione.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
TQID: https://experienceleague.adobe.com/9edtg5tMbnB3BrdLrDkcHQ-AjBNOqMFGojAja3NCwCs
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 4dba099a1bf484d9e2dfa71d5ad21a1ac076d794
workflow-type: tm+mt
source-wordcount: 1738
ht-degree: 0%

---

# Flusso di lavoro end-to-end

{{limited-availability-release-note}}

Ad Adobe Real-Time CDP Collaboration, il flusso di lavoro end-to-end varia in base al modello di collaborazione scelto. Il flusso di lavoro illustra i passaggi necessari per la configurazione e l&#39;esecuzione di un progetto di collaborazione, dalla creazione di account e di tipi di pubblico, alla creazione di connessioni e alla creazione di progetti. Comprendere questo flusso di lavoro è essenziale per sfruttare in modo efficace le funzionalità della piattaforma per raggiungere i tuoi obiettivi di marketing.

## Introduzione

Prima di iniziare, assicurati di avere una solida comprensione di questi concetti chiave:

- **Modelli Collaboration**: questi modelli definiscono il modo in cui i collaboratori collaborano. Esistono cinque modelli distinti:
  - [inserzionista-editore](./collaboration-patterns.md#advertiser-to-publisher)
  - [brand-to-brand](./collaboration-patterns.md#brand-to-brand)
  - [partner inserzionista-dati](./collaboration-patterns.md#advertiser-to-data-partner)
  - [da agenzia a editore](./collaboration-patterns.md#agency-to-publisher)
  - [piattaforma da inserzionista a agente](./collaboration-patterns.md#advertiser-to-agency-platform)
- **Ruoli account**: i ruoli account determinano le funzionalità all&#39;interno della piattaforma. Devono allinearsi agli obiettivi, al marchio e agli obiettivi della tua organizzazione. Sono disponibili quattro ruoli account: [inserzionista](./roles.md#advertiser), [editore](./roles.md#publisher), [agenzia](./roles.md#agency) e [partner dati](./roles.md#data-partner).
- **Casi d&#39;uso**: i casi d&#39;uso definiscono i modi in cui puoi sfruttare Collaboration per raggiungere i tuoi obiettivi di marketing. Esistono tre casi di utilizzo di collaborazione: [Discover](./use-cases.md#discover), [Activate](./use-cases.md#activate) e [Measure](./use-cases.md#measure).

Questa guida utilizza tre collaboratori fittizi per illustrare il flusso di lavoro end-to-end:

- **[!UICONTROL Luma]**: un marchio di abbigliamento sportivo. Sono un inserzionista che vuole raggiungere tipi di pubblico specifici tramite campagne di marketing mirate.
- **[!UICONTROL Tubo TV]**: provider di streaming digitale. Sono un editore che fornisce dati sul pubblico per l’utilizzo da parte degli inserzionisti.
- **[!UICONTROL Abbigliamento adatto]**: altra marca di abbigliamento sportivo. Si tratta di un secondo inserzionista che desidera collaborare per condividere i dati sul pubblico e le informazioni per migliorare le attività di marketing.
- **[!UICONTROL Agenzia99]**: agenzia di comunicazione. Gestiscono più account client all’interno della propria area di lavoro e si connettono con editori e inserzionisti.
- **[!UICONTROL DataM8]**: provider di dati di terze parti. Forniscono dati sul pubblico per l’utilizzo da parte degli inserzionisti.
- **[!UICONTROL Holdco]**: piattaforma di servizi di marketing e pubblicitari per società holding utilizzata da team di agenzie interne per gestire le campagne dei clienti.

## Flusso di lavoro da inserzionista a editore {#advertiser-to-publisher-workflow}

[!UICONTROL Luma], una società di vendita al dettaglio di atletica, desidera stabilire una connessione con [!UICONTROL TV Tube], un provider di streaming digitale, per raggiungere tipi di pubblico specifici tramite campagne di marketing mirate.

Per iniziare, [!UICONTROL Luma] deve [creare un account](../setup/onboard-account.md) con il ruolo di inserzionista, mentre [!UICONTROL TV Tube] crea un account con il ruolo di editore.

Dopo aver stabilito i propri account, sia [!UICONTROL Luma] che [!UICONTROL TV Tube] devono [creare una connessione dati e i tipi di pubblico di origine](../setup/onboard-audiences.md). Solo [!UICONTROL TV Tube] attiverà i tipi di pubblico per le campagne di marketing, pertanto è necessario [configurare una destinazione](../destinations/manage-destinations.md).

Una volta che entrambi i collaboratori hanno configurato i loro account, sono pronti a [creare una connessione](../connect/establishing-connections.md) all&#39;interno della piattaforma. [!UICONTROL Luma] utilizza la funzionalità [individua collaboratori](../connect/discover-collaborators.md) per trovare [!UICONTROL TV Tube] e avviare una richiesta di connessione. Dopo che [!UICONTROL TV Tube] ha accettato la richiesta di connessione, [!UICONTROL Luma] configura le impostazioni di connessione per definire la modalità di collaborazione. [!UICONTROL TV Tube] accetta la richiesta di connessione per stabilire un collegamento sicuro tra i due marchi.

Una volta stabilita la connessione, [!UICONTROL Luma] [crea un progetto](../collaborate/manage-projects.md) per avviare la collaborazione con [!UICONTROL TV Tube]. Durante la configurazione del progetto, scelgono i casi di utilizzo di collaborazione più adatti ai loro obiettivi: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md) e [Measure](../collaborate/measure.md).

[!UICONTROL Luma] sfrutta il caso d&#39;uso [Discover](../collaborate/discover.md) per ottenere informazioni approfondite sui dati del pubblico di [!UICONTROL TV Tube]. Una volta che [!UICONTROL Luma] ha identificato i segmenti del pubblico di destinazione, [attiva](../collaborate/activate.md) questi tipi di pubblico.

Dopo aver attivato i tipi di pubblico, [!UICONTROL TV Tube] esegue campagne di marketing mirate e carica i dati in [Misura](../collaborate/measure.md) i risultati per valutare l&#39;efficacia della campagna.

## Flusso di lavoro da marchio a marchio {#brand-to-brand-workflow}

[!UICONTROL Fit Apparel], un marchio di abbigliamento sportivo, desidera collaborare con [!UICONTROL Luma], un altro marchio di abbigliamento sportivo, per condividere dati e approfondimenti sul pubblico per attività di marketing avanzate.

Dopo aver stabilito i propri account, sia [!UICONTROL Adatta abbigliamento] che [!UICONTROL Luma] devono [creare una connessione dati e i tipi di pubblico di origine](../setup/onboard-audiences.md). Sia [!UICONTROL Adatta abbigliamento] che [!UICONTROL Luma] attiveranno i tipi di pubblico per le campagne di marketing, pertanto entrambi devono [configurare una destinazione](../destinations/manage-destinations.md).

Dopo aver ottenuto i tipi di pubblico, [!UICONTROL Adatta abbigliamento] e [!UICONTROL Luma] [formano una connessione](../connect/establishing-connections.md) all&#39;interno della piattaforma per condividere in modo sicuro i dati sul pubblico. A tale scopo, è necessario utilizzare la funzionalità [invito alla connessione privata](../connect/establishing-connections.md#private-connection-invite). [!UICONTROL Luma] condivide il proprio codice di connessione con [!UICONTROL Adatta abbigliamento], che lo utilizza per avviare una richiesta di connessione. Dopo che [!UICONTROL Luma] ha accettato la richiesta di connessione, [!UICONTROL Adatta abbigliamento] configura le impostazioni di connessione per definire la modalità di collaborazione. Nella configurazione, [!UICONTROL Adatta abbigliamento] specifica che entrambi i collaboratori possono attivare i tipi di pubblico per le campagne di marketing. Per completare la connessione, [!UICONTROL Luma] accetta la richiesta di stabilire un collegamento sicuro tra i due brand.

Una volta stabilita la connessione, [!UICONTROL Adatta abbigliamento] [crea un progetto](../collaborate/manage-projects.md) per avviare la collaborazione con [!UICONTROL Luma]. Durante la configurazione del progetto, scelgono i casi di utilizzo di collaborazione più adatti ai loro obiettivi: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md) e [Measure](../collaborate/measure.md).

Sia [!UICONTROL Abbigliamento adatto] che [!UICONTROL Luma] possono utilizzare il caso d&#39;uso [Discover](../collaborate/discover.md) per ottenere informazioni approfondite sui dati del pubblico dell&#39;altra parte. Dopo aver identificato segmenti di pubblico importanti, [Attiva](../collaborate/activate.md) i tipi di pubblico scelti per le campagne di marketing.

Infine, dopo aver eseguito le campagne, entrambi i brand caricano i dati in [Misura](../collaborate/measure.md) i risultati e valutano l&#39;efficacia della loro collaborazione.

## Flusso di lavoro da inserzionista a piattaforma pubblicitaria {#advertiser-to-advertising-platform-workflow}

[!UICONTROL Luma], un&#39;azienda di vendita al dettaglio sportiva, desidera connettersi con [!DNL Amazon Marketing Cloud] ([!DNL AMC]) per migliorare le proprie funzionalità di marketing sfruttando gli strumenti di risoluzione identità e targeting di [!DNL AMC]. Luma dispone già di un account [!DNL Amazon Advertising] attivo ed è approvato per l&#39;utilizzo di [!DNL AMC].

Per iniziare, [!UICONTROL Luma] deve [creare un account](../setup/onboard-account.md) con il ruolo inserzionista. Dopo aver stabilito il proprio account, [!UICONTROL Luma] deve [creare una connessione dati e i tipi di pubblico di origine](../setup/onboard-audiences.md). Poiché [!UICONTROL Luma] attiverà i tipi di pubblico per le campagne di marketing, è necessario [configurare una destinazione](../destinations/manage-destinations.md).

Una volta che [!UICONTROL Luma] ha configurato il suo account, è possibile [creare una connessione](../connect/establishing-connections.md) con [!DNL AMC] nella piattaforma. [!UICONTROL Luma] utilizza la funzionalità [individua collaboratori](../connect/discover-collaborators.md) per trovare [!UICONTROL Amazon Marketing Cloud] e [avviare una richiesta di connessione](../connect/advertising-platforms/amc.md). Dopo l&#39;autenticazione e l&#39;autorizzazione della connessione tramite la pagina di accesso [!DNL Amazon], la connessione con [!DNL AMC] viene stabilita.

Una volta stabilita la connessione, [!UICONTROL Luma] [crea un progetto](../collaborate/manage-projects.md) per avviare la collaborazione con [!DNL AMC]. Le impostazioni di connessione, inclusi i casi di utilizzo, sono preconfigurate a seconda della piattaforma pubblicitaria. Per [!DNL AMC], il caso d&#39;uso disponibile è [Discover](../collaborate/advertising-platforms/amc.md#discover).

[!UICONTROL Luma] sfrutta il caso d&#39;uso [Discover](../collaborate/advertising-platforms/amc.md#discover) per ottenere approfondimenti e dati sul pubblico da [!DNL AMC]. Utilizzando queste informazioni, [!UICONTROL Luma] può ottimizzare le strategie di marketing e migliorare l&#39;efficacia della campagna.

## Flusso di lavoro da inserzionista a partner dati {#advertiser-to-data-partner-workflow}

[!UICONTROL Luma], una società di vendita al dettaglio di atletica leggera, desidera collaborare con [!UICONTROL DataM8], un provider di dati di terze parti, per arricchire i profili dei clienti e migliorare il targeting del pubblico.

Per iniziare, [!UICONTROL Luma] deve [creare un account](../setup/onboard-account.md) con il ruolo inserzionista, mentre [!UICONTROL DataM8] crea un account con il ruolo partner dati.

Dopo aver stabilito i propri account, sia [!UICONTROL Luma] che [!UICONTROL DataM8] devono [creare una connessione dati e i tipi di pubblico di origine](../setup/onboard-audiences.md). Entrambi i collaboratori possono attivare i tipi di pubblico per le campagne di marketing, pertanto devono [configurare una destinazione](../destinations/manage-destinations.md).

Una volta che entrambi i collaboratori hanno configurato i loro account, sono pronti a [creare una connessione](../connect/establishing-connections.md) all&#39;interno della piattaforma. [!UICONTROL Luma] utilizza la funzionalità [individua collaboratori](../collaborate/discover.md) per trovare [!UICONTROL DataM8] e avviare una richiesta di connessione. Dopo che [!UICONTROL DataM8] ha accettato la richiesta di connessione, [!UICONTROL Luma] configura le impostazioni di connessione per definire la modalità di collaborazione. [!UICONTROL DataM8] accetta la richiesta di connessione per stabilire un collegamento sicuro tra i due collaboratori.

Una volta stabilita la connessione, [!UICONTROL Luma] [crea un progetto](../collaborate/manage-projects.md) per avviare la collaborazione con [!UICONTROL DataM8]. Durante la configurazione del progetto, scelgono i casi di utilizzo di collaborazione più adatti ai loro obiettivi: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md) e [Measure](../collaborate/measure.md).

[!UICONTROL Luma] sfrutta il caso d&#39;uso [Discover](../collaborate/discover.md) per ottenere informazioni approfondite sui dati del pubblico di [!UICONTROL DataM8]. Una volta che [!UICONTROL Luma] ha identificato i segmenti del pubblico di destinazione, [attiva](../collaborate/activate.md) questi tipi di pubblico.

[!UICONTROL DataM8] può anche [attivare](../collaborate/activate.md) i propri tipi di pubblico per [!UICONTROL Luma]. [!UICONTROL Luma] utilizza queste funzionalità per aggiungere attributi di terze parti ai profili cliente e analizzare la composizione del pubblico. Con i dati arricchiti disponibili direttamente nel relativo CDP, [!UICONTROL Luma] può creare tipi di pubblico più precisi e attivarli in destinazioni di media a pagamento senza spostare i dati al di fuori dell&#39;ambiente governato.

## Flusso di lavoro da agenzia a editore {#agency-to-publisher-workflow}

[!UICONTROL Agency99], un&#39;agenzia di media, desidera collaborare con [!UICONTROL TV Tube], un provider di streaming digitale, per raggiungere tipi di pubblico specifici tramite campagne di marketing mirate.

Per iniziare, [!UICONTROL Agency99] deve [creare un account](../setup/onboard-account.md) con il ruolo di agenzia, mentre [!UICONTROL TV Tube] crea un account con il ruolo di editore.

Dopo aver stabilito i propri account, sia [!UICONTROL Agency99] che [!UICONTROL TV Tube] devono [creare una connessione dati e un pubblico di origine](../setup/onboard-audiences.md). [!UICONTROL Agency99] configurerà account secondari client e dati client di origine nella propria area di lavoro. Solo [!UICONTROL TV Tube] attiverà i tipi di pubblico per le campagne di marketing, pertanto è necessario [configurare una destinazione](../destinations/manage-destinations.md).

Una volta che entrambi i collaboratori hanno configurato i loro account, sono pronti a [creare una connessione](../connect/establishing-connections.md) all&#39;interno della piattaforma. [!UICONTROL Agency99] utilizza la funzionalità [individua collaboratori](../collaborate/discover.md) per trovare [!UICONTROL TV Tube] e avviare una richiesta di connessione. [!UICONTROL Agency99] eseguirà questa operazione per uno o più client che desiderano collaborare con [!UICONTROL TV Tube]. Dopo che [!UICONTROL TV Tube] ha accettato le richieste di connessione, [!UICONTROL Agency99] configura le impostazioni di connessione per definire la modalità di collaborazione. [!UICONTROL TV Tube] accetta le richieste di connessione per stabilire un collegamento sicuro tra i due marchi.

Una volta stabilita la connessione, [!UICONTROL Agency99] [crea un progetto](../collaborate/manage-projects.md) per avviare la collaborazione con [!UICONTROL TV Tube] in ogni account secondario del client. Durante la configurazione del progetto, scelgono i casi di utilizzo di collaborazione più adatti ai loro obiettivi: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md) e [Measure](../collaborate/measure.md).

[!UICONTROL Agency99] sfrutta il caso d&#39;uso [Discover](../collaborate/discover.md) per ottenere informazioni approfondite sui dati del pubblico di [!UICONTROL TV Tube]. Una volta che [!UICONTROL Agency99] ha identificato i segmenti del pubblico di destinazione, [attiva](../collaborate/activate.md) questi tipi di pubblico.

Dopo aver attivato i tipi di pubblico, [!UICONTROL TV Tube] esegue campagne di marketing mirate e carica i dati in [misura](../collaborate/measure.md) i risultati per valutare l&#39;efficacia della campagna.

## Flusso di lavoro da inserzionista a agenzia {#advertiser-to-agency-platform-workflow}

[!UICONTROL Luma], una società di vendita al dettaglio di atletica leggera, desidera collaborare con [!UICONTROL Holdco], una piattaforma di agenzia, per condividere dati e ricevere informazioni multimediali a pagamento.

Per iniziare, [!UICONTROL Luma] deve [creare un account](../setup/onboard-account.md) con il ruolo inserzionista, mentre [!UICONTROL Holdco] crea un account con il ruolo di agenzia. 

Dopo aver stabilito i propri account, sia [!UICONTROL Luma] che [!UICONTROL Holdco] devono [creare una connessione dati e i tipi di pubblico di origine](../setup/onboard-audiences.md). Entrambi i collaboratori possono attivare i tipi di pubblico per le campagne di marketing, pertanto devono [configurare una destinazione](../destinations/manage-destinations.md). 

Una volta che entrambi i collaboratori hanno configurato i loro account, sono pronti a [creare una connessione](../connect/establishing-connections.md) all&#39;interno della piattaforma. [!UICONTROL Luma] utilizza la funzionalità [individua collaboratori](../collaborate/discover.md) per trovare [!UICONTROL Holdco] e avviare una richiesta di connessione. Dopo che [!UICONTROL Holdco] ha accettato la richiesta di connessione, [!UICONTROL Luma] configura le impostazioni di connessione per definire la modalità di collaborazione.

[!UICONTROL Holdco] accetta la richiesta di connessione per stabilire un collegamento sicuro tra i due collaboratori.

Una volta stabilita la connessione, [!UICONTROL Luma] [crea un progetto](../collaborate/manage-projects.md) per avviare la collaborazione con [!UICONTROL Holdco]. Durante la configurazione del progetto, scelgono i casi di utilizzo di collaborazione più adatti ai loro obiettivi: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md) e [Measure](../collaborate/measure.md).

[!UICONTROL Luma] sfrutta il caso d&#39;uso [Discover](../collaborate/discover.md) per ottenere informazioni approfondite sui dati del pubblico di [!UICONTROL Holdco]. Una volta che [!UICONTROL Luma] ha identificato i segmenti del pubblico di destinazione, [attiva](../collaborate/activate.md) questi tipi di pubblico.

[!UICONTROL Holdco] può anche [attivare](../collaborate/activate.md) il proprio pubblico per [!UICONTROL Luma]. [!UICONTROL Luma] utilizza queste funzionalità per ricevere informazioni multimediali a pagamento dalle campagne gestite dall&#39;agenzia per approfondimenti, aggiunte di profili CDP e orchestrazione multimediale di proprietà.
