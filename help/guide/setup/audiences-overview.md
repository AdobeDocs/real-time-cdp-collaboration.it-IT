---
title: Panoramica sui tipi di pubblico
description: Scopri i tipi di pubblico in Real-Time CDP Collaboration, compreso da dove possono provenire.
audience: admin, publisher
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 160bd29d89d1ce828476d68e917e0271d0852eb6
workflow-type: tm+mt
source-wordcount: 707
ht-degree: 3%

---

# Panoramica sui tipi di pubblico

{{limited-availability-release-note}}

Ad Adobe Real-Time CDP Collaboration, i tipi di pubblico sono gruppi di utenti o clienti inseriti in Collaboration. Dopo la determinazione dell’origine, puoi utilizzare i tipi di pubblico per scoprire la sovrapposizione con i collaboratori, attivare i tipi di pubblico e misurare le prestazioni della campagna. Puoi creare tipi di pubblico da diversi tipi di origine, tra cui Adobe Experience Platform, sistemi di archiviazione e condivisione cloud e flussi di lavoro per il caricamento di file, a seconda di dove si trovano già i dati sul pubblico.

## Operazioni possibili con i tipi di pubblico {#audiences-in-collaboration}

Una volta originato in Collaboration, il pubblico diventa disponibile per l’utilizzo nei flussi di lavoro di collaborazione supportati.

Utilizza i tipi di pubblico in Collaboration per:

* Confrontare il pubblico con i tipi di pubblico di collaboratori
* Identificare sovrapposizioni e opportunità
* Attiva tipi di pubblico
* Misurare i risultati e le prestazioni della campagna
* Gestire la visibilità del pubblico e le impostazioni correlate

## Adattamento dei tipi di pubblico a Collaboration {#conceptual-diagram}

>[!NOTE]
>
> Il diagramma seguente fornisce una visualizzazione di alto livello del modo in cui i tipi di pubblico di origine si adattano a Collaboration e vengono utilizzati nei progetti.

```text
Source → Data connection → Audience → Project
                                         │
                          ┌──────────────┼──────────────┐
                          ▼              ▼              ▼
                      Discover       Activate       Measure
                                         │
                                         ▼
                                    Destination
```

## Concetti principali {#core-concepts}

I concetti seguenti descrivono gli oggetti chiave coinvolti nell’audience sourcing e nei flussi di lavoro di collaborazione.

**Source**\
Il sistema o la posizione da cui provengono i dati sul pubblico, ad esempio Adobe Experience Platform, una posizione di archiviazione cloud o un caricamento di file.

**Connessione dati**\
La connessione configurata che Collaboration utilizza per accedere ai dati del pubblico da un’origine. Una connessione dati include dettagli di configurazione specifici dell&#39;origine, ad esempio autenticazione, mappatura campi e pianificazione.

**Pubblico**\
Un gruppo di utenti o clienti che è stato originato in Collaboration ed è disponibile per l’utilizzo nei progetti.

**Connessione**\
La relazione di collaborazione tra la tua organizzazione e un’altra organizzazione.

**Progetto**\
L’area di lavoro in cui i collaboratori utilizzano insieme i tipi di pubblico per i casi di utilizzo supportati, ad esempio individuazione, attivazione e misurazione.

**Destinazione**\
La piattaforma o il sistema esterno in cui vengono inviati i tipi di pubblico attivati.

**Corrispondenza chiavi**
Identificatori utilizzati da Collaboration per abbinare i record di set di dati e collaboratori. Le chiavi di corrispondenza supportano flussi di lavoro quali la sovrapposizione di tipi di pubblico, l’attivazione e la misurazione.

## Ciclo di vita del pubblico {#audience-lifecycle}

In Collaboration i tipi di pubblico vengono originati tramite connessioni dati, gestiti in **[!UICONTROL Configurazione]** e utilizzati in progetti per casi di utilizzo supportati.

1. **Tipi di pubblico di Source**: inserisci i dati del pubblico in Collaboration tramite una connessione dati.
2. **Gestione tipi di pubblico**: rivedi e gestisci i dettagli, la visibilità e le impostazioni correlate del pubblico.
3. **Utilizza i tipi di pubblico nei progetti**: utilizza i tipi di pubblico di origine nei progetti per i casi d&#39;uso supportati, tra cui **Scopri**, **Attiva** e **Misura**.

