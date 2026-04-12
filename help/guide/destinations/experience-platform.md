---
title: Configurare Adobe Experience Platform come destinazione
description: Scopri come configurare e gestire Adobe Experience Platform come destinazione in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
source-git-commit: 0dead396657c97cec47ddd64c8ec3c349f541a8f
workflow-type: tm+mt
source-wordcount: '1534'
ht-degree: 14%

---

# Configurare Adobe Experience Platform come destinazione

{{limited-availability-release-note}}

Configura questa destinazione per attivare il pubblico dal progetto a Adobe Experience Platform. L’attivazione dei tipi di pubblico in Adobe Experience Platform consente di sfruttare le funzionalità della piattaforma per la segmentazione, l’analisi e l’attivazione dei tipi di pubblico tra vari canali di marketing. Per ulteriori informazioni su Adobe Experience Platform, consulta la [panoramica di Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/landing/home){target="_blank"}.

>[!WARNING]
>
>Una volta creata, una destinazione non può essere aggiornata. Se devi modificare delle impostazioni, devi eliminare la destinazione esistente e crearne una nuova.

## Configurare la destinazione {#configure-destination}

Per configurare Adobe Experience Platform come destinazione, passare a **[!UICONTROL Configurazione]** e selezionare la scheda **[!UICONTROL Destinazioni personali]**. Selezionare **[!UICONTROL Configurazione]** per Adobe Experience Platform.

