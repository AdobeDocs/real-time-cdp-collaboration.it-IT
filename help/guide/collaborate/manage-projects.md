---
title: Creare e gestire i progetti
description: Scopri come creare e gestire i progetti in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: ae492846-bc0a-4422-86ca-577bcc1fa60c
TQID: https://experienceleague.adobe.com/IZIkK4lv29vqrah48fsJsnMOFtyh7rOo1IT2yLOW9Ec
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2: id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 680
ht-degree: 11%

---

# Creare e gestire i progetti

{{limited-availability-release-note}}

I progetti sono il fulcro del flusso di lavoro in Adobe Real-Time CDP Collaboration. Dopo aver stabilito la connessione con i collaboratori, crea un progetto per eseguire i calcoli di sovrapposizione dei tipi di pubblico e scoprire i tipi di pubblico rilevanti per le campagne.

>[!TIP]
>
>I progetti devono in genere essere associati a una singola campagna.

![Il dashboard Collaborazione visualizza tutti i progetti correnti.](/help/assets/collaborate/manage-view-projects/projects-overview-page.png){zoomable="yes"}

Puoi utilizzare i filtri per visualizzare solo i progetti avviati con alcuni collaboratori, come illustrato di seguito:

![Visualizzazione filtrata dei progetti con un unico collaboratore.](/help/assets/collaborate/manage-view-projects/filtered-project-view.png){zoomable="yes"}

## Crea progetto {#create-project}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_create_project_advertisername_amc"
>title="Nome inserzionista (Amazon Marketing Cloud)"
>abstract="Per le connessioni Amazon Marketing Cloud (AMC), questo campo rappresenta l’istanza di AMC a cui il tuo account Amazon Ads può accedere. Non rispecchia il nome di un inserzionista. Se l’istanza richiesta non è elencata, contatta il tuo amministratore Amazon Marketing Cloud per richiedere l’accesso."

Per creare un progetto, devi prima [stabilire una connessione](/help/guide/connect/establishing-connections.md) con un collaboratore. Una volta stabilita la connessione, puoi creare un progetto con quel collaboratore.

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_projects_advertisername"
>title="Nome inserzionista"
>abstract="Seleziona il nome dell’inserzionista dal menu a discesa. Le opzioni sono preconfigurate dall’editore nelle impostazioni di connessione per garantire la compatibilità con i suoi sistemi."

Passa a **[!UICONTROL Collabora]** e quindi a **[!UICONTROL Progetti personali]**. Se si tratta del primo progetto, è possibile selezionare **[!UICONTROL Crea un progetto]**. In caso contrario, è possibile selezionare l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) per creare un nuovo progetto in qualsiasi momento.

![Selezionare il simbolo più o creare un progetto per impostare un nuovo progetto.](/help/assets/collaborate/manage-view-projects/create-project.png){zoomable="yes"}

Viene visualizzata la finestra di dialogo **[!UICONTROL Crea progetto]**. Selezionare **[!UICONTROL Collaborator]** con cui si sta creando il progetto tramite il menu a discesa. Se sei un editore e hai impostato i nomi degli inserzionisti durante la configurazione della connessione, puoi selezionare **[!UICONTROL Nome inserzionista]**.

>[!NOTE]
>
> Se hai configurato un singolo nome dell’inserzionista nelle impostazioni di connessione, questo viene visualizzato per impostazione predefinita. Se non è stato impostato alcun nome di inserzionista, il **[!UICONTROL Nome]** dell&#39;inserzionista viene preselezionato come **[!UICONTROL Nome inserzionista]**.

![Finestra di dialogo Crea progetto con il collaboratore selezionato e il nome dell&#39;inserzionista evidenziato.](/help/assets/collaborate/manage-view-projects/create-project-advertiser-names.png){zoomable="yes"}

Quindi, aggiungi **[!UICONTROL Nome progetto]** e **[!UICONTROL Descrizione]** per il progetto. Quindi, seleziona un’immagine che rappresenti il progetto. Questa immagine aiuta a distinguere il progetto nella pagina di panoramica del progetto. Al termine, seleziona **[!UICONTROL Crea]** per creare il progetto.

![Opzioni necessarie per impostare un nuovo progetto](/help/assets/collaborate/manage-view-projects/create-project-required-info.png){zoomable="yes"}

Ora puoi visualizzare il nuovo progetto, i relativi dettagli e le sezioni disponibili in base ai casi d’uso selezionati durante la configurazione della connessione.

![Area di lavoro panoramica progetto.](/help/assets/collaborate/manage-view-projects/project-overview.png){zoomable="yes"}

## Gestisci ID campagna {#manage-campaign-id}

Un **ID campagna** collega il progetto a una campagna specifica ed è richiesto per [generare rapporti di misurazione](./measure.md#create-measurement-report). Puoi aggiungere più ID campagna a un progetto se esegui più campagne con lo stesso collaboratore. Tutte queste campagne sono disponibili per la selezione nel reporting.

- **Editori**: immetti o aggiorna gli ID campagna e i nomi associati nell&#39;interfaccia utente di Collaboration prima di eseguire i rapporti.
- **Inserzionisti**: richiedi al tuo collaboratore (editore) di aggiungere gli ID campagna in base alle esigenze.

Per aggiungere o aggiornare gli ID campagna, passa all&#39;area di lavoro **[!UICONTROL Collabora]**, quindi seleziona **[!UICONTROL Visualizza]** nella scheda del progetto corrispondente.

![L&#39;area di lavoro di collaborazione evidenzia l&#39;opzione Visualizza all&#39;interno di una scheda del progetto.](/help/assets/collaborate/manage-view-projects/view-project.png){zoomable="yes"}

L&#39;area di lavoro **[!UICONTROL Panoramica progetto]** corrispondente viene visualizzata con un **[!UICONTROL ID campagna e nome]** che elenca tutte le campagne collegate al progetto. Se non hai ancora aggiunto una campagna, seleziona **[!UICONTROL Aggiungi]**. Se sono già presenti campagne, seleziona **[!UICONTROL Modifica]** per aggiornare i dettagli o aggiungerne di nuovi.

![Nell&#39;area di lavoro della panoramica del progetto è visualizzata la sezione ID e nome campagna con l&#39;opzione Modifica evidenziata.](/help/assets/collaborate/manage-view-projects/edit-campaign-id.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL ID campagna e nome]**, seleziona **[!UICONTROL Aggiungi ID campagna]** per aggiungere una nuova riga in cui inserire i dettagli della campagna.

![Nella finestra di dialogo ID e nome campagna viene visualizzata la riga della campagna vuota dopo aver selezionato l&#39;opzione Aggiungi ID campagna.](/help/assets/collaborate/manage-view-projects/add-campaign-row.png){zoomable="yes"}

Fornisci **[!UICONTROL ID campagna]** e **[!UICONTROL nome campagna]**, quindi seleziona **[!UICONTROL Salva]**.

![La finestra di dialogo dell&#39;ID e del nome della campagna mostra i nuovi dettagli della campagna e l&#39;opzione Salva evidenziata.](/help/assets/collaborate/manage-view-projects/save-campaign-id.png){zoomable="yes"}

Controlla la sezione **[!UICONTROL ID e nome campagna]** per visualizzare le ultime campagne e le modifiche recenti. Ora puoi utilizzare i nuovi ID campagna per generare rapporti di misurazione.

![Nell&#39;area di lavoro della panoramica del progetto viene visualizzata la sezione aggiornata relativa all&#39;ID e al nome della campagna.](/help/assets/collaborate/manage-view-projects/view-updated-campaigns.png){zoomable="yes"}
