---
title: Note sulla versione più recente di Real-Time CDP Collaboration
description: Segui le ultime versioni di Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
source-git-commit: 697a822eb02d42e2fad46c09232ce569a675c032
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 1%

---

# Note sulla versione più recente di Real-Time CDP Collaboration

{{limited-availability-release-note}}

**Ultimo aggiornamento**: luglio 2025.

Queste note sulla versione descrivono le funzionalità rilasciate in Adobe Real-Time CDP Collaboration. I rilasci di Collaboration funzionano su un modello di consegna continua, che consente una cadenza di rilascio mensile approssimativa. Queste note sulla versione vengono aggiornate spesso, quindi assicurati di controllarle regolarmente.

## Luglio 2025 {#july-2025}

Real-time CDP Collaboration ora supporta la collaborazione brand-to-brand. I collaboratori possono ora creare connessioni, indipendentemente dal fatto che siano inserzionisti o editori. Ciò consente opportunità di collaborazione più flessibili e consente ai brand di sfruttare i dati e le informazioni reciproci. Per ulteriori informazioni sulle differenze tra la collaborazione da brand a brand e la collaborazione da inserzionista a editore, consulta la [guida ai modelli di collaborazione](../overview/collaboration-patterns.md).

* I collaboratori possono ora connettersi tra loro utilizzando [inviti di connessione privati](../connect/establishing-connections.md#private-connection-invites). Condividi il codice di connessione univoco del tuo account con un collaboratore che potrà quindi utilizzarlo per connetterti direttamente. Questa è una caratteristica fondamentale della collaborazione brand-to-brand, che consente ai collaboratori di stabilire connessioni oltre a quelle degli inserzionisti che esplorano la directory **[!UICONTROL Discover publishers]**.
* [Le destinazioni self-service](../setup/manage-destinations.md) sono ora disponibili sia per gli inserzionisti che per gli editori.
* Attivazione pubblico è ora disponibile per entrambi i collaboratori in una connessione, indipendentemente dal loro [ruolo account](../overview/roles.md). Le impostazioni di Audience Activation sono configurate durante la [creazione di connessioni](../connect/establishing-connections.md#configure-connection-settings), consentendo di specificare quale collaboratore può attivare i tipi di pubblico. Per ulteriori informazioni sull&#39;attivazione del pubblico, consulta la guida [attiva tipi di pubblico](../collaborate/activate.md).
* Il caso d&#39;uso **[!UICONTROL Attiva]** è stato riconfigurato per supportare la collaborazione brand-to-brand. Nella scheda **[!UICONTROL Attiva]** di un progetto vengono ora visualizzati i tipi di pubblico inviati al collaboratore e quelli attivati a destinazione dal collaboratore. Per ulteriori informazioni, consulta la guida [attiva pubblico](../collaborate/activate.md). <br> ![Attiva dashboard con le sezioni Audiences inviate a e Audiences attivate.](/help/assets/release-notes/2025/activate-dashboard.png){zoomable="yes"}

## Maggio 2025 {#may-2025}

* Real-Time CDP Collaboration è ora disponibile per i clienti in **Australia** e **Nuova Zelanda**. È disponibile automaticamente per i clienti Real-Time CDP Prime e Ultimate in queste aree geografiche.
* Real-Time CDP Collaboration ora offre [destinazioni self-service](../setup/manage-destinations.md) tramite la scheda **[!UICONTROL Destinazioni personali]** nella sezione **[!UICONTROL Configurazione]**. Le destinazioni consentono di attivare tipi di pubblico in piattaforme di terze parti, come reti pubblicitarie o piattaforme di gestione dei dati, per raggiungere i clienti su vari canali. Attualmente, sono supportate solo le destinazioni Adobe Experience Platform. Se ti interessa configurare una destinazione diversa, contatta il tuo rappresentante Adobe. Per ulteriori informazioni sulle destinazioni, consulta la guida [panoramica sulle destinazioni](../destinations/overview.md).
   * Le destinazioni aggiungono inoltre il supporto per visualizzare i tipi di pubblico di Collaboration nel [portale del pubblico di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences).
* Ora puoi modificare la frequenza di aggiornamento del pubblico per le connessioni dati esistenti in Collaboration. Attualmente, puoi scegliere di aggiornare i tipi di pubblico ogni giorno oppure ogni due o sei giorni. Per ulteriori informazioni su come modificare la frequenza di aggiornamento del pubblico, consulta la guida [gestire le connessioni dati](../setup/manage-data-connection.md#scheduling).
* Le suddivisioni dei crediti tra collaboratori sono ora impostate per ogni caso d’uso selezionato all’interno della connessione. È possibile impostare regole di consumo credito diverse per ogni caso d’uso per controllare meglio come vengono utilizzati i crediti. Per ulteriori informazioni sulla funzionalità di divisione del credito, consulta la guida alle [impostazioni di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sul modo in cui vengono utilizzati i crediti, consulta la guida [tipi di attività di credito](../setup/my-activity.md#types-of-activities). <br> ![Schermata delle impostazioni di connessione che mostra la funzionalità di divisione del credito.](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* Gli editori possono ora impostare i nomi e gli ID degli inserzionisti prima di accettare le impostazioni di connessione da un inserzionista. Gli editori possono impostare nomi e ID in base al sistema interno, che può essere diverso dai nomi e dagli ID dell’inserzionista. Per ulteriori informazioni sull&#39;aggiunta di nomi e ID inserzionisti, leggere la guida alle [impostazioni di connessione](../connect/establishing-connections.md#connection-settings.md). <br> ![Schermata delle impostazioni di connessione che mostra i nomi e gli ID degli inserzionisti dell&#39;impostazione del server di pubblicazione.](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## Aprile 2025 {#april-2025}

* Una nuova colonna **[!UICONTROL Input elaborati]** è stata aggiunta alla tabella dell&#39;attività di consumo di credito. Questa colonna mostra il numero totale di input (ad esempio, ID o righe) elaborati per ogni attività. [Ulteriori informazioni](/help/guide/setup/my-activity.md#inputs-processed). <br> ![Colonna elaborata degli input evidenziata nella visualizzazione Attività personale.](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* È stata aggiunta una nuova opzione e-mail di contatto per la creazione dell’account. In questo modo i collaboratori partner possono contattarti in base alle esigenze durante il processo di connessione. [Ulteriori informazioni](../setup/onboard-account.md).

## Marzo 2025 {#march-2025}

* Quando [si crea un&#39;origine per il pubblico](/help/guide/setup/onboard-audiences.md) in Collaboration, è ora possibile impostare una frequenza di aggiornamento del pubblico da **ogni giorno a sei giorni** per gestire meglio l&#39;[attività di credito di Gestione dell&#39;audience](/help/guide/setup/my-activity.md#types-of-activities). Per ulteriori informazioni, consulta la guida [gestire tipi di pubblico](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences). <br> ![Schermata di pianificazione che mostra intervalli di frequenza diversi per l&#39;aggiornamento dell&#39;iscrizione al pubblico.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png "Schermata di pianificazione che mostra intervalli di frequenza diversi per l&#39;aggiornamento dell&#39;iscrizione al pubblico."){width="250" align="center" zoomable="yes"}
* Quando stabilisci una connessione con un collaboratore, ora puoi scegliere tra **casi d&#39;uso** predefiniti. Il caso d’uso selezionato determina le sezioni di progetto e le funzionalità del prodotto che diventano disponibili. Per ulteriori informazioni, consulta la guida [gestisci progetti](/help/guide/collaborate/manage-projects.md#project-use-cases).
   * *Measurement* abilita la sezione del progetto **Measure**.
   * *L&#39;individuazione del pubblico* abilita la sezione del progetto **Discover**.
   * *Attivazione pubblico* abilita le sezioni **del progetto** Attiva<br>
* È ora possibile eliminare le connessioni con i collaboratori che non si desidera più utilizzare. Per informazioni su come eliminare le connessioni, leggere la guida [eliminazione delle connessioni](/help/guide/connect/establishing-connections.md#delete-connections).

## Febbraio 2025 {#february-2025}

Adobe Real-Time CDP Collaboration, creato appositamente per consentire agli inserzionisti e agli editori di scoprire, attivare e misurare tipi di pubblico di alto valore senza cookie di terze parti, ora è generalmente disponibile negli Stati Uniti.

### Introduzione

1. **Configurazione dell&#39;accesso**: gli amministratori di sistema configurano le autorizzazioni di accesso per gli utenti. Per ulteriori informazioni sulla configurazione delle autorizzazioni di accesso, leggere la [guida alla gestione dell&#39;accesso utente](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access).
2. **Connetti origini dati**: tipi di pubblico di Source da utilizzare in Collaboration. Per iniziare a individuare i tipi di pubblico, leggere la guida [source and manage audiences](/help/guide/setup/onboard-audiences.md) (Origine e gestione dei tipi di pubblico).
3. **Stabilisci connessioni**: inizia a collaborare con inserzionisti o editori attendibili. Per ulteriori informazioni sulla creazione di connessioni, leggere la guida [stabilire connessioni](/help/guide/connect/establishing-connections.md).
4. **Scopri e attiva**: crea progetti per identificare tipi di pubblico importanti da attivare nelle campagne. Per ulteriori informazioni sulla creazione di progetti, consulta la guida [gestisci progetti](/help/guide/collaborate/manage-projects.md).

### Disponibilità

* Adobe Real-Time CDP Collaboration è attualmente disponibile solo per i clienti negli Stati Uniti.
* È disponibile automaticamente per i clienti di Adobe Real-Time CDP Prime e Ultimate

Per ulteriori informazioni, leggere:

* [Panoramica di Collaboration](/help/guide/home.md)
* [Flusso di lavoro end-to-end](/help/guide/overview/end-to-end-workflow.md)
* [Panoramica sulle autorizzazioni](/help/guide/permissions/overview.md)
