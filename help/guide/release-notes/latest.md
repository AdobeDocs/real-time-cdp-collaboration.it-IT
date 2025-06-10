---
title: Note sulla versione più recente di Real-Time CDP Collaboration
description: Segui le ultime versioni di Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
source-git-commit: 691161cdc1f9338a470373988fbc0dee9a5be6db
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 3%

---

# Note sulla versione più recente di Real-Time CDP Collaboration

{{limited-availability-release-note}}

**Ultimo aggiornamento**: aprile 2025.

Queste note sulla versione descrivono le funzionalità di Real-Time Customer Data Platform Collaboration. I rilasci di Real-Time CDP Collaboration funzionano su un modello di consegna continua, che consente una cadenza di rilascio mensile approssimativa. Queste note sulla versione vengono aggiornate spesso, quindi assicurati di controllarle regolarmente.

## Maggio 2025 {#may-2025}

* Real-Time CDP Collaboration è ora disponibile per i clienti in **Australia** e **Nuova Zelanda**. È disponibile automaticamente per i clienti Real-Time CDP Prime e Ultimate in queste aree geografiche.
* Real-Time CDP Collaboration ora offre [destinazioni self-service](../setup/manage-destinations.md) tramite la scheda **[!UICONTROL Destinazioni personali]** nella sezione **[!UICONTROL Configurazione]**. Le destinazioni consentono di attivare tipi di pubblico in piattaforme di terze parti, come reti pubblicitarie o piattaforme di gestione dei dati, per raggiungere i clienti su vari canali. Attualmente, sono supportate solo le destinazioni Adobe Experience Platform. Se ti interessa configurare una destinazione diversa, contatta il tuo rappresentante Adobe. Per ulteriori informazioni sulle destinazioni, consulta la guida [panoramica sulle destinazioni](../destinations/overview.md).

   * Le destinazioni aggiungono inoltre il supporto per visualizzare i tipi di pubblico di Real-Time CDP Collaboration nel [portale del pubblico di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences.).

* Ora puoi modificare la frequenza di aggiornamento del pubblico per le connessioni dati esistenti in Real-Time CDP Collaboration. Attualmente, puoi scegliere di aggiornare i tipi di pubblico ogni giorno oppure ogni due o sei giorni. Per ulteriori informazioni su come modificare la frequenza di aggiornamento del pubblico, consulta la guida [gestire le connessioni dati](../setup/manage-data-connection.md#scheduling).
* Le suddivisioni dei crediti tra collaboratori sono ora impostate per ogni caso d’uso selezionato all’interno della connessione. È possibile impostare regole di consumo credito diverse per ogni caso d’uso per controllare meglio come vengono utilizzati i crediti. Per ulteriori informazioni sulla funzionalità di divisione del credito, consulta la guida alle [impostazioni di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sul modo in cui vengono utilizzati i crediti, consulta la guida [tipi di attività di credito](../setup/my-activity.md#types-of-activities). <br> ![Schermata delle impostazioni di connessione che mostra la funzionalità di divisione del credito.](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* Gli editori possono ora impostare i nomi e gli ID degli inserzionisti prima di accettare le impostazioni di connessione da un inserzionista. Gli editori possono impostare nomi e ID in base al sistema interno, che può essere diverso dai nomi e dagli ID dell’inserzionista. Per ulteriori informazioni sull&#39;aggiunta di nomi e ID inserzionisti, leggere la guida alle [impostazioni di connessione](../connect/establishing-connections.md#connection-settings.md). <br> ![Schermata delle impostazioni di connessione che mostra i nomi e gli ID degli inserzionisti dell&#39;impostazione del server di pubblicazione.](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## Aprile 2025 {#april-2025}

* Una nuova colonna **[!UICONTROL Input elaborati]** è stata aggiunta alla tabella dell&#39;attività di consumo di credito. Questa colonna mostra il numero totale di input (ad esempio, ID o righe) elaborati per ogni attività. [Ulteriori informazioni](/help/guide/setup/my-activity.md#inputs-processed). <br> ![Colonna elaborata degli input evidenziata nella visualizzazione Attività personale.](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* È stata aggiunta una nuova opzione e-mail di contatto per la creazione dell’account. In questo modo i collaboratori partner possono contattarti in base alle esigenze durante il processo di connessione. [Ulteriori informazioni](../setup/onboard-organization.md).

## Marzo 2025 {#march-2025}

* Quando [importi tipi di pubblico](/help/guide/setup/onboard-audiences.md) in Real-Time CDP Collaboration, ora puoi impostare una frequenza di aggiornamento del pubblico da **ogni uno a sei giorni** per gestire meglio l&#39;attività di credito di [Gestione dell&#39;audience](/help/guide/setup/my-activity.md#types-of-activities). [Ulteriori informazioni](/help/guide/setup/onboard-audiences.md#schedule). <br> ![Schermata di pianificazione che mostra intervalli di frequenza diversi per l&#39;aggiornamento dell&#39;iscrizione al pubblico.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png "Schermata di pianificazione che mostra intervalli di frequenza diversi per l&#39;aggiornamento dell&#39;iscrizione al pubblico."){width="250" align="center" zoomable="yes"}
* Quando stabilisci una connessione con un collaboratore, ora puoi scegliere tra **casi d&#39;uso** predefiniti. Il caso d’uso selezionato determina le sezioni di progetto e le funzionalità del prodotto che diventano disponibili. [Ulteriori informazioni](/help/guide/collaborate/manage-projects.md#project-use-cases).
   * *Misurazione campagna* abilita la sezione del progetto **Misura**.
   * *L&#39;individuazione del pubblico* abilita la sezione del progetto **Discover**.
   * *Attivazione pubblico* abilita le sezioni <br> del progetto **Attiva**
* È ora possibile eliminare le connessioni con i collaboratori che non si desidera più utilizzare. [Ulteriori informazioni](/help/guide/connect/establishing-connections.md#delete-connections).


## Febbraio 2025 - Disponibilità generale per i clienti USA {#february-2025-ga}

Real-Time CDP Collaboration, progettato appositamente per consentire ad inserzionisti ed editori di scoprire, attivare e misurare tipi di pubblico di alto valore senza cookie di terze parti, è ora generalmente disponibile negli Stati Uniti.

### Introduzione

1. **Configurazione dell&#39;accesso**: gli amministratori di sistema configurano le autorizzazioni di accesso per gli utenti. [Ulteriori informazioni](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access).
2. **Connetti origini dati**: importa tipi di pubblico da utilizzare in Real-Time CDP Collaboration. [Ulteriori informazioni](/help/guide/setup/onboard-audiences.md).
3. **Stabilisci connessioni partner**: inizia a collaborare con autori o marchi attendibili. [Ulteriori informazioni](/help/guide/connect/establishing-connections.md).
4. **Scopri e attiva**: crea progetti per identificare segmenti di pubblico importanti e attivarli nelle campagne. [Ulteriori informazioni](/help/guide/collaborate/manage-projects.md).

### Disponibilità

* Real-Time CDP Collaboration è attualmente disponibile solo per i clienti USA.
* È disponibile automaticamente per i clienti Real-Time CDP Prime e Ultimate

Per ulteriori informazioni, consulta:

* [Panoramica di Real-Time CDP Collaboration](/help/guide/home.md)
* [Flusso di lavoro end-to-end](/help/guide/end-to-end-workflow.md)
* [Panoramica sulle autorizzazioni](/help/guide/permissions/overview.md)
