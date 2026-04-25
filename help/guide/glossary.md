---
title: Glossario
description: Terminologia chiave per Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hide: true
exl-id: 870c45d0-df68-487f-bbe2-d9862a8ea62e
TQID: https://experienceleague.adobe.com/aamkkPQbkaATqzByHmnTU2QGiUXLOn1yhz1jPA8LgGc
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 837
ht-degree: 3%

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

Un identificatore di dispositivo è un numero univoco associato a un dispositivo, ad esempio uno smartphone o un tablet. It is used to track and identify the device across various platforms and services, enabling personalized user experiences and targeted advertising.

## I

### Invita

An invite in Adobe Real-Time CDP Collaboration refers to a request sent to another user or organization to join a project or data collaboration effort. Invites help facilitate secure and controlled access to shared data and resources.

<!--

## J

### Join key

In the context of identity crosswalks, a join key is a unique identifier used to match and link different identifiers across datasets, enabling the integration and unification of audience data from various sources. For example, a hashed email (HEM) can be a join key.

-->

## L

### Chiavi di corrispondenza

Match keys are unique identifiers used to link records across different datasets. They help ensure that data from different sources can be accurately matched and integrated, facilitating better data analysis and audience segmentation.

## O

### Overlap

An overlap (or audience overlap) refers to the common audience segments that exist between different datasets. Understanding audience overlap helps identify potential collaboration opportunities and allows for more targeted marketing efforts by leveraging shared audience data.

## P

### Progetto

A project in Adobe Real-Time CDP Collaboration is a workspace where users can collaborate on specific data integration and audience segmentation tasks. Projects help organize and manage data-sharing efforts, making collaboration more efficient and streamlined.

### Pubblico non privato

Within the context of projects, this is an audience that is discoverable by your collaborator. Audiences can be private, custom, or public. Private audiences are not discoverable by any other collaborators. Custom audiences can be discovered by certain collaborators only, and public audiences can be discovered by all collaborators.

### Editore

A Publisher is an owner or operator of online content or services where personal data is collected with consent and is available for use by other entities for digital advertising and audience measurement.

## S

### Sketches {#sketches}

Sketches (or data sketches) are simplified summaries of audience data used in Real-Time CDP Collaboration. They allow brands and publishers to analyze audience overlaps and insights without sharing actual customer data. Think of them like anonymous headcounts rather than detailed customer profiles.
In Adobe Real-Time CDP Collaboration, data sketches:

* Help determine how similar two audiences are
* Maintain privacy while enabling collaboration
* Need to be refreshed at least every 7 days to remain valid

If sketches aren&#39;t refreshed regularly, audience overlap reports will show zero values and audience sharing may become temporarily unavailable. Data sketches are automatically refreshed whenever an audience membership is updated in Real-Time CDP Collaboration.

## U

### Caso d’uso

Un caso d’uso definisce uno scenario di business specifico o un problema che può essere risolto utilizzando Adobe Real-Time CDP Collaboration. In Real-Time CDP Collaboration, per raggiungere un obiettivo particolare, sono disponibili casi di utilizzo di esempio come l’individuazione o la misurazione del pubblico.
