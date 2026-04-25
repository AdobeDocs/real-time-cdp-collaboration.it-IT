---
title: Configurare Adobe Experience Platform come destinazione
description: Scopri come configurare e gestire Adobe Experience Platform come destinazione in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
TQID: https://experienceleague.adobe.com/vOAlNzIaEKC6cZC-zMxShPTn77kmV3WbUuvZU8Svzh4
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1534
ht-degree: 14%

---

# Configurare Adobe Experience Platform come destinazione

{{limited-availability-release-note}}

Configura questa destinazione per attivare il pubblico dal progetto a Adobe Experience Platform. L’attivazione dei tipi di pubblico in Adobe Experience Platform consente di sfruttare le funzionalità della piattaforma per la segmentazione, l’analisi e l’attivazione dei tipi di pubblico tra vari canali di marketing. Per ulteriori informazioni su Adobe Experience Platform, consulta la [panoramica di Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/home){target="_blank"}.

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

In alternativa, è possibile selezionare **[!UICONTROL Sfoglia sandbox]** per visualizzare tutte le sandbox disponibili e le relative **[!UICONTROL Tipo]**, **[!UICONTROL Stato]** e **[!UICONTROL Area]**. Selezionare la sandbox da utilizzare, quindi selezionare **[!UICONTROL Salva]**.

Quindi, configura **[!UICONTROL Scadenza pubblico]**. Per impostazione predefinita, la scadenza del pubblico è impostata su 30 giorni. Puoi scegliere di impostare la scadenza tra 1 e 30 giorni. Dopo la data di scadenza, il pubblico non sarà più disponibile in Adobe Experience Platform.

![La sezione Scadenza pubblico è evidenziata nel flusso di lavoro Crea destinazione.](/help/assets/destinations/adobe-experience-platform/audience-expiration.png)

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

