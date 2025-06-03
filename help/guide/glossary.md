---
title: Glossario
description: Terminologia chiave per Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 870c45d0-df68-487f-bbe2-d9862a8ea62e
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 2%

---

# Glossario

{{limited-availability-release-note}}

Il presente glossario fornisce le definizioni dei termini chiave identificati nel prodotto e nella documentazione dell’Adobe Real-Time CDP Collaboration. Comprendere questi termini ti aiuterà a utilizzare meglio il prodotto e le sue funzioni.

## A

### Inserzionista

Qualsiasi entità che spenderà il budget di marketing per raggiungere il pubblico tra gli editori o altri partner del brand per raggiungere gli obiettivi di brand awareness, ricerca di potenziali clienti, ricoinvolgimento e conversioni.

## C

### Archiviazione cloud

L’archiviazione cloud è una soluzione di cloud computing che consente di memorizzare dati e file su Internet tramite un provider di cloud computing ed è quasi sempre parte dello stack di dati di un’organizzazione. Alcuni esempi includono Amazon Web Services (AWS), Microsoft Azure e Google Cloud Platform (GCP).

### Richiesta di connessione

Una richiesta di connessione è una richiesta formale inviata da un&#39;organizzazione a un&#39;altra per stabilire una connessione di condivisione dei dati. Una volta accettato, consente alle due parti di collaborare e condividere i dati sul pubblico in modo sicuro.

### Impostazioni della connessione

Dopo aver accettato una richiesta di connessione, l&#39;iniziatore della richiesta invia le impostazioni di connessione al collaboratore per l&#39;approvazione. Queste impostazioni di connessione disciplinano il modo in cui i collaboratori collaborano sui progetti e includono le chiavi di corrispondenza da utilizzare, la proprietà della fatturazione e altro ancora.

<!--

### Crosswalk

An identity crosswalk is a tool used to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. It creates a bridge between different data points, allowing for a more comprehensive and cohesive view of the data.

-->

## D

### Data Clean Room

Un ambiente di collaborazione sicuro che consente a due o più partecipanti di sfruttare le risorse di dati per utilizzi specifici e concordati, garantendo al contempo l’applicazione di rigorose limitazioni di accesso ai dati. Questo livello di infrastruttura viene spesso fornito dai provider di archiviazione cloud e/o da data warehouse come Snowflake e Databricks ed è ideale per gli utenti tecnici come data engineer e data scientist esperti in competenze come SQL.

### Collaborazione sui dati

La collaborazione sui dati prevede la combinazione e l’analisi dei dati all’interno di un’azienda o insieme ai partner per vari scopi, come il targeting del pubblico, la misurazione e le informazioni approfondite. Le piattaforme di collaborazione sui dati offrono ambienti sicuri per condividere i dati in modo sicuro, rispettando al contempo i requisiti di privacy e sicurezza.

### Connessione dati

Una connessione dati è l&#39;origine da cui è possibile importare i dati in Real-Time CDP Collaboration. Attualmente, Experience Platform è l’unica connessione dati disponibile. Ulteriori informazioni sulla [gestione delle connessioni dati](/help/guide/setup/manage-data-connection.md).

### Accordo di condivisione dei dati

Un accordo di condivisione dei dati è un contratto formale tra due o più parti che delinea i termini e le condizioni per la condivisione dei dati. Garantisce che tutte le parti rispettino i requisiti legali e di privacy e stabilisce linee guida per l’utilizzo e la protezione dei dati.

### Identificatore dispositivo

Un identificatore di dispositivo è un numero univoco associato a un dispositivo, ad esempio uno smartphone o un tablet. Viene utilizzato per tracciare e identificare il dispositivo tra varie piattaforme e servizi, consentendo esperienze utente personalizzate e pubblicità mirata.

## I

### Invita

Un invito in un Adobe Real-Time CDP Collaboration si riferisce a una richiesta inviata a un altro utente o organizzazione per partecipare a un progetto o a un&#39;attività di collaborazione sui dati. Invita ad agevolare un accesso sicuro e controllato ai dati e alle risorse condivisi.

<!--

## J

### Join key

In the context of identity crosswalks, a join key is a unique identifier used to match and link different identifiers across datasets, enabling the integration and unification of audience data from various sources. For example, a hashed email (HEM) can be a join key.

-->

## M

### Chiavi di corrispondenza

Le chiavi di corrispondenza sono identificatori univoci utilizzati per collegare record tra set di dati diversi. Garantiscono che i dati provenienti da diverse origini possano essere combinati e integrati in modo accurato, facilitando una migliore analisi dei dati e segmentazione del pubblico.

## O

### Sovrapposizione

Una sovrapposizione (o sovrapposizione di pubblico) si riferisce ai segmenti di pubblico comuni esistenti tra set di dati diversi. Comprendere la sovrapposizione dei tipi di pubblico aiuta a identificare potenziali opportunità di collaborazione e consente attività di marketing più mirate sfruttando i dati di pubblico condiviso.

## P

### Progetto

Un progetto in Adobe Real-Time CDP Collaboration è un’area di lavoro in cui gli utenti possono collaborare a specifiche attività di integrazione dei dati e segmentazione del pubblico. I progetti aiutano a organizzare e gestire le attività di condivisione dei dati, rendendo la collaborazione più efficiente e semplificata.

### Pubblico

Nel contesto dei progetti, si tratta di un pubblico individuabile dal tuo collaboratore. Il pubblico può essere privato, personalizzato o pubblico. I tipi di pubblico privati non sono individuabili da altri collaboratori. I tipi di pubblico personalizzati possono essere rilevati solo da alcuni collaboratori e quelli pubblici possono essere rilevati da tutti i collaboratori.

### Editore

Un editore è un proprietario o un operatore di contenuti o servizi online in cui i dati personali vengono raccolti con il consenso e sono disponibili per l’utilizzo da parte di altre entità per la pubblicità digitale e la misurazione del pubblico.

## S

### Schizzi {#sketches}

Gli schizzi (o schizzi di dati) sono riepiloghi semplificati dei dati sul pubblico utilizzati in Real-Time CDP Collaboration. Consentono ai brand e agli editori di analizzare le sovrapposizioni di pubblico e le informazioni senza condividere i dati effettivi dei clienti. Considerali come headcount anonimi piuttosto che profili cliente dettagliati.
Ad Adobe Real-Time CDP Collaboration, gli schizzi di dati:

* Aiuta a determinare quanto sono simili due tipi di pubblico
* Mantenere la privacy e consentire la collaborazione
* Deve essere aggiornato almeno ogni 7 giorni per rimanere valido

Se gli schizzi non vengono aggiornati regolarmente, i rapporti di sovrapposizione del pubblico mostreranno valori zero e la condivisione del pubblico potrebbe diventare temporaneamente non disponibile. Gli schizzi di dati vengono aggiornati automaticamente ogni volta che un’iscrizione al pubblico viene aggiornata in Real-Time CDP Collaboration.

## U

### Caso d’uso

Un caso d’uso definisce uno scenario di business specifico o un problema che può essere risolto utilizzando Adobe Real-Time CDP Collaboration. In Real-Time CDP Collaboration, per raggiungere un obiettivo particolare, sono disponibili casi di utilizzo di esempio come l’individuazione del pubblico o la misurazione delle campagne.