![L&#39;area di lavoro Destinazioni personali con l&#39;opzione Configura evidenziata per la destinazione Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/setup-aep.png)

Viene visualizzato il flusso di lavoro **[!UICONTROL Crea destinazione]**.

![Flusso di lavoro per la creazione della destinazione per Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/create-destination.png)

### Configurare la sandbox {#configure-sandbox}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="Scadenza pubblico"
>abstract="Il periodo di tempo dopo il quale il pubblico non sarà più disponibile in Adobe Experience Platform. La scadenza predefinita è di 30 giorni, ma è possibile impostarla su qualsiasi valore compreso tra 1 e 30 giorni."

Innanzitutto, devi selezionare la sandbox in cui verranno inviati i dati sul pubblico.

>[!IMPORTANT]
>
>Puoi selezionare solo una sandbox a cui l’utente ha accesso. Per impostazione predefinita, tutti gli utenti di Collaboration hanno accesso alla sandbox **Prod**. Per poter accedere ad altre sandbox, un amministratore deve aggiungere altre sandbox a un ruolo assegnato al tuo utente. Per ulteriori informazioni sulla gestione dei ruoli, fare riferimento alla guida [gestione ruoli](../permissions/manage-roles.md).

Nella sezione **[!UICONTROL Configura sandbox]**, seleziona il menu a discesa **[!UICONTROL Sandbox]** o digita il nome di una sandbox.

![Il menu a discesa Sandbox è evidenziato nel flusso di lavoro Crea destinazione.](/help/assets/destinations/adobe-experience-platform/select-sandbox.png)

In alternativa, è possibile selezionare **[!UICONTROL Sfoglia sandbox]** per visualizzare tutte le sandbox disponibili e le relative **[!UICONTROL Tipo]**, **[!UICONTROL Stato]** e **[!UICONTROL Area]**. Select the sandbox that you want to use, and then select **[!UICONTROL Save]**.

Next, configure the **[!UICONTROL Audience Expiration]**. By default, the audience expiration is set to 30 days. You can choose to set the expiration anywhere from 1 to 30 days. After the expiration date, the audience will no longer be available in Adobe Experience Platform.

![The Audience Expiration section highlighted in the Create destination workflow.](/help/assets/destinations/adobe-experience-platform/audience-expiration.png)

### Creare la mappatura di attivazione {#create-activation-mapping}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_matchkeys"
>title="Chiavi di corrispondenza dell’attivazione"
>abstract="Le chiavi di corrispondenza dell’attivazione vengono visualizzate in base a quelle selezionate al momento della creazione dell’organizzazione."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_mapping"
>title="Maggiori informazioni"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="Spazi dei nomi di destinazione"
>abstract="Gli spazi dei nomi di destinazione specificano a quale spazio dei nomi di identità verrà mappata la chiave di corrispondenza in Adobe Experience Platform. Le chiavi di corrispondenza con hash devono essere mappate a uno spazio dei nomi di destinazione che supporta i valori con hash."

All match keys enabled for your account are included in the activation mapping by default. If you do not wish to directly map a match key to a target nampespace, you can use the linked key option to replace it with a different match key. For more information about linked keys, see the [section below](#linked-keys).

#### Map target namespaces {#map-target-namespaces}

To map each match key to a target namespace, select the **[!UICONTROL Target namespaces]** field next to the match key. The **[!UICONTROL Select source field]** dialog appears. Find the target namespace in the list, or search for a specific namespace. Select the target namespace that you want to use for the match key, and then select **[!UICONTROL Select]**.

>[!IMPORTANT]
>
>Le chiavi di corrispondenza con hash devono essere mappate a uno spazio dei nomi di destinazione che supporta i valori con hash. For example, the **[!UICONTROL Hashed email]** match key must be mapped to the **[!UICONTROL Email(SHA256, lowercased)]** identity namespace in Adobe Experience Platform. You cannot map the **[!UICONTROL Hashed email]** match key to the **[!UICONTROL Email]** identity namespace, as this namespace does not support hashed values.

![The Select source field dialog with the Select option highlighted..](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

Repeat this process for each match key that you want to include in the activation mapping. If you do not wish to include a match key, you can remove it, or use the linked key option to replace it with a different match key.

#### Chiavi collegate {#linked-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_linked_key"
>title="Chiave collegata"
>abstract="Le chiavi collegate consentono di specificare che, durante l’attivazione, dovrà essere utilizzata una chiave di corrispondenza diversa da quella originale. Per poter essere attivato, un profilo deve avere valori sia per la chiave di corrispondenza originale, sia per quella collegata."

Le chiavi collegate consentono di specificare che, durante l’attivazione, dovrà essere utilizzata una chiave di corrispondenza diversa da quella originale. To better understand how linked keys work, consider the following example:

A retailer wishes to send the data being activated to Experience Platform to their CRM system. The retailer has enabled Hashed IP as a match key for their account to increase the match rate when activating audiences. However, the retailer’s CRM system does not support Hashed IP as an identity namespace, so they want to use the CRM ID match key instead when activating audiences to Experience Platform. The retailer can use the linked key option to activate audiences to Experience Platform using CRM ID instead of Hashed IP.

>[!NOTE]
>
>Per poter essere attivato, un profilo deve avere valori sia per la chiave di corrispondenza originale, sia per quella collegata. For example, if Hashed ID is linked to CRM ID, a profile must have values for both Hashed ID and CRM ID to be activated. If either value is missing, the profile will not be activated.

To use a linked key, toggle on the **[!UICONTROL Linked key]** option next to the match key that you want to use in its place. The **[!UICONTROL Linked key]** section appears asking you to create the mapping.

![The Linked key option and section highlighted in the Create destination workflow.](/help/assets/destinations/adobe-experience-platform/linked-key.png)

Select the **[!UICONTROL Linked key]** that you want to use from the dropdown menu. Following the above example, the retailer would select **[!UICONTROL CRM ID]** as the linked key.

![The Linked key dropdown highlighted in the Create destination workflow.](/help/assets/destinations/adobe-experience-platform/select-linked-key.png)

Next, you want to specify the target namespace for the linked key if you have not already done so. If you&#39;ve already selected the target namespace for the match key in the **[!UICONTROL Create activation mapping]** section, this will be autopopulated. If you have not yet selected a target namespace for the linked key, you can do so now.

Select the **[!UICONTROL Target namespaces]** field next to the linked key. The **[!UICONTROL Select source field]** dialog appears. Find the target namespace in the list, or search for a specific namespace. Select the target namespace that you want to use for the linked key, and then select **[!UICONTROL Select]**.

![The Select source field dialog.](/help/assets/destinations/adobe-experience-platform/select-linked-key-target-namespace.png)

The linked key is now configured.

>[!NOTE]
>
>You can only used one linked key target namespace per activation mapping. For example, if you link Hashed ID to CRM ID, toggling on the linked key option for another field will also link it to CRM ID.

When you&#39;ve finished mapping all match keys, review your settings. The **[!UICONTROL Preview]** section provides a summary of your configuration.

![The Preview section in the Create destination workflow.](/help/assets/destinations/adobe-experience-platform/preview.png)

>[!IMPORTANT]
>
>Currently, each match key activates to Experience Platform as a separate audience. For example, if you have [!UICONTROL Hashed email] and [!UICONTROL Hashed phone] as match keys, two separate audiences will be created in Audience Portal when an audience is activated.

When you&#39;re satisfied with your configuration, select **[!UICONTROL Create destination]**. A confirmation message appears indicating that the destination was created successfully.

## Utilizzo di Adobe Experience Platform come destinazione

Dopo aver configurato Experience Platform come destinazione, puoi iniziare a [attivare i tipi di pubblico](../collaborate/activate.md) nella piattaforma tramite i tuoi progetti. Attualmente, il processo di attivazione è un processo in un unico passaggio avviato dal collaboratore. Ad esempio, quando un inserzionista attiva un pubblico, questo viene inviato alla destinazione preconfigurata dell’editore (Experience Platform). L’editore non deve effettuare alcuna operazione aggiuntiva per inviare il pubblico alla destinazione. Lo stesso vale per il modello di collaborazione brand-to-brand.

>[!IMPORTANT]
>
>**devi** configurare Experience Platform come destinazione *prima* che il tuo collaboratore attivi un pubblico. Se la destinazione non è configurata, il pubblico verrà inviato all&#39;utente e sarà visibile nella scheda **[!UICONTROL Attiva]** all&#39;interno di un progetto, ma non verrà attivato in Experience Platform.

Dopo l&#39;attivazione, il pubblico sarà disponibile in [Audience Portal](#audience-portal) in Experience Platform con Real-Time CDP Collaboration come origine.  Questi tipi di pubblico possono quindi essere utilizzati nelle campagne e nel coinvolgimento dei clienti.

### Audience Portal {#audience-portal}

Dopo aver configurato Adobe Experience Platform come destinazione, puoi visualizzare i tipi di pubblico attivati nel Portale pubblico. Audience Portal è un hub centrale all’interno di Adobe Experience Platform che consente di visualizzare e gestire i tipi di pubblico. Audience Portal ora fornisce Real-Time CDP Collaboration come origine per filtrare i tipi di pubblico.

>[!IMPORTANT]
>
>È tua responsabilità applicare tutte le etichette di utilizzo dei dati necessarie ai tipi di pubblico attivati in Adobe Experience Platform. Per ulteriori informazioni, consulta la guida [etichette di utilizzo dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

![Il portale del pubblico con Real-Time CDP Collaboration come origine nelle opzioni di filtro.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

Per ulteriori informazioni su Audience Portal, consulta la guida [Panoramica di Audience Portal](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"}.
