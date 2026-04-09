---
title: Gestire le connessioni dati di misurazione
description: Scopri come gestire le connessioni dati di misurazione, inclusi i dettagli e le chiavi di corrispondenza in Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 494277f421606eda62b74c254f1fdd29b22e3473
workflow-type: tm+mt
source-wordcount: '1338'
ht-degree: 3%

---

# Gestire le connessioni dati di misurazione

{{limited-availability-release-note}}

## Panoramica

Utilizza le connessioni dati di misurazione in Real-Time CDP Collaboration per originare i dati di conversione da varie piattaforme. Scopri come gestire i dettagli e le chiavi di corrispondenza per le connessioni dati esistenti.

## Visualizzare le connessioni dati di misurazione {#view-measurement-data-connections}

Puoi visualizzare i dettagli di qualsiasi connessione dati di misurazione esistente, tra cui il modo in cui vengono originati i dati di conversione, le chiavi corrispondenti in uso e tutti gli eventi di conversione collegati alla connessione.

Dall&#39;area di lavoro **[!UICONTROL Setup]**, passare alla scheda **[!UICONTROL Le mie connessioni dati]**. Tutte le connessioni dati di misurazione correnti vengono visualizzate nella sezione **[!UICONTROL Misurazione]** in visualizzazione tabulare o griglia. Selezionare **[!UICONTROL Visualizza connessione dati]** nella scheda di connessione corrispondente oppure selezionare il nome della connessione dati in visualizzazione tabella per aprire l&#39;area di lavoro e visualizzare tutti i dettagli.

