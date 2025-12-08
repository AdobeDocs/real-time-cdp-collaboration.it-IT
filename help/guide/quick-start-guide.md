---
title: Guida rapida e configurazione di Real-Time CDP Collaboration
description: Scopri come configurare Real-Time CDP Collaboration, ruoli e account, tipi di pubblico di origine, attivare i dati e connettersi con i partner in modo sicuro.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
source-git-commit: d0ad2d66ac7178c24449be415a613b89d9b3bee1
workflow-type: tm+mt
source-wordcount: '1389'
ht-degree: 0%

---

# Guida rapida di Real-Time CDP Collaboration

{{limited-availability-release-note}}

Inizia a usare Real-Time CDP Collaboration configurando l’organizzazione, individuando i tipi di pubblico e abilitando l’attivazione e la misurazione incentrate sulla privacy.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti elementi:

- Una licenza Real-Time CDP Collaboration attiva.
- [Accesso amministratore di sistema o di prodotto a Adobe Experience Platform](./permissions/overview.md).
- [Accesso eseguito per gli utenti finali](./permissions/manage-user-access.md).
- [Ruoli creati per la tua organizzazione e assegnati agli utenti](./permissions/manage-roles.md).
- Accesso alle risorse di branding, ad esempio il nome, il logo e il banner dell’organizzazione.
- Una [strategia chiave di corrispondenza definita](./setup/onboard-account.md#set-up-match-keys)
- (Facoltativo) Accedi a un’origine cloud supportata (Amazon S3 o Snowflake) se non utilizzi Experience Platform per la gestione dell’audience.

## Passaggio 1: completare la configurazione basata sui ruoli {#complete-role-based-setup}

I ruoli di accesso della tua organizzazione determinano ciò che gli utenti possono vedere e fare in Collaboration. Prima di procedere, assicurati che le autorizzazioni basate sul ruolo siano configurate correttamente per garantire l’accesso e la visibilità appropriati nella piattaforma.

**Risorse:**

- [Documentazione di accesso utente](./permissions/manage-user-access.md)
- [Documentazione sulla configurazione dei ruoli](./permissions/manage-roles.md)


Guarda questo video per scoprire come assegnare l’accesso ai prodotti e le autorizzazioni per Collaboration utilizzando Admin Console e Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3452238/?captions=ita&learn=on&enablevpops)

## Passaggio 2: configurare l’account Collaboration {#set-up-your-account}

Prima di poter individuare i tipi di pubblico, è necessario configurare l’account in Collaboration. Questo governa il modo in cui apparisci e gli elementi a cui hai accesso nell’interfaccia.

Se non disponi dell’accesso necessario, fai riferimento al passaggio 1 o contatta l’amministratore della tua organizzazione per assistenza al completamento della configurazione.

Definisci il ruolo del tuo account in Collaboration, fornisci risorse di branding e configura chiavi di corrispondenza per allineare i tipi di pubblico tra le connessioni.

>[!NOTE]
>
>Puoi creare uno o più account (ad esempio un inserzionista e un editore) durante la configurazione. Alcuni campi, ad esempio le risorse di branding e l&#39;e-mail di contatto, possono essere aggiornati successivamente nell&#39;area di lavoro **[!UICONTROL Impostazioni]**.

- **Assegna un ruolo** - Determina se il tuo account è un inserzionista o un editore. Il tuo ruolo definisce le funzionalità disponibili in Collaboration. Per ulteriori informazioni sull&#39;impatto dei ruoli sul flusso di lavoro di collaborazione, consulta la guida [roles](./overview/roles.md).
- **Risorse di branding** - Aggiungi quanto segue al tuo account:
   - Nome account (massimo 100 caratteri)
   - Descrizione (massimo 1.000 caratteri)
   - Logo (SVG &lt;20 KB, idealmente quadrato)

>[!NOTE]
>
>Se desideri essere visibile al pubblico nel catalogo delle connessioni di Collaboration durante la creazione di un account publisher, contatta il rappresentante del tuo account Adobe. Gli account dell’editore richiedono un banner personalizzato per il marchio (JPG 2688x1536); questo file può essere condiviso direttamente con il tuo rappresentante.

- **E-mail di contatto** - Fornisci un&#39;e-mail aziendale che i collaboratori potranno utilizzare dopo aver stabilito una connessione.
- **Configura chiavi di corrispondenza** - Seleziona gli identificatori utilizzati per la corrispondenza del pubblico.

Per ulteriori informazioni sulla configurazione iniziale dell&#39;account, tra cui la definizione dei ruoli, il caricamento delle risorse di branding e la configurazione delle chiavi di corrispondenza, consulta la [guida alla configurazione iniziale dell&#39;account](./setup/onboard-account.md#initial-account-setup){target="_blank"}.

