---
title: Guida rapida e configurazione di Real-Time CDP Collaboration
description: Scopri come configurare Real-Time CDP Collaboration, ruoli e account, impostare le origini dei tipi di pubblico, attivare i dati e connetterti con i partner in modo sicuro.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
TQID: https://experienceleague.adobe.com/rhIArZZm0Thkj3E-qiHtVHO6qxpr1vd-Qs4hWt4tf1U
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2: id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1417
ht-degree: 2%

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
- (Facoltativo) Accedi a un’origine cloud supportata (Amazon S3, Google Cloud Storage o Snowflake) se non utilizzi Experience Platform per la gestione dell’audience.

## Passaggio 1: completare la configurazione basata sui ruoli {#complete-role-based-setup}

I ruoli di accesso della tua organizzazione determinano ciò che gli utenti possono vedere e fare in Collaboration. Prima di procedere, assicurati che le autorizzazioni basate sul ruolo siano configurate correttamente per garantire l’accesso e la visibilità appropriati nella piattaforma.

**Risorse:**

- [Documentazione di accesso utente](./permissions/manage-user-access.md)
- [Documentazione sulla configurazione dei ruoli](./permissions/manage-roles.md)


Guarda questo video per scoprire come assegnare l’accesso ai prodotti e le autorizzazioni per Collaboration utilizzando Admin Console e Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3452216/?learn=on&enablevpops)

## Passaggio 2: configurare l’account Collaboration {#set-up-your-account}

Prima di poter individuare i tipi di pubblico, è necessario configurare l’account in Collaboration. Questo governa il modo in cui apparisci e gli elementi a cui hai accesso nell’interfaccia.

Se non disponi dell’accesso necessario, fai riferimento al passaggio 1 o contatta l’amministratore della tua organizzazione per assistenza al completamento della configurazione.

Definisci il ruolo del tuo account in Collaboration, fornisci risorse di branding e configura chiavi di corrispondenza per allineare i tipi di pubblico tra le connessioni.

>[!NOTE]
>
>Puoi creare uno o più account (ad esempio un inserzionista e un editore) durante la configurazione. Certain fields, like branding assets and contact email, can be updated later in the **[!UICONTROL Settings]** workspace.

- **Assign a role** – Determines whether your account is an advertiser or a publisher. Your role defines which capabilities you have in Collaboration. To learn more about how roles impact the collaboration workflow, see the [roles](./overview/roles.md) guide.
- **Branding assets** – Add the following to your account:
   - Account name (max 100 characters)
   - Description (max 1,000 characters)
   - Logo (SVG &lt;20KB, ideally square)

>[!NOTE]
>
>If you&#39;re creating a publisher account and would like to be publicly visible in Collaboration&#39;s connections catalog, please contact your Adobe account representative. Publisher accounts require a custom brand banner (JPG 2688x1536); this file can be shared directly with your representative.

- **Contact email** – Provide a business email for collaborators to use after a connection is established.
- **Configure match keys** – Select the identifiers used for audience matching.

To learn more about initial account setup, including how to define roles, upload branding assets, and configure match keys, see the [initial account setup](./setup/onboard-account.md#initial-account-setup){target="_blank"} guide.

Watch this video for a step-by-step walkthrough of an advertiser setup, including account creation, branding, and match key configuration.

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## Step 3: Source audiences (from Experience Platform or a cloud source) {#source-audiences}

Once your account is created and your branding and match keys are configured, you&#39;re ready to begin sourcing audiences. Choose one of the following sourcing methods based on your data store and business needs.

### Option A: Source from Experience Platform

[Use Collaboration to link a sandbox that contains audiences](./setup/onboard-audiences.md). Use this self-service method to reference existing audience segments from within your Experience Platform instance.

#### Configure audiences

Configure how audiences are prepared, matched, and governed for use in connections.

- **Select audiences** *(Experience Platform only)* – Choose audience segments with supported identifiers.
- **Map match keys** – Align audience fields with the configured match keys.
- **Apply transformations** – Hash plaintext values (for example, email) if needed.
- **Schedule refreshes** – Define update frequency (for example, daily).
- **Configure consent settings** – Determine which profiles are eligible to be included in connections by selecting a consent mode: opt-in, opt-out, or none.

>[!NOTE]
>
>You can add or remove audiences and update the refresh schedule directly in Collaboration. To change other settings, such as match keys or consent mode, you must delete and recreate the data connection.

>[!IMPORTANT]
>
>**Maximum number of audiences per collaborator role:**
>
>- **Advertisers** can source up to 25 audiences.
>- **Publishers** can source up to 250 audiences (each with a minimum of 1,000 IDs).

>[!IMPORTANT]
>
>**Match key requirements:**
>
>All match keys must be **trimmed**, **lowercased**
>Le chiavi di corrispondenza con hash devono essere **SHA256-hash**.\
>Se fornisci valori con hash che utilizzano caratteri maiuscoli, Collaboration li converte automaticamente in minuscoli.\
>If your source contains **plaintext identifiers**, use the **[!UICONTROL Apply transformation]** option to apply hashing. Questa opzione è disponibile solo quando si selezionano i tipi di pubblico da Experience Platform e non è supportata per le origini basate su cloud.
>
>For more information, see the [map fields](./setup/onboard-audiences.md#map-fields) section of the source and manage audiences guide.

To see a full walkthrough of how to source audiences using Collaboration, watch the video below.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

Alternatively, see the document on [sourcing audiences in Collaboration](./setup/onboard-audiences.md#source-and-manage-audiences).

### Option B: Source from Snowflake, Amazon S3, or Google Cloud Storage

To configure a cloud source, such as [!DNL Snowflake], [!DNL Amazon S3], or [!DNL Google Cloud Storage], prepare your audience data using the [Audience Specification PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)

You can configure [!DNL Amazon S3], [!DNL Google Cloud Storage], or [!DNL Snowflake] as self-service data sources. For setup instructions, see the [Amazon S3 sourcing guide](./setup/configure-aws-s3-audience-sourcing.md), the [GCS sourcing guide](./setup/configure-gcs-audience-sourcing.md), or the [Snowflake sourcing guide](./setup/configure-snowflake-audience-sourcing.md).

For other cloud service providers, contact your Adobe account representative to finalize the setup.

>[!IMPORTANT]
>
>Cloud-based audience files must follow the required schema outlined in the Audience Specification PDF. Files must include hashed identifiers (lowercased SHA256), required metadata fields such as `segment_name` and `activation_id`, and use supported formats such as CSV or Parquet. Adobe does not normalize data before activation. TTL is enforced based on the audience&#39;s lifespan.
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

Per una panoramica di questo flusso, vedere la [guida alla creazione delle connessioni](./connect/establishing-connections.md){target="_blank"}. Per una panoramica visiva del processo di connessione, inclusi la navigazione dei collaboratori e la gestione delle impostazioni di connessione, guarda il video di configurazione dell&#39;account dell&#39;inserzionista [](https://experienceleague.adobe.com/it/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

## Passaggi successivi

Hai completato la configurazione iniziale e hai configurato l’organizzazione per una collaborazione sicura. Quindi, esplora le seguenti risorse per comprendere meglio i concetti di attivazione, misurazione e governance dei dati:

- [Documentazione del flusso di lavoro di Audience Activation](./collaborate/activate.md)
- [Casi di utilizzo della misurazione](./collaborate/measure.md)
- [Best practice per la governance di Collaboration](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