![La scheda Le mie connessioni dati evidenzia una scheda di connessione dati di misurazione e l&#39;opzione Visualizza connessione dati.](/help/assets/setup/manage-measurement-data-connection/view-measurement-data-connection.png){zoomable="yes"}

### Dettagli della connessione dati di misurazione {#measurement-data-connection-details}

In questa sezione sono disponibili i seguenti dettagli della connessione dati:

| Campo | Descrizione |
|-------------------|-------------|
| Stato | Lo stato corrente della connessione dati di misurazione, ad esempio **[!UICONTROL Attivo]**. |
| Origine | La piattaforma o il sistema che fornisce i dati di misurazione per questa connessione. |
| Sandbox | Il nome della sandbox in cui è configurata la connessione dati per la misurazione. |
| Set di dati | Nome del set di dati utilizzato per la determinazione origine dei dati di misurazione nella connessione. |
| Ultimo aggiornamento | Il timestamp dell’aggiornamento più recente della connessione dati per la misurazione. |
| Ultimo aggiornamento di | L&#39;ultimo utente che ha modificato la connessione dati di misurazione. |
| Creato | La marca temporale in cui è stata creata la connessione dati per la misurazione. |
| Creato da | Utente che ha creato originariamente la connessione dati per la misurazione. |

{style="table-layout:auto"}

### Chiavi di corrispondenza {#match-keys}

Le chiavi di corrispondenza sono i campi di destinazione a cui hai mappato i campi di origine quando [hai originato i dati di misurazione](./onboard-measurement-data.md). Per ulteriori informazioni sul funzionamento delle chiavi di corrispondenza, consulta la guida [chiavi di corrispondenza](./onboard-account.md#set-up-match-keys).

![Area di lavoro di connessione dati di misurazione con la sezione Chiavi di corrispondenza evidenziata.](/help/assets/setup/manage-measurement-data-connection/view-match-keys.png){zoomable="yes"}

### Eventi di conversione {#conversion-events}

Nella parte inferiore dell’area di lavoro viene visualizzato un elenco di eventi di conversione associati alla connessione dati. Nell&#39;elenco viene visualizzata una breve panoramica di ogni evento, con il relativo stato, tipo di conversione e origine. È possibile selezionare il nome dell&#39;evento per visualizzarne e modificarne le configurazioni oppure rimuovere l&#39;evento di conversione con l&#39;opzione di eliminazione (![icona Elimina](/help/assets/common/delete.svg)). Per una guida completa sulla gestione di un evento di conversione, consulta la guida [aggiungi e gestisci dati di misurazione](./onboard-measurement-data.md).

![Area di lavoro di connessione dati di misurazione con la sezione degli eventi di conversione evidenziata.](/help/assets/setup/manage-measurement-data-connection/view-conversion-events.png){zoomable="yes"}

## Modifica connessione dati di misurazione {#edit-measurement-data-connection}

Puoi aggiornare i dettagli e le chiavi di corrispondenza di una connessione dati di misurazione esistente in qualsiasi momento per garantire la precisione dei rapporti e dell’analisi. Per iniziare, passare alla scheda **[!UICONTROL Le mie connessioni dati]** e selezionare la connessione dati di misurazione che si desidera modificare. Verrà aperta l&#39;area di lavoro connessione dati, in cui è possibile eseguire i passaggi seguenti per apportare le modifiche necessarie.

### Modifica nome e descrizione {#edit-name-and-description}

Per aggiornare il nome e la descrizione della connessione dati, selezionare l&#39;icona di modifica (![icona Modifica](/help/assets/icons/edit.png)) accanto al nome della connessione corrente.

![L&#39;area di lavoro della connessione dati di misurazione evidenzia l&#39;icona Modifica accanto al nome della connessione dati.](/help/assets/setup/manage-measurement-data-connection/edit-name-description.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL Modifica connessione dati]**, aggiorna i campi con i valori desiderati, quindi seleziona **[!UICONTROL Salva]** per applicare le modifiche.

![Finestra di dialogo Modifica connessione dati con l&#39;opzione Salva evidenziata.](/help/assets/setup/manage-measurement-data-connection/edit-name-description-dialog.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo di conferma per confermare che i dettagli sono stati aggiornati correttamente.

### Modifica chiavi di corrispondenza {#edit-match-keys}

>[!IMPORTANT]
>
>Prima di modificare le chiavi di corrispondenza per una connessione dati, tieni presente quanto segue:
>
>* Per le connessioni dati è possibile utilizzare solo le chiavi di corrispondenza configurate per il tuo account.
>* Al momento, è possibile aggiungere altre chiavi di corrispondenza a una connessione dati, ma una volta abilitata, una chiave di corrispondenza non può essere rimossa.

Nell&#39;area di lavoro connessione dati, selezionare **[!UICONTROL Modifica]** nel pannello **[!UICONTROL Corrispondenza chiavi]**.

![Sezione delle chiavi di corrispondenza con l&#39;opzione Modifica evidenziata.](/help/assets/setup/manage-measurement-data-connection/edit-match-keys.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo di conferma in cui viene spiegato che eventuali modifiche alla connessione dati verranno applicate a tutte le conversioni associate. Seleziona **[!UICONTROL OK]** per confermare. Puoi scegliere di saltare questa conferma in futuro.

![Finestra di dialogo di conferma che indica che le modifiche apportate alla connessione dati verranno applicate a tutte le conversioni associate.](/help/assets/setup/manage-measurement-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL Corrispondenza chiavi]**, puoi rivedere le impostazioni di arricchimento e visualizzare le mappature correnti tra i campi di origine e i campi di destinazione (chiavi di corrispondenza).

![La finestra di dialogo Corrispondenza chiavi mostra le impostazioni di arricchimento e le mappature esistenti tra i campi di origine e i campi di destinazione corrispondenti.](/help/assets/setup/manage-measurement-data-connection/edit-match-keys-dialog.png){zoomable="yes"}

#### Arricchimento {#enrichment}

Se l&#39;arricchimento non è stato abilitato quando [hai originato i dati di misurazione](./onboard-measurement-data.md), puoi arricchire il set di dati dell&#39;evento con gli attributi di Real-Time Customer Profile. Una volta attivato l’arricchimento per i dati di misurazione, non può essere disattivato. Puoi comunque aggiornare le chiavi di unione per l’arricchimento in base alle esigenze.

Quando abiliti l&#39;arricchimento nella finestra di dialogo **[!UICONTROL Corrispondenza chiavi]**, l&#39;interfaccia utente si espande per visualizzare altre opzioni di configurazione nella sezione **[!UICONTROL Arricchisci i dati dell&#39;evento con ID dai profili]**.

Selezionare l&#39;opzione **[!UICONTROL Chiave di unione campi di Source]**.

![Finestra di dialogo Corrispondenza chiavi con l&#39;opzione chiave di unione campi di Source evidenziata.](../../assets/setup/manage-measurement-data-connection/enrich-event-data.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL Chiave di unione campo di Source]**, scegli il campo di origine, seguito da **[!UICONTROL Seleziona]**.

![La finestra di dialogo della chiave di unione campi di Source evidenzia il campo di origine selezionato e l&#39;opzione Avanti.](../../assets/setup/manage-measurement-data-connection/source-field-join-key-dialog.png){zoomable="yes"}

Selezionare quindi l&#39;opzione **[!UICONTROL Chiave di aggiunta profilo]**. Nella finestra di dialogo **[!UICONTROL Chiave di aggiunta profilo]**, seleziona il campo del profilo dall&#39;elenco. Puoi utilizzare l’opzione Cerca per trovare il campo desiderato. Quindi, scegli **[!UICONTROL Seleziona]** per confermare.

![La finestra di dialogo Chiave di unione profilo evidenzia il campo del profilo selezionato e l&#39;opzione Seleziona.](../../assets/setup/manage-measurement-data-connection/profile-join-key-dialog.png){zoomable="yes"}

#### Modifica mappatura {#edit-mapping}

Per modificare una chiave di corrispondenza esistente, aggiornare il campo di origine e il campo di destinazione associati nella finestra di dialogo **[!UICONTROL Chiavi di corrispondenza]**. Se si desidera includere una nuova chiave di corrispondenza, selezionare **[!UICONTROL Aggiungi campo]**. In questo modo viene creata una riga vuota in cui è possibile definire una mappatura aggiuntiva tra i campi di origine e di destinazione.

![Dopo aver selezionato Aggiungi campo, nella finestra di dialogo Tasti di corrispondenza viene visualizzata una nuova riga di mappatura vuota pronta per l&#39;input.](/help/assets/setup/manage-measurement-data-connection/add-new-field.png){zoomable="yes"}

Quindi, seleziona il campo di origine vuoto. Viene visualizzata la finestra di dialogo **[!UICONTROL Seleziona campo di origine]** con un elenco dei campi di origine disponibili raggruppati in opzioni quali **[!UICONTROL Spazi dei nomi identità]** e **[!UICONTROL Attributi profilo]**. Puoi filtrare l’elenco e trovare il campo sorgente desiderato con l’opzione di ricerca.

Scegli il campo di origine desiderato, seguito da **[!UICONTROL Seleziona]**.

![La finestra di dialogo Seleziona campo di origine evidenzia l&#39;opzione Cerca, il campo Origine telefono e l&#39;opzione Seleziona.](/help/assets/setup/manage-measurement-data-connection/select-source-field.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL Corrispondenza chiavi]**, utilizza il menu a discesa per mappare il nuovo campo di origine a un campo di destinazione. Tutti i campi di destinazione disponibili sono le chiavi di corrispondenza configurate per l&#39;account Collaborator. Se non trovi il campo di destinazione necessario, [modifica le chiavi di corrispondenza dell&#39;account](./onboard-account.md#edit-match-keys) per aggiungerlo.

Utilizzare l&#39;opzione **[!UICONTROL Applica trasformazione]** se si desidera impostare come origine di un campo senza hash un campo di destinazione con hash, ad esempio quando si esegue il mapping di un campo di origine telefono in testo normale al campo di destinazione **[!UICONTROL Telefono con hash]**.

![Nel menu a discesa vengono visualizzati tutti i campi di destinazione disponibili da mappare con il nuovo campo di origine.](/help/assets/setup/manage-measurement-data-connection/target-field-dropdown.png){zoomable="yes"}

Dopo aver completato la mappatura dei campi, controlla gli aggiornamenti e seleziona **[!UICONTROL Conferma]** per applicare le modifiche.

![La finestra di dialogo Corrispondenza chiavi mostra il mapping dei campi aggiornato con l&#39;opzione Conferma evidenziata.](/help/assets/setup/manage-measurement-data-connection/confirm-edit-match-keys.png){zoomable="yes"}

Una finestra di dialogo di conferma conferma conferma che i codici di corrispondenza sono stati aggiornati correttamente.

## Elimina connessione dati

Se si elimina una connessione dati, verranno rimosse tutte le conversioni sottostanti, le impostazioni associate e l’utilizzo in Collaboration. Questa azione non può essere annullata.

Per eliminare una connessione dati esistente, selezionare l&#39;icona Elimina (![icona Elimina](/help/assets/common/delete.svg)) nell&#39;area di lavoro di una singola connessione dati.

![Area di lavoro connessioni dati con l&#39;opzione Elimina evidenziata.](/help/assets/setup/manage-measurement-data-connection/delete-measurement-data-connection.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo di conferma. Seleziona **[!UICONTROL Elimina]** per completare l&#39;eliminazione della connessione dati.

![Finestra di dialogo Elimina connessione dati con l&#39;opzione Elimina evidenziata.](/help/assets/setup/manage-measurement-data-connection/delete-measurement-data-connection-confirm.png){zoomable="yes"}

Una finestra di dialogo di conferma conferma conferma la corretta eliminazione della connessione dati.

## Passaggi successivi {#next-steps}

Dopo aver gestito le connessioni dati di misurazione, puoi:

* Aggiungi altri eventi di conversione collegati alla connessione dati in base alle esigenze. Per i passaggi dettagliati, consulta la documentazione [Aggiungi e gestisci dati di misurazione](./onboard-measurement-data.md).
* Genera rapporti di misurazione per ottenere informazioni approfondite sulle prestazioni e sull’impatto della campagna. Per ulteriori informazioni sui tipi di report disponibili e su come crearli, vedere la guida alle [misurazioni delle prestazioni](/help/guide/collaborate/measure.md).