Guarda questo video per una descrizione dettagliata della configurazione di un inserzionista, inclusa la creazione di account, il branding e la configurazione della chiave di corrispondenza.

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## Passaggio 3: tipi di pubblico di Source (da Experience Platform o da una sorgente cloud) {#source-audiences}

Una volta creato l’account e configurate le chiavi di branding e corrispondenza, puoi iniziare a selezionare i tipi di pubblico. Scegliere uno dei seguenti metodi di determinazione origine in base all&#39;archivio dati e alle esigenze aziendali.

### Opzione A: Source da Experience Platform

[Utilizza Collaboration per collegare una sandbox che contiene tipi di pubblico](./setup/onboard-audiences.md). Utilizza questo metodo self-service per fare riferimento a segmenti di pubblico esistenti dall&#39;interno della tua istanza di Experience Platform.

#### Configurare i tipi di pubblico

Configura il modo in cui i tipi di pubblico vengono preparati, abbinati e governati per essere utilizzati nelle connessioni.

- **Seleziona tipi di pubblico** *(solo Experience Platform)* - Scegli segmenti di pubblico con identificatori supportati.
- **Mappa le chiavi di corrispondenza** - Allinea i campi del pubblico con le chiavi di corrispondenza configurate.
- **Applica trasformazioni** - Se necessario, inserisci valori in testo normale (ad esempio e-mail).
- **Aggiornamenti pianificati** - Definisci la frequenza di aggiornamento (ad esempio, giornaliera).
- **Configura le impostazioni di consenso** - Determina quali profili possono essere inclusi nelle connessioni selezionando una modalità di consenso: consenso, rinuncia o nessuno.

>[!NOTE]
>
>Puoi aggiungere o rimuovere tipi di pubblico e aggiornare la pianificazione dell’aggiornamento direttamente in Collaboration. Per modificare altre impostazioni, ad esempio le chiavi di corrispondenza o la modalità di consenso, devi eliminare e ricreare la connessione dati.

>[!IMPORTANT]
>
>**Numero massimo di tipi di pubblico per ruolo di collaboratore:**
>
>- **Gli inserzionisti** possono creare fino a 25 tipi di pubblico.
>- **Gli editori** possono creare fino a 250 tipi di pubblico (ciascuno con un minimo di 1.000 ID).

