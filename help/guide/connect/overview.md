---
title: Panoramica delle connessioni
description: Scopri le connessioni in Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 5c08738cdc8e1e208203ee1f9a1cf1891b5b07cb
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 0%

---

# Panoramica delle connessioni

{{limited-availability-release-note}}

Prima che i collaboratori possano lavorare insieme sulle campagne, devono stabilire una connessione. Questa connessione consente loro di attivare tipi di pubblico, creare progetti ed eseguire rapporti sulle prestazioni della campagna.

Le connessioni vengono stabilite in base al modello di collaborazione scelto. Collaboration supporta tre pattern di collaborazione chiave: da inserzionista a editore, da brand a brand e da inserzionista a piattaforma pubblicitaria. Per ulteriori informazioni su questi pattern, consulta la guida [modelli di collaborazione](/help/guide/overview/collaboration-patterns.md).

Per informazioni su come stabilire una connessione, leggere la sezione seguente corrispondente al proprio modello di collaborazione:

- [Connessione inserzionista-editore](#advertiser-to-publisher-connection)
- [Connessione brand-to-brand](#brand-to-brand-connection)
- [Connessione inserzionista a piattaforma pubblicitaria](#advertiser-to-advertising-platform-connection)

## Connessione inserzionista-editore {#advertiser-to-publisher-connection}

![Diagramma di alto livello del processo di connessione inserzionista-editore.](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

Nel modello da inserzionista a editore, un inserzionista individua un editore con cui desidera collaborare tramite l&#39;area di lavoro **[!UICONTROL Discover publishers]** e invia un invito alla connessione. L’editore rivede quindi l’invito e lo accetta, consentendo all’inserzionista di proporre le impostazioni di connessione. Una volta che l&#39;editore accetta le impostazioni di connessione, la connessione viene stabilita ed entrambi i collaboratori possono iniziare a lavorare insieme ai progetti.

### Panoramica di alto livello

Per stabilire una connessione tra un inserzionista e un editore, sono necessari i seguenti passaggi:

1. [Individua editori](./discover-collaborators.md): l&#39;inserzionista identifica i potenziali editori con cui collaborare.
2. [Invia invito](./establishing-connections.md#send-invite): l&#39;inserzionista invia un invito di connessione all&#39;editore selezionato.
3. [Accetta invito](./establishing-connections.md#accept-invite): l&#39;editore rivede e accetta l&#39;invito.
4. [Configura impostazioni di connessione](./establishing-connections.md#configure-connection-settings): l&#39;inserzionista configura le impostazioni di connessione e le invia all&#39;editore per la revisione.
5. [Conferma impostazioni di connessione](./establishing-connections.md#review-connection-settings): l&#39;editore esamina le impostazioni di connessione e le accetta o le rifiuta. Se accettata, la connessione viene stabilita. Se viene rifiutato, l’editore può fornire un feedback per le revisioni al di fuori del prodotto. L&#39;inserzionista può quindi rivedere le impostazioni e inviarle nuovamente per la revisione.

Una volta accettate le impostazioni di connessione, la connessione viene stabilita e i collaboratori sono pronti a [creare un progetto](/help/guide/collaborate/manage-projects.md#create-project) per iniziare a collaborare alle campagne.

## Connessione brand-to-brand {#brand-to-brand-connection}

![Diagramma di alto livello del processo di connessione brand-to-brand.](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>Il termine **brand** viene utilizzato per indicare un&#39;azienda o un brand al di fuori di Collaboration. Il termine **collaboratore** fa riferimento a qualsiasi account che può creare una connessione in Collaboration, indipendentemente dal fatto che sia un inserzionista o un editore.

Nel modello brand-to-brand, due brand che hanno comunicato al di fuori del prodotto possono connettersi direttamente in Collaboration utilizzando un [invito di connessione privato](#private-connection-invite). Un marchio può essere un inserzionista o un editore. Questo modello è particolarmente utile per i marchi che potrebbero non rientrare nel modello tradizionale inserzionista-editore, ad esempio due inserzionisti o due editori.

Per iniziare, un collaboratore invia un invito di connessione privato a un altro collaboratore. Il destinatario rivede l’invito e lo accetta, consentendo al proprietario di proporre le impostazioni di connessione. Una volta che il destinatario accetta le impostazioni di connessione, la connessione viene stabilita ed entrambi i collaboratori possono iniziare a lavorare insieme ai progetti.

### Panoramica di alto livello

>[!TIP]
>
>Quando si parla del processo di connessione, verrà fatta una distinzione tra **proprietario** e **destinatario**. Il proprietario è il collaboratore che avvia la connessione inviando l&#39;invito, mentre il destinatario è il collaboratore che riceve e rivede l&#39;invito.

Il processo di connessione tra due marchi prevede diversi passaggi. Prima di avviare il processo di connessione, è necessario soddisfare alcuni prerequisiti:

1. Due marchi comunicano al di fuori del prodotto per discutere il potenziale collegamento.
1. I marchi [creano account](/help/guide/setup/onboard-account.md) in Collaboration, se non lo hanno già fatto, assicurandosi di selezionare il tipo di ruolo appropriato (inserzionista o editore).

Una volta soddisfatti i prerequisiti, il processo di connessione può iniziare. Le seguenti fasi delineano il processo:

1. [Invia invito di connessione privata](./establishing-connections.md#private-connection-invite): un collaboratore invia un invito di connessione privata a un altro collaboratore.
2. [Accetta invito di connessione privata](./establishing-connections.md#accept-invite): il destinatario rivede e accetta l&#39;invito di connessione privata.
3. [Configura impostazioni di connessione](./establishing-connections.md#configure-connection-settings): il proprietario configura le impostazioni di connessione e le invia al destinatario per la revisione e l&#39;accettazione.
4. [Conferma impostazioni di connessione](./establishing-connections.md#review-connection-settings): il destinatario esamina le impostazioni di connessione e le accetta o le rifiuta.

Una volta accettate le impostazioni di connessione, la connessione viene stabilita e i collaboratori sono pronti a [creare un progetto](/help/guide/collaborate/manage-projects.md#create-project) per iniziare a collaborare alle campagne.

## Connessione inserzionista a piattaforma pubblicitaria {#advertiser-to-advertising-platform-connection}

Il processo di connessione tra inserzionisti e piattaforme pubblicitarie consente agli inserzionisti di connettersi con piattaforme pubblicitarie di terze parti, come Amazon Marketing Cloud (AMC), per migliorare le loro funzionalità di marketing.

### Panoramica di alto livello

Il processo di connessione tra un inserzionista e una piattaforma pubblicitaria prevede diversi passaggi. Prima di iniziare il processo di connessione, assicurati di disporre di un account attivo con la piattaforma pubblicitaria e di disporre dell’approvazione per l’utilizzo dei relativi servizi. I passaggi seguenti descrivono il processo di connessione:

1. [Scopri le piattaforme pubblicitarie](./discover-collaborators.md): l&#39;inserzionista identifica le potenziali piattaforme pubblicitarie con cui collaborare.
2. [Connetti alla piattaforma pubblicitaria](./advertising-platforms/overview.md#advertising-platforms-overview): l&#39;inserzionista avvia il processo di connessione selezionando la piattaforma pubblicitaria con cui desidera connettersi e segue le istruzioni per l&#39;autenticazione e l&#39;autorizzazione della connessione.
