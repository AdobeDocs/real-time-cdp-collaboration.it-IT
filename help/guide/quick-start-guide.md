---
title: Guida introduttiva all’onboarding di Real-Time CDP Collaboration
description: Scopri come integrare la tua organizzazione in Real-Time CDP Collaboration, inclusa la configurazione di ruoli e organizzazioni, l’origine del pubblico, l’attivazione e la misurazione. Questa guida aiuta gli inserzionisti e gli editori a configurare le impostazioni di collaborazione e a iniziare a utilizzare i tipi di pubblico condivisi in modo sicuro ed efficiente.
audience: admin, publisher, advertiser
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
source-git-commit: 5b17bcfbab02e8d24009a875ddea15cbd49c1506
workflow-type: tm+mt
source-wordcount: '1605'
ht-degree: 0%

---

# Guida introduttiva all’onboarding di Real-Time CDP Collaboration

Inizia a usare Real-Time CDP Collaboration configurando l’organizzazione, individuando i tipi di pubblico e abilitando l’attivazione e la misurazione incentrate sulla privacy.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti elementi:

- Una licenza Real-Time CDP Collaboration attiva.
- [Accesso amministratore di sistema o di prodotto a Adobe Experience Platform](./permissions/overview.md#use-cases).
- [Accesso eseguito per gli utenti finali](./permissions/manage-user-access.md).
- [Ruoli creati per la tua organizzazione e assegnati agli utenti](./permissions/manage-roles.md).
- Accesso alle risorse di branding, ad esempio il nome, il logo e il banner dell’organizzazione.
- Una [strategia chiave di corrispondenza definita](./setup/onboard-organization.md#set-up-match-keys) (attualmente, l&#39;e-mail con hash è l&#39;unica chiave di corrispondenza supportata).
- (Facoltativo) Se non utilizzi Experience Platform come destinazione, accedi a un’origine cloud supportata (Amazon S3 o Snowflake).

## Passaggio 1: completare la configurazione basata sui ruoli {#complete-role-based-setup}

>[!NOTE]
>
>Questo passaggio si applica sia agli inserzionisti che agli editori.

I ruoli di accesso della tua organizzazione determinano ciò che gli utenti possono vedere e fare in Real-Time CDP Collaboration. Prima di procedere, assicurati che le autorizzazioni basate sul ruolo siano configurate correttamente per garantire l’accesso e la visibilità appropriati nella piattaforma.

**Risorse:**

- [Documentazione di accesso utente](./permissions/manage-user-access.md)
- [Documentazione sulla configurazione dei ruoli](./permissions/manage-roles.md)


Guarda questo video per scoprire come assegnare l’accesso ai prodotti e le autorizzazioni per Collaboration utilizzando l’interfaccia utente di Admin Console e Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3452238/?learn=on&enablevpops&captions=ita)

## Passaggio 2: configurare l’organizzazione Real-Time CDP Collaboration {#set-up-your-organization}

>[!NOTE]
>
>Questo passaggio si applica sia agli inserzionisti che agli editori.

Prima di poter aggiungere tipi di pubblico, devi configurare l’organizzazione in Collaboration. Questo governa come si presenta e si comporta l’organizzazione nell’interfaccia.

Se non disponi dell’accesso come amministratore ad Experience Platform, contatta l’amministratore della tua organizzazione per ottenere assistenza per completare la configurazione.

Definisci il ruolo della tua organizzazione in Collaboration, fornisci risorse di branding e configura chiavi di corrispondenza per allineare i tipi di pubblico tra le connessioni. Quindi, completa i passaggi seguenti per finalizzare la configurazione e preparare la tua organizzazione a interagire con le connessioni.

>[!NOTE]
>
>Puoi creare uno o più collaboratori (ad esempio i profili dell’inserzionista o dell’editore) durante la configurazione. Alcuni campi, ad esempio le risorse di branding e l&#39;e-mail di contatto, possono essere aggiornati successivamente nell&#39;area di lavoro **[!UICONTROL Impostazioni]**. È possibile rimuovere le chiavi di corrispondenza a livello di progetto, ma non aggiungerle, quindi pianificale con attenzione.

- **Assegna un ruolo** - Determina se l&#39;organizzazione funge da inserzionista, editore o entrambi. Il tuo ruolo definisce le funzionalità di collaborazione disponibili, ad esempio l’avvio della condivisione di tipi di pubblico (inserzionista) o la disponibilità di tipi di pubblico (editore). Per ulteriori informazioni sull&#39;impatto dei ruoli sul flusso di lavoro di collaborazione, consulta la [Guida del flusso di lavoro end-to-end](./end-to-end-workflow.md).
- **Risorse di branding** - Aggiungi quanto segue al tuo account:
   - Marchio (massimo 100 caratteri)
   - Descrizione del marchio (massimo 1.000 caratteri)
   - Logo del marchio (SVG &lt;20 KB, idealmente quadrato)
   - Banner del marchio (JPG 2688x1536 o simile)
- **E-mail di contatto** - Fornisci un&#39;e-mail aziendale che i collaboratori potranno utilizzare dopo aver stabilito una connessione.

  >[!NOTE]
  >
  >Se stai creando un account publisher e desideri che sia visibile al pubblico nel catalogo delle connessioni di Collaboration, contatta il rappresentante del tuo account Adobe. Gli account dell’editore richiedono un banner personalizzato per il marchio (JPG 2688x1536); questo file può essere condiviso direttamente con il tuo rappresentante.

- **Configura chiavi di corrispondenza** - Seleziona gli identificatori utilizzati per la corrispondenza del pubblico (attualmente, l&#39;e-mail con hash è l&#39;unica chiave di corrispondenza supportata).

Una volta creata l’organizzazione e configurate le chiavi di branding e corrispondenza, l’organizzazione è pronta per iniziare a individuare il pubblico e ad attivare i dati.

Per ulteriori informazioni sulla configurazione iniziale dell&#39;organizzazione, tra cui la definizione dei ruoli, il caricamento delle risorse di branding e la configurazione delle chiavi di corrispondenza, consulta il [documento di configurazione iniziale dell&#39;organizzazione](./setup/onboard-organization.md#initial-organization-setup){target="_blank"}.

Guarda una procedura dettagliata sulla configurazione dell’inserzionista, che include la creazione di account, il branding e la configurazione della chiave di corrispondenza.

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## Passaggio 3: tipi di pubblico di Source (da Experience Platform o da una sorgente cloud) {#source-audiences}

Scegli uno o entrambi i seguenti archivi di dati per il pubblico di origine. Utilizza l’interfaccia utente di Collaboration o coordina con Adobe per generare il pubblico in un formato che rispetti la privacy.

### Opzione A: Source da Experience Platform

[Utilizza l&#39;interfaccia utente delle destinazioni di Collaboration per collegare una sandbox che contiene tipi di pubblico](./setup/onboard-audiences.md). Utilizza questo metodo self-service per fare riferimento a segmenti di pubblico esistenti dall&#39;interno della tua istanza di Experience Platform.

### Opzione B: Source da Snowflake o Amazon S3

Per configurare un&#39;origine cloud (ad esempio, [!DNL AWS S3] o [!DNL Snowflake]), prepara i dati del pubblico utilizzando il seguente [Audience Specification PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.0.pdf). Una volta completata la configurazione o in caso di domande, contatta il rappresentante del tuo account Adobe per finalizzarla. Questo metodo non è self-service e richiede l’assistenza di Adobe.

>[!IMPORTANT]
>
>I file del pubblico basati su cloud devono seguire lo schema richiesto descritto in Audience Specification PDF. I file devono includere identificatori con hash (SHA256 minuscolo), campi di metadati obbligatori come `segment_name` e `activation_id` e utilizzare formati supportati come CSV o Parquet. Adobe non normalizza i dati prima dell’attivazione. Il TTL viene applicato in base alla durata del pubblico.
>
>In questa fase, tutti i tipi di pubblico nel file caricato provengono da origini complete. L’accesso a specifiche organizzazioni partner viene fornito separatamente tramite l’interfaccia utente di Collaboration.

### Configurare i tipi di pubblico

Configura il modo in cui i tipi di pubblico vengono preparati, abbinati e governati per essere utilizzati nelle connessioni.

- **Seleziona tipi di pubblico** *(solo Experience Platform)* - Scegli segmenti di pubblico con identificatori supportati.
- **Mappa le chiavi di corrispondenza** - Allinea i campi del pubblico con le chiavi di corrispondenza configurate.
- **Applica trasformazioni** - Se necessario, inserisci valori in testo normale (ad esempio e-mail).
- **Aggiornamenti pianificati** - Definisci la frequenza di aggiornamento (ad esempio, giornaliera).
- **Configura le impostazioni di consenso** - Determina quali profili possono essere inclusi nelle connessioni selezionando una modalità di consenso: consenso, rinuncia o nessuno.

>[!NOTE]
>
>Puoi aggiungere o rimuovere tipi di pubblico e aggiornare la pianificazione dell’aggiornamento direttamente nell’interfaccia utente di Collaboration. Per modificare altre impostazioni, ad esempio le chiavi di corrispondenza o la modalità di consenso, devi eliminare e ricreare la connessione dati.

>[!IMPORTANT]
>
>**Numero massimo di tipi di pubblico per ruolo di collaboratore:**
>
>- **Gli inserzionisti** possono creare fino a 25 tipi di pubblico.
>- **Gli editori** possono creare fino a 250 tipi di pubblico (ciascuno con un minimo di 5.000 ID).

>[!IMPORTANT]
>
>**Corrispondenza con i requisiti chiave:**
>
>Tutte le chiavi di corrispondenza devono essere **tagliate**, **in minuscolo** e **con hash SHA256**.\
>Se fornisci valori con hash che utilizzano caratteri maiuscoli, Collaboration li converte automaticamente in minuscoli.\
>Se l&#39;origine contiene **identificatori di testo normale**, utilizza l&#39;opzione **[!UICONTROL Applica trasformazione]** nell&#39;interfaccia utente per applicare l&#39;hashing. Questa opzione è disponibile solo quando si selezionano i tipi di pubblico da Experience Platform e non è supportata per le origini basate su cloud.
>
>Per ulteriori informazioni, consulta la sezione [map fields](./setup/onboard-audiences.md#map-fields) della guida import and manage audiences.

Per visualizzare una procedura dettagliata su come fare riferimento a tipi di pubblico utilizzando l’interfaccia utente di Collaboration, guarda il video dimostrativo di Collaboration Audience Referencing riportato di seguito.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

In alternativa, consulta il documento su [rendere i tipi di pubblico disponibili in Real-Time CDP Collaboration](https://experienceleague.adobe.com/it/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#import-audiences).

## Passaggio 4: attivare i tipi di pubblico (su Experience Platform o una destinazione cloud) {#activate-audiences}

>[!NOTE]
>
>Questo passaggio si applica sia agli inserzionisti che agli editori.

Utilizza l’interfaccia utente di Collaboration per attivare i tipi di pubblico nell’istanza di Experience Platform o in una destinazione cloud.

### Opzione A: Attivare Experience Platform

Completa i seguenti passaggi descritti nella guida [Configurare Adobe Experience Platform come destinazione](https://experienceleague.adobe.com/it/docs/real-time-cdp-collaboration/using/destinations/experience-platform).

- **Crea una destinazione**. Utilizza l&#39;interfaccia utente per impostare una destinazione Experience Platform (a livello di sandbox).
- **Mappa chiavi corrispondenti** - Seleziona l&#39;identificatore (ad esempio, `hashedEmail`).
- **Definisci TTL** - Imposta scadenza (1-30 giorni).
- **Verifica in Audience Portal** - Dopo che un collaboratore ti ha inviato un pubblico, verifica che questo venga visualizzato in Audience Portal nell&#39;origine &quot;[!UICONTROL Real-Time CDP Collaboration].&quot;

### Opzione B: Attivare su cloud

Per attivare i tipi di pubblico in una destinazione cloud (ad esempio [!DNL AWS S3] o [!DNL Snowflake]), contatta il rappresentante del tuo account Adobe per avviare il processo di configurazione. Dovrai fornire i dettagli della destinazione, ad esempio il percorso del file, le credenziali e il formato di file previsto. Durante l&#39;installazione, è inoltre necessario specificare una chiave di corrispondenza (ad esempio, `hashedEmail`) e definire il TTL e la frequenza di aggiornamento desiderati. Una volta completata la configurazione, Adobe esegue il provisioning della destinazione e assicura che i dati vengano consegnati correttamente.

I dati del pubblico inviati a una destinazione cloud seguono uno schema predefinito. Per una descrizione dettagliata dei campi e del formato richiesti, scarica la [Guida di Collaboration Audience Activation](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

### Differenze chiave

L’elenco seguente evidenzia le differenze tra le opzioni di Experience Platform e di attivazione cloud:

- Le attivazioni per Experience Platform sono completamente self-service e visibili nel Portale dell’audience.
- Le destinazioni cloud richiedono il coordinamento di Adobe e non sono visibili nell’interfaccia utente.

## Passaggio 5: impostare la misurazione (facoltativo) {#set-up-measurement}

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile in **beta** ed è disponibile esclusivamente per i clienti del programma Disponibilità limitata. Contatta il tuo rappresentante Adobe per richiedere l’accesso.

>[!IMPORTANT]
>
>L&#39;area di lavoro **[!UICONTROL Measure]** è disponibile solo se il caso di utilizzo **[!UICONTROL Measurement]** è stato abilitato [durante il processo di connessione](./connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, consulta la guida [gestisci progetti](./collaborate/manage-projects.md#project-use-cases).

Collaboration offre una serie di rapporti per analizzare la portata, la frequenza e l’efficacia delle campagne. Anche se l&#39;area di lavoro **[!UICONTROL Measure]** è disponibile nell&#39;interfaccia utente, la funzionalità di reporting completa potrebbe richiedere l&#39;abilitazione del back-end.

Per informazioni su come visualizzare e interpretare i report di misurazione, vedere la [Guida alla misurazione](./collaborate/measure.md). Include informazioni sull’attribuzione, le metriche di riepilogo delle campagne e dashboard quali le curve di portata e la distribuzione della frequenza.

<!-- Commenting out the below information as this workflow is not yet in Beta but will be imminently. A guided measurement configuration workflow will be available in a future release."
### Configure measurement workflow

Collaboration supports two measurement workflows:

- **Attribution using Adobe Experience Platform datasets**
- **Campaign summary using only partner-provided data**

Choose the appropriate workflow below based on your campaign measurement goals.

#### Option A: Attribution using Experience Platform datasets

Use this workflow to measure conversion activity using datasets stored in Experience Platform.

1. **Create a measurement data connection**
   - Select the dataset that contains your conversion events.
   - Map identity fields from your dataset to the match keys used in Collaboration.
   - Manage consent and governance settings.
   - Define one or more conversion events to measure.
   - Review and confirm your setup.

2. **Run a measurement report**
   - Go to the **[!UICONTROL Measure]** workspace within the associated project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Attribution]** as the report type.
   - Select the defined conversion event(s).
   - Submit the report. It will run on the specified date and populate within 24 hours.

#### Option B: Campaign summary using partner-provided data

Use this workflow to generate campaign summary insights based on advertiser-supplied identifiers (for example, campaign ID).

1. **Set up the connection**
   - In the connection settings, ensure **[!UICONTROL Measurement]** is selected as a use case.
   - Create a project under the connection with **[!UICONTROL Measurement]** as an activity.

2. **Provide campaign context**
   - Input required campaign identifiers (for example, **Campaign ID**) for the partner to reference.
   - Align with your partner on campaign scope and reporting timeline.

3. **Run a measurement report**
   - Navigate to the **[!UICONTROL Measure]** workspace within the project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Campaign summary]** as the report type.
   - Submit the report. It will run on the selected date and populate within 24 hours. -->

## Verifica

Dopo l’attivazione, verifica che i tipi di pubblico siano stati correttamente consegnati o resi disponibili nella destinazione appropriata.

- Verifica che i tipi di pubblico vengano visualizzati nel Portale pubblico (per l’attivazione di Experience Platform).
- Conferma la corretta consegna cloud tramite i registri di destinazione esterni o la conferma.

## Passaggio 6: Connettersi con i collaboratori {#connect-with-collaborators}

Al termine della configurazione e del provisioning dei dati, l’organizzazione è ora pronta a connettersi con i collaboratori inviando o accettando inviti e inviando le impostazioni del progetto per l’approvazione. Questo processo di connessione prevede l&#39;invio o la ricezione di inviti, la revisione e l&#39;invio di impostazioni di connessione (ad esempio casi d&#39;uso e consumo di credito) e la conferma della relazione.

In qualità di inserzionista, utilizza l&#39;area di lavoro **[!UICONTROL Connetti]** dal menu di navigazione a sinistra nell&#39;interfaccia utente di Collaboration per sfogliare gli editori disponibili.

>[!NOTE]
>
>Attualmente, solo gli inserzionisti possono sfogliare gli editori. Gli editori non possono esplorare o avviare connessioni con gli inserzionisti.

Per una panoramica di questo flusso, vedere la [Guida alla connessione con inserzionisti o editori](./connect/establishing-connections.md){target="_blank"}. Per una panoramica visiva del processo di connessione, inclusi la navigazione dei collaboratori e la gestione delle impostazioni di connessione, guarda il video di configurazione dell&#39;account dell&#39;inserzionista [&#128279;](https://experienceleague.adobe.com/it/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

## Passaggi successivi

Hai completato la configurazione iniziale e hai configurato l’organizzazione per una collaborazione sicura. Quindi, esplora le seguenti risorse per comprendere meglio i concetti di attivazione, misurazione e governance dei dati:

- [Documentazione del flusso di lavoro di Audience Activation](./collaborate/activate.md)
- [Casi di utilizzo della misurazione](./collaborate/measure.md)
- [Best practice per la governance di Collaboration](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
