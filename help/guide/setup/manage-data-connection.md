---
title: Gestisci connessioni dati
description: Scopri come gestire le connessioni dati, tra cui le chiavi di corrispondenza, la pianificazione, i casi d’uso e il filtro del pubblico in Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
TQID: https://experienceleague.adobe.com/QvkEpR1fJMZ5BXrucAzEtxFNSfSMS-2hIZvMSg63ySE
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1179
ht-degree: 5%

---

# Gestisci connessioni dati

{{limited-availability-release-note}}

## Panoramica

Utilizza le connessioni dati in Real-Time CDP Collaboration per indirizzare il pubblico da varie piattaforme. Scopri come gestire le chiavi di corrispondenza e pianificare l’aggiornamento dei dati per le connessioni dati esistenti. Inoltre, potrai filtrare i tipi di pubblico in base a attributi diversi per ottenere informazioni più granulari.

>[!NOTE]
>
>Per creare una nuova connessione dati, vedere [Aggiungere e gestire tipi di pubblico](./onboard-audiences.md).

## Visualizzare connessioni dati

Per visualizzare le connessioni dati esistenti, passare a **[!UICONTROL Configurazione]** e selezionare la scheda **[!UICONTROL Connessioni dati personali]**. Viene visualizzata tutta la connessione dati corrente, con una breve panoramica di ogni connessione. Per una visualizzazione completa delle informazioni di una connessione dati, incluse le chiavi di corrispondenza, i dettagli di pianificazione e i tipi di pubblico, selezionare **[!UICONTROL Visualizza connessione dati]** nella connessione corrispondente.