Non tutti i tipi di pubblico vengono utilizzati in ogni caso d’uso. Ad esempio, un pubblico può essere originato e utilizzato per **Discover** senza essere attivato, oppure può essere utilizzato in **Measure** flussi di lavoro senza essere inviato a una destinazione.

Per ulteriori informazioni sull&#39;origine e sulla gestione dei tipi di pubblico, vedere [Source e gestire i tipi di pubblico](./onboard-audiences.md). Per informazioni sulla gestione delle connessioni dati, vedere [Gestire le connessioni dati](./manage-data-connection.md).

## Da dove provengono i tipi di pubblico {#supported-sources}

Collaboration supporta più tipi di origine del pubblico. L’origine scelta determina il flusso di configurazione, i prerequisiti, i requisiti di autenticazione, il formato dei dati, la mappatura dei campi, il comportamento di aggiornamento e le opzioni di configurazione disponibili per l’introduzione di tipi di pubblico in Collaboration.

* Adobe Experience Platform
* Archiviazione cloud, tra cui Amazon S3, Google Cloud Storage e archiviazione Azure
* Servizi di condivisione dei dati, tra cui Snowflake e Condivisione Delta delle banche dati
* Adobe Audience Manager
* Caricamento di file CSV

Per un elenco delle origini supportate e dei passaggi di configurazione specifici per l&#39;origine, vedere [Panoramica sulle origini](./source-overview.md#available-sources).

## Di quali tipi di pubblico si compongono {#match-keys}

I tipi di pubblico in RTCDP Collaboration sono costituiti da chiavi di corrispondenza. A seconda della configurazione dell&#39;account, le chiavi di corrispondenza supportate possono includere **ID persone**, **ID dispositivo** e **ID partner**. Le chiavi di corrispondenza supportano flussi di lavoro come **sovrapposizione pubblico**, **attivazione** e **misurazione**.

Per ulteriori informazioni, consulta [Configurare le chiavi di corrispondenza](../setup/onboard-account.md#set-up-match-keys) e [Gestire le connessioni dati](../setup/manage-data-connection.md#match-keys)

## Utilizzare i tipi di pubblico nei progetti {#audiences-in-projects}

I progetti forniscono il contesto per collaborare con un’altra organizzazione. All’interno di un progetto, puoi utilizzare i tipi di pubblico per i casi di utilizzo di collaborazione supportati:

* **Individua**: confronta i tipi di pubblico e controlla le informazioni sulla sovrapposizione. Vedi [Individuare la sovrapposizione del pubblico](../collaborate/discover.md).
* **Attiva**: attiva i tipi di pubblico selezionati per l&#39;utilizzo della campagna. L&#39;attivazione viene avviata dalla scheda [!UICONTROL Attiva] nell&#39;area di lavoro del progetto e invia i tipi di pubblico alla destinazione configurata della connessione. Consulta [Attivare i tipi di pubblico](../collaborate/activate.md).
* **Misura**: rivedi i rapporti di consegna e conversione delle campagne associati al progetto. Vedere [Misurare le prestazioni](../collaborate/measure.md).

Per ulteriori informazioni sulla creazione e la gestione dei progetti, vedere [Creare e gestire progetti](../collaborate/manage-projects.md). Per informazioni sulla configurazione delle destinazioni, vedere [Panoramica sulle destinazioni](../destinations/overview.md).

## Passaggi successivi {#next-steps}

* [Rivedere le fonti di pubblico disponibili](./source-overview.md)
* [Source e gestire i tipi di pubblico](./onboard-audiences.md)
* [Creare e gestire i progetti](../collaborate/manage-projects.md)
* [Scopri la sovrapposizione del pubblico](../collaborate/discover.md)
* [Attiva tipi di pubblico](../collaborate/activate.md)
* [Misurare le prestazioni](../collaborate/measure.md)
* [Panoramica sulle destinazioni](../destinations/overview.md)