Per impostazione predefinita, tutte le chiavi di corrispondenza abilitate per l’account sono incluse nella mappatura di attivazione. Se non desideri mappare direttamente una chiave di corrispondenza a uno spazio dei nomi di destinazione, puoi utilizzare l’opzione della chiave collegata per sostituirla con una chiave di corrispondenza diversa. Per ulteriori informazioni sulle chiavi collegate, vedere la [sezione seguente](#linked-keys).

#### Mappare gli spazi dei nomi di destinazione {#map-target-namespaces}

Per mappare ogni chiave di corrispondenza a uno spazio dei nomi di destinazione, seleziona il campo **[!UICONTROL Spazi dei nomi di destinazione]** accanto alla chiave di corrispondenza. Viene visualizzata la finestra di dialogo **[!UICONTROL Seleziona campo di origine]**. Trovare lo spazio dei nomi di destinazione nell&#39;elenco o cercare uno spazio dei nomi specifico. Selezionare lo spazio dei nomi di destinazione da utilizzare per la chiave di corrispondenza, quindi selezionare **[!UICONTROL Seleziona]**.

>[!IMPORTANT]
>
>Le chiavi di corrispondenza con hash devono essere mappate a uno spazio dei nomi di destinazione che supporta i valori con hash. Ad esempio, la chiave di corrispondenza per l&#39;**[!UICONTROL e-mail con hash]** deve essere mappata allo spazio dei nomi dell&#39;identità **[!UICONTROL E-mail(SHA256, in minuscolo)]** in Adobe Experience Platform. Impossibile mappare la chiave di corrispondenza **[!UICONTROL Hashed e-mail]** allo spazio dei nomi dell&#39;identità **[!UICONTROL E-mail]**, poiché questo spazio dei nomi non supporta valori con hash.

![Finestra di dialogo Seleziona campo di origine con l&#39;opzione Seleziona evidenziata..](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

Ripeti questo processo per ogni chiave di corrispondenza da includere nella mappatura di attivazione. Se non desideri includere una chiave di corrispondenza, puoi rimuoverla o utilizzare l’opzione della chiave collegata per sostituirla con una chiave di corrispondenza diversa.

#### Chiavi collegate {#linked-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_linked_key"
>title="Chiave collegata"
>abstract="Le chiavi collegate consentono di specificare che, durante l’attivazione, dovrà essere utilizzata una chiave di corrispondenza diversa da quella originale. Per poter essere attivato, un profilo deve avere valori sia per la chiave di corrispondenza originale, sia per quella collegata."

Le chiavi collegate consentono di specificare che, durante l’attivazione, dovrà essere utilizzata una chiave di corrispondenza diversa da quella originale. Per comprendere meglio il funzionamento delle chiavi collegate, considera l’esempio seguente:

Un retailer desidera inviare i dati attivati ad Experience Platform al proprio sistema di gestione delle relazioni con i clienti. Retailer ha abilitato l’IP con hash come chiave di corrispondenza per il proprio account per aumentare la percentuale di corrispondenza quando si attivano i tipi di pubblico. Tuttavia, il sistema CRM di retailer non supporta l’IP con hash come spazio dei nomi di identità, pertanto desidera utilizzare la chiave di corrispondenza dell’ID del sistema CRM invece di attivare i tipi di pubblico in Experience Platform. Retailer può utilizzare l’opzione della chiave collegata per attivare i tipi di pubblico in Experience Platform utilizzando l’ID del sistema di gestione delle relazioni con i clienti invece dell’IP con hash.

>[!NOTE]
>
>Per poter essere attivato, un profilo deve avere valori sia per la chiave di corrispondenza originale, sia per quella collegata. Ad esempio, se l’ID con hash è collegato all’ID del sistema di gestione delle relazioni con i clienti, un profilo deve avere valori sia per l’ID con hash che per l’ID del sistema di gestione delle relazioni con i clienti da attivare. Se manca uno dei due valori, il profilo non verrà attivato.

Per utilizzare una chiave collegata, attiva l&#39;opzione **[!UICONTROL Chiave collegata]** accanto alla chiave di corrispondenza che desideri utilizzare al suo posto. Viene visualizzata la sezione **[!UICONTROL Chiave collegata]** che richiede di creare la mappatura.

![L&#39;opzione chiave collegata e la sezione evidenziate nel flusso di lavoro Crea destinazione.](/help/assets/destinations/adobe-experience-platform/linked-key.png)

Selezionare la **[!UICONTROL chiave collegata]** che si desidera utilizzare dal menu a discesa. In base all&#39;esempio precedente, retailer selezionerà **[!UICONTROL ID CRM]** come chiave collegata.

![L&#39;elenco a discesa della chiave Collegata è evidenziato nel flusso di lavoro Crea destinazione.](/help/assets/destinations/adobe-experience-platform/select-linked-key.png)

Quindi, se non lo hai già fatto, specifica lo spazio dei nomi di destinazione per la chiave collegata. Se hai già selezionato lo spazio dei nomi di destinazione per la chiave di corrispondenza nella sezione **[!UICONTROL Crea mapping di attivazione]**, verrà popolato automaticamente. Se non hai ancora selezionato uno spazio dei nomi di destinazione per la chiave collegata, puoi farlo ora.

Seleziona il campo **[!UICONTROL Spazi dei nomi di destinazione]** accanto alla chiave collegata. Viene visualizzata la finestra di dialogo **[!UICONTROL Seleziona campo di origine]**. Trovare lo spazio dei nomi di destinazione nell&#39;elenco o cercare uno spazio dei nomi specifico. Selezionare lo spazio dei nomi di destinazione da utilizzare per la chiave collegata, quindi selezionare **[!UICONTROL Seleziona]**.

![Finestra di dialogo Seleziona campo di origine.](/help/assets/destinations/adobe-experience-platform/select-linked-key-target-namespace.png)

La chiave collegata è ora configurata.

>[!NOTE]
>
>È possibile utilizzare un solo spazio dei nomi di destinazione chiave collegato per ogni mappatura di attivazione. Ad esempio, se colleghi l’ID con hash all’ID del sistema di gestione delle relazioni con i clienti, l’attivazione dell’opzione della chiave collegata per un altro campo lo collegherà anche all’ID del sistema di gestione delle relazioni con i clienti.

Una volta completata la mappatura di tutte le chiavi di corrispondenza, controlla le impostazioni. La sezione **[!UICONTROL Anteprima]** fornisce un riepilogo della configurazione.

![Sezione Anteprima nel flusso di lavoro Crea destinazione.](/help/assets/destinations/adobe-experience-platform/preview.png)

>[!IMPORTANT]
>
>Attualmente, ogni chiave di corrispondenza si attiva ad Experience Platform come pubblico separato. Ad esempio, se hai [!UICONTROL e-mail con hash] e [!UICONTROL telefono con hash] come chiavi di corrispondenza, verranno creati due tipi di pubblico separati in Audience Portal quando viene attivato un pubblico.

Quando sei soddisfatto della tua configurazione, seleziona **[!UICONTROL Crea destinazione]**. Viene visualizzato un messaggio di conferma che indica che la destinazione è stata creata correttamente.

## Using Adobe Experience Platform as a destination

Once you&#39;ve configured Experience Platform as a destination, you can begin [activating audiences](../collaborate/activate.md) to the platform through your projects. Currently, the activation process is a single-step process initiated by the collaborator. For example, when an advertiser activates an audience, it is sent to the publisher’s pre-configured destination (Experience Platform). The publisher does not need to take any additional steps to send the audience to the destination. The same holds true for the brand-to-brand collaboration pattern.

>[!IMPORTANT]
>
>You **must** configure Experience Platform as a destination *before* your collaborator activates an audience. If the destination is not configured, the audience will be sent to you and visible in the **[!UICONTROL Activate]** tab within a project, but will not be activated to Experience Platform.

After the audience is activated, it will be available in [Audience Portal](#audience-portal) in Experience Platform with Real-Time CDP Collaboration as the origin.  These audiences can then be used in campaigns and customer engagement.

### Audience Portal {#audience-portal}

Now that you have configured Adobe Experience Platform as a destination, you can view the activated audiences in the Audience Portal. Audience Portal is a central hub within Adobe Experience Platform that allows you to view and manage your audiences. Audience portal now provides Real-Time CDP Collaboration as an origin when filtering your audiences.

>[!IMPORTANT]
>
>You are responsible for applying any necessary data usage labels to the audiences you activate to Adobe Experience Platform. For more information, refer to the [data usage labels](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/overview){target="_blank"} guide.

![The Audience Portal with Real-Time CDP Collaboration as an origin in the filter options.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

To learn more about Audience Portal, refer to the [Audience Portal overview](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"} guide.