![Imposta l&#39;area di lavoro con la visualizzazione della scheda Connessioni dati visualizzata ed evidenziata.](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### Chiavi di corrispondenza {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Chiavi di corrispondenza"
>abstract="Le chiavi di corrispondenza determinano il modo in cui verranno abbinati i dati provenienti da origini diverse. Le chiavi di corrispondenza mostrate di seguito sono i campi di destinazione a cui hai mappato i campi di origine."

Le chiavi di corrispondenza sono i campi di destinazione [sui quali hai mappato i campi di origine](./onboard-audiences.md#map-fields). Per ulteriori informazioni sul funzionamento delle chiavi di corrispondenza, consulta la guida [chiavi di corrispondenza](./onboard-account.md#set-up-match-keys).

![Area di lavoro connessioni dati con la sezione Chiavi di corrispondenza evidenziata.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Pianificazione {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Pianificazione"
>abstract="Visualizza i dettagli di pianificazione per la connessione dati e, se necessario, modifica le configurazioni."

Visualizza e gestisci le impostazioni di pianificazione per le connessioni dati. La pianificazione determina la frequenza con cui il pubblico viene aggiornato.

Dopo aver creato una connessione dati, è possibile aggiornarne la frequenza di aggiornamento, la data di inizio e la data di fine direttamente dalla sezione **[!UICONTROL Pianificazione]** dell&#39;area di lavoro connessione dati.

>[!NOTE]
>
>Quando si selezionano i tipi di pubblico da Adobe Experience Platform, i tipi di pubblico diventano disponibili entro 24 ore dall’impostazione della connessione dati. Dopo l’origine iniziale, i dati del pubblico vengono aggiornati in base alla frequenza definita.

Per ulteriori informazioni sulla pianificazione, consulta la [sezione pianificazione](/help/guide/setup/onboard-audiences.md#schedule) nella guida alla configurazione dei tipi di pubblico.

![Area di lavoro di una connessione dati con la sezione Pianificazione evidenziata.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Modifica connessione dati {#edit-data-connection}

Leggi le sezioni seguenti per scoprire come aggiornare le chiavi di corrispondenza e le impostazioni di pianificazione di una connessione dati esistente.

### Modifica chiavi di corrispondenza {#edit-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_edit_measurement_data_connection_enrichment"
>title="Arricchimento"
>abstract="La disattivazione dell’arricchimento non è supportata. In alternativa, puoi modificare le chiavi di unione per l’arricchimento."
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-manage-dataconnections" text="Arricchimento"

>[!IMPORTANT]
>
>Before editing the match keys for a data connection, note the following:
>
>* Only match keys that are configured for your account can be used for data connections.
>* At this time, you can add additional match keys to a data connection, but once a match key is enabled, it cannot be removed.

Select **[!UICONTROL Edit]** from the **[!UICONTROL Match keys]** section.

![The Match keys section with the Edit option highlighted.](/help/assets/setup/manage-data-connection/edit-match-keys.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo di conferma in cui viene spiegato che eventuali modifiche alla connessione dati verranno applicate a tutti i tipi di pubblico associati. Seleziona **[!UICONTROL OK]** per confermare. Puoi scegliere di saltare questa conferma in futuro.

![Finestra di dialogo di conferma che indica che eventuali modifiche alla connessione dati verranno applicate a tutti i tipi di pubblico associati.](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

In the **[!UICONTROL Match keys]** dialog, you can view the existing mappings between source fields and their corresponding target fields (match keys). You can edit a match key by updating the mapped source field, or add additional mapping field rows to populate new match keys.

![The Match keys dialog showing the existing mappings between source fields and the corresponding target fields.](/help/assets/setup/manage-data-connection/match-keys-dialog.png){zoomable="yes"}

#### Add match keys {#add-match-keys}

Select **[!UICONTROL Add field]** to add a new field row.

![After selecting Add field, the Match keys dialog displays an empty new mapping field ready for input.](/help/assets/setup/manage-data-connection/add-new-field.png){zoomable="yes"}

Next, select the empty source field. The **[!UICONTROL Select source field]** dialog appears with the **[!UICONTROL Identity namespaces]** and **[!UICONTROL Profile attributes]** options. You can filter the list and find the desired source field with the search option.

Scegli il campo di origine desiderato, seguito da **[!UICONTROL Seleziona]**.

![The Select source field dialog with the GAID option selected.](/help/assets/setup/manage-data-connection/select-source-field.png){zoomable="yes"}

In the **[!UICONTROL Match keys]** dialog, use the dropdown menu to map the new source field to a target field. All available target fields are the match keys configured for your Collaborator account. If you don&#39;t see the target field you need, [edit your account&#39;s match keys](./onboard-account.md#edit-match-keys) to add it.

Use the **[!UICONTROL Apply transformation]** option if you want to source a non-hashed field to a hashed target field, for example, when mapping a plain text email source field to the **[!UICONTROL Hashed email]** target field.

![Nel menu a discesa vengono visualizzati tutti i campi di destinazione disponibili da mappare con il nuovo campo di origine.](/help/assets/setup/manage-data-connection/select-target-field.png){zoomable="yes"}

Dopo aver completato la mappatura dei campi, controlla gli aggiornamenti e seleziona **[!UICONTROL Conferma]** per applicare le modifiche.

![La finestra di dialogo Corrispondenza chiavi mostra il mapping dei campi aggiornato con l&#39;opzione Conferma evidenziata.](/help/assets/setup/manage-data-connection/review-and-confirm.png){zoomable="yes"}

Una finestra di dialogo di conferma conferma conferma che i codici di corrispondenza sono stati aggiornati correttamente.

### Modifica pianificazione {#edit-scheduling}

Dopo aver creato una connessione dati, è possibile aggiornarne la frequenza di aggiornamento, la data di inizio e la data di fine direttamente dalla sezione **[!UICONTROL Pianificazione]** dell&#39;area di lavoro connessione dati.

Puoi modificare la frequenza di una connessione dati esistente per controllare meglio la frequenza con cui i tipi di pubblico vengono aggiornati. Per modificare la pianificazione, seleziona **[!UICONTROL Modifica]** dalla connessione dati nella scheda di pianificazione.

![La sezione Pianificazione con l&#39;opzione Modifica evidenziata.](/help/assets/setup/manage-data-connection/edit-scheduling.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo di conferma in cui viene spiegato che eventuali modifiche alla connessione dati verranno applicate a tutti i tipi di pubblico associati. Seleziona **[!UICONTROL OK]** per confermare. Puoi scegliere di saltare questa conferma in futuro.

![Finestra di dialogo di conferma che indica che eventuali modifiche alla connessione dati verranno applicate a tutti i tipi di pubblico associati.](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL Pianificazione]**, seleziona il menu a discesa per aggiornare la **[!UICONTROL Frequenza]**. Impostare la frequenza di aggiornamento in modo che venga eseguita ogni giorno oppure ogni due o sei giorni.

![La finestra di dialogo Pianificazione con il menu a discesa Frequenza è stata espansa per visualizzare le opzioni di frequenza di aggiornamento del pubblico.](../../assets/setup/manage-data-connection/edit-frequency.png){zoomable="yes"}

Quindi, seleziona **[!UICONTROL Intervallo date]** per aggiornare il periodo durante il quale i tipi di pubblico vengono popolati e aggiornati.

![La finestra di dialogo Pianificazione mostra l&#39;elenco a discesa dell&#39;intervallo di date espanso per modificare le date di inizio e di fine per la popolazione e l&#39;aggiornamento del pubblico.](../../assets/setup/manage-data-connection/edit-date-range.png){zoomable="yes"}

Al termine, controlla gli aggiornamenti e seleziona **[!UICONTROL Salva]** per applicare le modifiche.

![La finestra di dialogo Pianificazione evidenzia gli aggiornamenti e l&#39;opzione Salva.](../../assets/setup/manage-data-connection/scheduling-dialog.png){zoomable="yes"}

## Elimina connessione dati

L’eliminazione di una connessione dati rimuoverà tutti i tipi di pubblico sottostanti, le impostazioni associate e l’utilizzo in Collaboration. Questa azione non può essere annullata.

Per eliminare una connessione dati esistente, selezionare l&#39;icona Elimina (![icona Elimina](/help/assets/common/delete.svg)) nell&#39;area di lavoro di una singola connessione dati.

![Area di lavoro connessioni dati con l&#39;opzione Elimina evidenziata.](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo di conferma. Seleziona **[!UICONTROL Elimina]** per completare l&#39;eliminazione della connessione dati.

![Finestra di dialogo Elimina connessione dati con l&#39;opzione Elimina evidenziata.](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## Gestire i tipi di pubblico {#manage-audiences}

Nella parte inferiore dell’area di lavoro viene visualizzato un elenco di tipi di pubblico associati alla connessione dati. L’elenco presenta una breve panoramica di ciascun pubblico, con il relativo stato, l’origine e l’accesso alla connessione. Per modificare le categorie di un pubblico, l’accesso alla connessione o la visibilità dei metadati, seleziona il nome del pubblico. Per una guida completa sulla gestione di un pubblico, consulta la guida [visualizza i singoli tipi di pubblico](./onboard-audiences.md#view-individual-audiences).

![Un&#39;area di lavoro connessioni dati con i tipi di pubblico evidenziati.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Passaggi successivi

Dopo aver gestito le connessioni dati, puoi [individuare le sovrapposizioni](/help/guide/collaborate/discover.md) tra i tipi di pubblico e quelli che il tuo collaboratore ha reso individuabili.
