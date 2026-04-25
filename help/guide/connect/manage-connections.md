---
title: Gestire le connessioni
description: Learn how to manage your connections in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 50120839-4a20-4ec1-8887-9342bd17c52d
TQID: https://experienceleague.adobe.com/plolWAj37G7hiH7gMYxDwJJDVXAIfMhSQHPRypErbxw
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1092
ht-degree: 1%

---

# Gestire le connessioni {#manage-connections}

{{limited-availability-release-note}}

The **[!UICONTROL My connections]** workspace provides a centralized location for managing your connections. You can view existing connections in the **[!UICONTROL Existing connections]** section and see any connections that require action in the **[!UICONTROL Action required]** section.

## Visualizza connessione {#view-connection}

To view your existing connections, navigate to the **[!UICONTROL Connect]** workspace. As a publisher, your existing connection will be displayed. As an advertiser, you should then navigate to **[!UICONTROL My connections]**.

![The View connection option highlighted for a connection in the My connections workspace.](/help/assets/connect/manage-connections/view-connection.png){zoomable="yes"}

The connection overview workspace appears, displaying details about the connection and its active projects. Select **[!UICONTROL Connection settings]** to view the connection settings.

![The Connection settings option highlighted in the connection overview workspace.](/help/assets/connect/manage-connections/connection-overview.png){zoomable="yes"}