>[!IMPORTANT]
>
>**Corrispondenza con i requisiti chiave:**
>
>Tutte le chiavi di corrispondenza devono essere **tagliate**, **in minuscolo**
>Le chiavi di corrispondenza con hash devono essere **SHA256-hash**.\
>Se fornisci valori con hash che utilizzano caratteri maiuscoli, Collaboration li converte automaticamente in minuscoli.\
>Se l&#39;origine contiene **identificatori di testo normale**, utilizzare l&#39;opzione **[!UICONTROL Applica trasformazione]** per applicare l&#39;hashing. Questa opzione è disponibile solo quando si selezionano i tipi di pubblico da Experience Platform e non è supportata per le origini basate su cloud.
>
>Per ulteriori informazioni, consulta la sezione [map fields](./setup/onboard-audiences.md#map-fields) della guida source and manage audiences.

Per visualizzare una procedura dettagliata su come individuare i tipi di pubblico utilizzando Collaboration, guarda il video seguente.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

In alternativa, consulta il documento su [tipi di pubblico di sourcing in Collaboration](./setup/onboard-audiences.md#source-and-manage-audiences).

### Opzione B: Source da Snowflake o Amazon S3

Per configurare un&#39;origine cloud, ad esempio [!DNL Snowflake] o [!DNL Amazon S3], preparare i dati del pubblico utilizzando [Specifiche del pubblico PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.1.pdf)

È possibile configurare [!DNL Amazon S3] come origine dati autonoma. Per istruzioni di installazione, consulta la [Guida all&#39;approvvigionamento di Amazon S3](./setup/configure-aws-s3-audience-sourcing.md)

Se utilizzi [!DNL Snowflake] o un altro provider di servizi cloud, contatta il rappresentante del tuo account Adobe per finalizzare la configurazione.

>[!IMPORTANT]
>
>I file del pubblico basati su cloud devono seguire lo schema richiesto descritto in Audience Specification PDF. I file devono includere identificatori con hash (SHA256 minuscolo), campi di metadati obbligatori come `segment_name` e `activation_id` e utilizzare formati supportati come CSV o Parquet. Adobe non normalizza i dati prima dell’attivazione. Il TTL viene applicato in base alla durata del pubblico.
>
>In questa fase, tutti i tipi di pubblico nel file caricato provengono da origini complete. L&#39;impostazione [visibilità pubblico](/help/guide/setup/onboard-audiences.md#metadata-visibility) determina se i collaboratori possono visualizzare il pubblico e viene gestita tramite l&#39;interfaccia utente di Collaboration.

## Passaggio 4: attivare i tipi di pubblico (su Experience Platform o una destinazione cloud) {#activate-audiences}

Quindi, attiva i tipi di pubblico nell’istanza di Experience Platform o in una destinazione cloud.

### Opzione A: Attivare Experience Platform

Completa i seguenti passaggi descritti nella guida [configurare Adobe Experience Platform come destinazione](/help/guide/destinations/experience-platform.md).

- **Crea una destinazione**. Utilizza l&#39;interfaccia utente per impostare una destinazione Experience Platform (a livello di sandbox).
- **Mappa chiavi corrispondenti** - Seleziona l&#39;identificatore (ad esempio, `hashedEmail`).
- **Definisci TTL** - Imposta scadenza (1-30 giorni).
- **Verifica in Audience Portal** - Dopo che un collaboratore ti ha inviato un pubblico, verifica che questo venga visualizzato in Audience Portal nell&#39;origine &quot;[!UICONTROL Real-Time CDP Collaboration].&quot;

### Opzione B: Attivare su cloud

Per configurare una destinazione cloud (ad esempio, [!DNL AWS S3] o [!DNL Snowflake]), contatta il rappresentante del tuo account Adobe per avviare il processo di configurazione. A seconda della destinazione cloud, dovrai fornire i dettagli della destinazione cloud come il percorso del file, le credenziali, i localizzatori dell’account, ecc. Una volta fornite le informazioni richieste, Adobe configurerà la configurazione della destinazione cloud.

I dati del pubblico inviati a una destinazione cloud seguono uno schema predefinito. Per una descrizione dettagliata dei campi e del formato richiesti, scarica la [Guida di Collaboration Audience Activation](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

## Passaggio 5: impostare la misurazione (facoltativo) {#set-up-measurement}

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile in **beta** ed è disponibile esclusivamente per i clienti del programma Disponibilità limitata. Contatta il tuo rappresentante Adobe per richiedere l’accesso.

>[!IMPORTANT]
>
>L&#39;area di lavoro **[!UICONTROL Measure]** è disponibile solo se il caso di utilizzo **[!UICONTROL Measurement]** è stato abilitato [durante il processo di connessione](./connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, consulta la guida [gestisci progetti](./collaborate/manage-projects.md#project-use-cases).

Collaboration offre una serie di rapporti per analizzare la portata, la frequenza e l’efficacia delle campagne. Anche se l&#39;area di lavoro **[!UICONTROL Measure]** è disponibile nell&#39;interfaccia utente, la funzionalità di reporting completa potrebbe richiedere l&#39;abilitazione del back-end.

Per informazioni su come visualizzare e interpretare i report di misurazione, vedere la [Guida alla misurazione](./collaborate/measure.md). Include informazioni sull’attribuzione, le metriche di riepilogo delle campagne e dashboard quali le curve di portata e la distribuzione della frequenza.

<!-- 
Commenting out the below information as this workflow is not yet in Beta but will be imminently. A guided measurement configuration workflow will be available in a future release."

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
   - Submit the report. It will run on the selected date and populate within 24 hours. 
-->

## Passaggio 6: Connettersi con i collaboratori {#connect-with-collaborators}

Al termine dell&#39;installazione, l&#39;organizzazione è ora pronta a connettersi con i collaboratori inviando o accettando inviti e inviando le impostazioni del progetto per l&#39;approvazione. Questo processo di connessione prevede l&#39;invio o la ricezione di inviti, la revisione e l&#39;invio di impostazioni di connessione (ad esempio casi d&#39;uso e consumo di credito) e la conferma della connessione.

Come inserzionista, utilizza l&#39;area di lavoro **[!UICONTROL Connetti]** nel menu di navigazione a sinistra per sfogliare gli editori disponibili. In alternativa, i collaboratori possono connettersi tra loro direttamente tramite [inviti di connessione privati](./connect/establishing-connections.md#private-connection-invite){target="_blank"}.

>[!NOTE]
>
>Attualmente, solo gli inserzionisti possono sfogliare gli editori. Gli editori non possono esplorare o avviare connessioni con gli inserzionisti.

Per una panoramica di questo flusso, vedere la [guida alla creazione delle connessioni](./connect/establishing-connections.md){target="_blank"}. Per una panoramica visiva del processo di connessione, inclusi la navigazione dei collaboratori e la gestione delle impostazioni di connessione, guarda il video di configurazione dell&#39;account dell&#39;inserzionista [&#128279;](https://experienceleague.adobe.com/it/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

## Passaggi successivi

Hai completato la configurazione iniziale e hai configurato l’organizzazione per una collaborazione sicura. Quindi, esplora le seguenti risorse per comprendere meglio i concetti di attivazione, misurazione e governance dei dati:

- [Documentazione del flusso di lavoro di Audience Activation](./collaborate/activate.md)
- [Casi di utilizzo della misurazione](./collaborate/measure.md)
- [Best practice per la governance di Collaboration](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
