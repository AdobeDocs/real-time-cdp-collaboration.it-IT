---
title: Gestire le connessioni
description: Scopri come gestire le connessioni in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 50120839-4a20-4ec1-8887-9342bd17c52d
source-git-commit: 46d2596bd0ccdc5da32067493968945c61f8acc4
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 1%

---

# Gestire le connessioni {#manage-connections}

{{limited-availability-release-note}}

L&#39;area di lavoro **[!UICONTROL Le mie connessioni]** fornisce una posizione centralizzata per la gestione delle connessioni. È possibile visualizzare le connessioni esistenti nella sezione **[!UICONTROL Connessioni esistenti]** e visualizzare tutte le connessioni che richiedono un&#39;azione nella sezione **[!UICONTROL Azione richiesta]**.

## Visualizza connessione {#view-connection}

Per visualizzare le connessioni esistenti, passa all&#39;area di lavoro **[!UICONTROL Connetti]**. In qualità di editore, verrà visualizzata la connessione esistente. In qualità di inserzionista, devi quindi passare a **[!UICONTROL Le mie connessioni]**.

![Opzione Visualizza connessione evidenziata per una connessione nell&#39;area di lavoro Connessioni.](/help/assets/connect/manage-connections/view-connection.png){zoomable="yes"}

Viene visualizzata l&#39;area di lavoro panoramica della connessione in cui sono visualizzati i dettagli della connessione e dei relativi progetti attivi. Selezionare **[!UICONTROL Impostazioni connessione]** per visualizzare le impostazioni di connessione.

![L&#39;opzione Impostazioni connessione è evidenziata nell&#39;area di lavoro panoramica connessione.](/help/assets/connect/manage-connections/connection-overview.png){zoomable="yes"}

Viene visualizzata l&#39;area di lavoro delle impostazioni di connessione, in cui vengono visualizzati i dettagli della connessione tra l&#39;utente e il collaboratore. Qui è possibile visualizzare tutte le impostazioni selezionate durante il processo di connessione, lo stato corrente della connessione, il proprietario della connessione e le informazioni di contatto per il collaboratore. Per informazioni su impostazioni di connessione specifiche, vedere la guida alle [impostazioni di connessione](/help/guide/connect/establishing-connections.md#connection-settings).

![L&#39;area di lavoro delle impostazioni di connessione visualizza i dettagli della connessione.](/help/assets/connect/manage-connections/connection-settings.png){zoomable="yes"}

## Elimina connessione {#delete-connection}

È possibile eliminare le connessioni con i collaboratori che non si desidera continuare a utilizzare. Per eliminare una connessione, passare alla connessione che si desidera eliminare, quindi selezionare l&#39;icona Elimina ![icona Elimina](/help/assets/common/delete.svg) nell&#39;area di lavoro connessione.

![Icona Elimina evidenziata nell&#39;area di lavoro connessione.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo di conferma in cui viene richiesto di confermare l’eliminazione della connessione. Seleziona **[!UICONTROL Elimina]** per confermare l&#39;eliminazione.

![Finestra di dialogo di conferma per eliminare una connessione.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Una volta eliminata la connessione, tutti i progetti esistenti nella collaborazione verranno eliminati definitivamente e non potranno essere ripristinati. La richiesta di connessione rimarrà in sospeso all&#39;interno della sezione **[!UICONTROL Azione richiesta]** all&#39;interno di **[!UICONTROL Le mie connessioni]**, ma la connessione e le relative configurazioni non saranno più attive. Se si desidera stabilire di nuovo la connessione con il collaboratore, è necessario ristabilire la connessione.

## Modifica connessione {#edit-connection}

In qualità di proprietario di una connessione di collaborazione, è possibile modificare le impostazioni di connessione con il proprio collaboratore una volta stabilita la connessione. Puoi eseguire le seguenti operazioni:

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

Per modificare le impostazioni di connessione, passare all&#39;area di lavoro impostazioni connessione. Selezionare l&#39;icona dei tre punti (![Icona dei tre punti.](/help/assets/icons/more.png)) per visualizzare le azioni disponibili, quindi selezionare **[!UICONTROL Modifica]**.

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