The connection settings workspace appears, displaying the connection details between you and your collaborator. Here, you can view all the settings selected during the connection process, the current status of the connection, the connection owner, and the contact information for your collaborator. For information on specific connection settings, see the [connection settings](/help/guide/connect/establishing-connections.md#connection-settings) guide.

![The connection settings workspace displaying connection details.](/help/assets/connect/manage-connections/connection-settings.png){zoomable="yes"}

## Elimina connessione {#delete-connection}

You can delete any connections with collaborators that you do not want to continue working with. To delete a connection, navigate to the connection you wish to delete and then select the delete icon ![delete icon](/help/assets/common/delete.svg) in the connection workspace.

![The delete icon highlighted in the connection workspace.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

A confirmation dialog appears, asking you to confirm the deletion of the connection. Select **[!UICONTROL Delete]** to confirm the deletion.

![The confirmation dialog to delete a connection.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Once the connection is deleted, all existing projects in the collaboration will be permanently deleted and unrecoverable. The connection request will remain in a pending state within the **[!UICONTROL Action required]** section within **[!UICONTROL My connections]**, but the connection and its configurations will no longer be active. You will need to re-establish the connection if you want to connect with the collaborator again.

## Modifica connessione {#edit-connection}

As the owner of a collaboration connection, you can edit the connection settings with your collaborator after the connection is established. Puoi eseguire le seguenti operazioni:

* Aggiungi casi d’uso
* Aggiungi chiavi di corrispondenza. La rimozione della chiave di corrispondenza sarà supportata in futuro.
* Aggiornare le autorizzazioni di attivazione del pubblico
* Aggiorna impostazioni di divisione crediti

>[!IMPORTANT]
>
>Una volta aggiunto un caso d’uso o una chiave di corrispondenza a una connessione, non è possibile rimuoverlo.

>[!TIP]
>
>Il **proprietario** è il collaboratore che avvia la connessione inviando l&#39;invito al **destinatario**. Per ulteriori informazioni, consulta la [documentazione relativa all&#39;impostazione di connessioni con i collaboratori](./establishing-connections.md).

Per modificare le impostazioni di connessione, passare all&#39;area di lavoro impostazioni connessione. Seleziona l&#39;icona dei tre punti (![icona dei tre punti.](/help/assets/icons/more.png)) per visualizzare le azioni disponibili, selezionare **[!UICONTROL Modifica]**.

![Area di lavoro delle impostazioni di connessione con l&#39;opzione Modifica evidenziata.](/help/assets/connect/manage-connections/edit-connection.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo in cui viene richiesto di modificare e inviare le modifiche alle impostazioni per la revisione collaboratore. Seleziona **[!UICONTROL Modifica]**.

![Finestra di dialogo Modifica impostazioni di connessione con l&#39;opzione Modifica evidenziata.](/help/assets/connect/manage-connections/edit-connection-settings-dialog.png){zoomable="yes"}

### Modifica attivazione pubblico {#edit-audience-activation}

Le impostazioni di attivazione del pubblico determinano quale collaboratore nella connessione può attivare i tipi di pubblico nelle destinazioni. Per modificare queste impostazioni, seleziona **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Audience Activation]**.

![Nella schermata Modifica impostazioni di connessione sono visualizzate la sezione Audience Activation e l&#39;opzione Modifica.](/help/assets/connect/manage-connections/edit-audience-activation.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL Audience Activation]**, utilizza il menu a discesa per aggiornare le autorizzazioni di Audience Activation. Puoi scegliere un singolo collaboratore o consentire a entrambi i collaboratori di attivare i tipi di pubblico.

![Il menu a discesa di evidenziazione della finestra di dialogo Attivazione pubblico è stato espanso per aggiornare le autorizzazioni di attivazione del pubblico.](/help/assets/connect/manage-connections/audience-activation-dropdown-menu.png){zoomable="yes"}

Al termine, seleziona **[!UICONTROL Salva]**.

![La finestra di dialogo di attivazione del pubblico mostra le nuove autorizzazioni di attivazione del pubblico e l&#39;opzione Salva.](/help/assets/connect/manage-connections/audience-activation-dialog.png){zoomable="yes"}

### Aggiungi casi d’uso {#add-use-cases}

In Collaboration, casi d’uso come Discover, Activate e Measure determinano le sezioni e le funzioni del progetto che è possibile utilizzare con il collaboratore. Puoi aggiungere altri casi d’uso a una connessione esistente per progetti futuri. Per ulteriori informazioni, vedi [casi di utilizzo di collaborazione](../overview/use-cases.md).

Per aggiungere nuovi casi d&#39;uso, seleziona **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Casi d&#39;uso]**.

![Nella schermata Modifica impostazioni di connessione sono evidenziate la sezione Casi d&#39;uso e l&#39;opzione Modifica.](/help/assets/connect/manage-connections/edit-use-cases.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL Casi d&#39;uso]**, attiva i nuovi casi d&#39;uso che desideri aggiungere, seguiti da **[!UICONTROL Salva]**.

![Nella finestra di dialogo Casi d&#39;uso è evidenziata l&#39;opzione Salva.](/help/assets/connect/manage-connections/use-cases-dialog.png){zoomable="yes"}

>[!NOTE]
>
>Quando [aggiungi nuovi casi d&#39;uso](#add-use-cases), ad esempio &quot;Audience Activation&quot; o &quot;Measurement&quot;, la schermata Modifica impostazioni connessione si aggiorna per includere le sezioni **[!UICONTROL Audience Activation]** e **[!UICONTROL Credit split]**. Devi configurare le impostazioni appropriate per questi nuovi casi d’uso. Per ulteriori dettagli, consulta le guide [Audience Activation](../connect/establishing-connections.md#audience-activation) e [Credit split](../connect/establishing-connections.md#credit-split).
>
>![Nella schermata Modifica impostazioni di connessione vengono visualizzate le sezioni di attivazione del pubblico e di suddivisione del credito dopo l&#39;aggiunta di nuovi casi d&#39;uso.](/help/assets/connect/manage-connections/setup-audience-activation-credit-split.png){zoomable="yes"}

### Aggiungi chiavi di corrispondenza {#add-match-keys}

Per la connessione sono disponibili solo le chiavi di corrispondenza configurate nel tuo account e selezionate anche dal tuo collaboratore. Una volta che [aggiungi nuove chiavi di corrispondenza all&#39;account](../setup/onboard-account.md#edit-match-keys) e anche il tuo collaboratore seleziona le stesse chiavi, puoi abilitarle all&#39;interno delle connessioni esistenti.

Nella schermata Modifica impostazioni di connessione, seleziona **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Corrispondenza chiavi]**.

![Nella schermata Modifica impostazioni di connessione sono evidenziate la sezione Corrispondenza chiavi e l&#39;opzione Modifica.](/help/assets/connect/manage-connections/edit-connection-match-keys.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo **[!UICONTROL Corrispondenza chiavi]** che mostra le chiavi di corrispondenza esistenti configurate per la connessione. Seleziona le chiavi di corrispondenza da aggiungere, seguite da **[!UICONTROL Salva]**.

![La finestra di dialogo delle chiavi di corrispondenza visualizza le nuove chiavi di corrispondenza selezionate e l&#39;opzione Salva.](/help/assets/connect/manage-connections/connection-match-keys-dialog.png){zoomable="yes"}

### Modifica frazionamento credito {#edit-credit-split}

Le impostazioni della suddivisione del credito specificano quale collaboratore è responsabile dei costi associati a ciascun caso d’uso della connessione. Per aggiornare queste impostazioni, selezionare **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Divisione crediti]**.

![Nella schermata Modifica impostazioni di connessione sono evidenziate la sezione Divisione crediti e l&#39;opzione Modifica.](/help/assets/connect/manage-connections/edit-credit-split.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL Divisione crediti]**, seleziona le impostazioni preferite per [!UICONTROL Corrispondenza attivazione] e [!UICONTROL Misurazione]. Quindi, seleziona **[!UICONTROL Salva]** per confermare.

![La finestra di dialogo per la divisione del credito mostra le impostazioni per la divisione del credito e l&#39;opzione Salva.](/help/assets/connect/manage-connections/credit-split-dialog.png){zoomable="yes"}

### Rivedi e invia modifiche {#review-and-submit-changes}

Dopo aver completato la modifica delle impostazioni di connessione, controllare e selezionare **[!UICONTROL Invia modifiche]**. Gli aggiornamenti delle impostazioni di connessione verranno inviati al tuo collaboratore per la revisione.

![Nella schermata Modifica impostazioni di connessione vengono visualizzati gli aggiornamenti e l&#39;opzione Invia modifiche.](/help/assets/connect/manage-connections/review-and-submit-changes.png){zoomable="yes"}

#### Salva le modifiche alle impostazioni di connessione come bozza

È possibile salvare le modifiche alle impostazioni di connessione come bozza e tornare alla fine dell&#39;aggiornamento delle impostazioni di connessione in qualsiasi momento.

Per salvare le modifiche come bozza, seleziona **[!UICONTROL Annulla]** accanto a **[!UICONTROL Invia modifiche]**. Quindi, nella finestra di dialogo **[!UICONTROL Modifiche non inviate]**, seleziona **[!UICONTROL Continua più tardi]** per confermare.

![Schermata Modifica impostazioni connessione.](/help/assets/connect/manage-connections/unsubmitted-changes-dialog.png){zoomable="yes"}

Le modifiche ora vengono salvate come bozza. Nell&#39;area di lavoro delle impostazioni di connessione è possibile visualizzare una notifica che indica che sono presenti modifiche non inviate. Per apportare ulteriori aggiornamenti, selezionare **[!UICONTROL Continua a modificare]**.

![Notifica nell&#39;area di lavoro delle impostazioni di connessione che indica che sono presenti modifiche non inviate in attesa di revisione e invio.](/help/assets/connect/manage-connections/continue-editing-connection.png){zoomable="yes"}
