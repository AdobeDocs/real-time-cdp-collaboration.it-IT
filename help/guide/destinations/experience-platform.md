---
title: Configurare Adobe Experience Platform come destinazione
description: Scopri come configurare e gestire Adobe Experience Platform come destinazione in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 11%

---

# Configurare Adobe Experience Platform come destinazione

{{limited-availability-release-note}}

Configura questa destinazione per attivare il pubblico dal progetto a Adobe Experience Platform. L’attivazione dei tipi di pubblico in Adobe Experience Platform consente di sfruttare le funzionalità della piattaforma per la segmentazione, l’analisi e l’attivazione dei tipi di pubblico tra vari canali di marketing. Per ulteriori informazioni su Adobe Experience Platform, consulta la [panoramica di Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/home){target="_blank"}.

>[!NOTE]
>
>Attualmente, solo gli editori possono configurare le destinazioni in Adobe Real-Time CDP Collaboration.

## Configurare la destinazione {#configure-destination}

Per configurare Adobe Experience Platform come destinazione, passare a **[!UICONTROL Configurazione]** e selezionare la scheda **[!UICONTROL Destinazioni]**. Selezionare **[!UICONTROL Configurazione]** per Adobe Experience Platform.

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
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="Spazi dei nomi di destinazione"
>abstract="Gli spazi dei nomi di destinazione specificano a quale spazio dei nomi di identità verrà mappata la chiave di corrispondenza in Adobe Experience Platform. Le chiavi di corrispondenza con hash devono essere mappate a uno spazio dei nomi di destinazione che supporta i valori con hash."

Successivamente, devi creare una mappatura di attivazione per definire come verranno inviati i dati sul pubblico a Adobe Experience Platform. Puoi mappare ogni [chiave corrispondente](../setup/onboard-account.md#set-up-match-keys) selezionata durante la creazione dell&#39;organizzazione su uno spazio dei nomi di destinazione. Gli spazi dei nomi di destinazione specificano a quale [spazio dei nomi identità](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} verrà mappata la chiave di corrispondenza in Adobe Experience Platform.

>[!IMPORTANT]
>
>Le chiavi di corrispondenza con hash devono essere mappate a uno spazio dei nomi di destinazione che supporta i valori con hash. Ad esempio, la chiave di corrispondenza per l&#39;**[!UICONTROL e-mail con hash]** deve essere mappata allo spazio dei nomi dell&#39;identità **[!UICONTROL E-mail(SHA256, in minuscolo)]** in Adobe Experience Platform. Impossibile mappare la chiave di corrispondenza **[!UICONTROL Hashed e-mail]** allo spazio dei nomi dell&#39;identità **[!UICONTROL E-mail]**, poiché questo spazio dei nomi non supporta valori con hash.

Seleziona il campo **[!UICONTROL Spazi dei nomi di destinazione]** accanto a ciascuna chiave di corrispondenza. Viene visualizzata la finestra di dialogo **[!UICONTROL Seleziona campo di origine]**. Trovare lo spazio dei nomi di destinazione nell&#39;elenco o cercare uno spazio dei nomi specifico. Selezionare lo spazio dei nomi di destinazione da utilizzare per la chiave di corrispondenza, quindi selezionare **[!UICONTROL Seleziona]**.

![Finestra di dialogo Seleziona campo di origine con l&#39;opzione Seleziona evidenziata..](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

Dopo aver completato la mappatura di tutte le chiavi di corrispondenza, controlla le impostazioni e seleziona **[!UICONTROL Crea]** per completare la creazione della destinazione.

## Utilizzo di Adobe Experience Platform come destinazione

Dopo aver configurato Adobe Experience Platform come destinazione, puoi iniziare a [attivare i tipi di pubblico](../collaborate/activate.md) nella piattaforma tramite i tuoi progetti. Attualmente, il processo di attivazione è un processo in un unico passaggio avviato dall’inserzionista. Quando l&#39;inserzionista attiva un pubblico, questo viene inviato alla destinazione preconfigurata dell&#39;editore (in questo caso, Adobe Experience Platform). L’editore non deve effettuare alcuna operazione aggiuntiva per inviare il pubblico alla destinazione.

>[!IMPORTANT]
>
>**devi** configurare Adobe Experience Platform come destinazione *prima* che il tuo collaboratore attivi un pubblico. Se la destinazione non è configurata, il pubblico verrà inviato all&#39;utente e sarà visibile nella scheda **[!UICONTROL Attiva]** all&#39;interno di un progetto, ma non verrà attivato in Adobe Experience Platform.

Dopo l&#39;attivazione, il pubblico sarà disponibile in [Audience Portal](#audience-portal) in Experience Platform con Real-Time CDP Collaboration come origine.  Questi tipi di pubblico possono quindi essere utilizzati nelle campagne e nel coinvolgimento dei clienti.

### Audience Portal {#audience-portal}

Dopo aver configurato Adobe Experience Platform come destinazione, puoi visualizzare i tipi di pubblico attivati nel Portale pubblico. Audience Portal è un hub centrale all’interno di Adobe Experience Platform che consente di visualizzare e gestire i tipi di pubblico. Audience Portal ora fornisce Real-Time CDP Collaboration come origine per filtrare i tipi di pubblico.

>[!IMPORTANT]
>
>È tua responsabilità applicare tutte le etichette di utilizzo dei dati necessarie ai tipi di pubblico attivati in Adobe Experience Platform. Per ulteriori informazioni, consulta la guida [etichette di utilizzo dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

![Il portale del pubblico con Real-Time CDP Collaboration come origine nelle opzioni di filtro.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

Per ulteriori informazioni su Audience Portal, consulta la guida [Panoramica di Audience Portal](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"}.
