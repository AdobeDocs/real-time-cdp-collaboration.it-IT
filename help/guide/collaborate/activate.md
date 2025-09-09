---
title: Attiva tipi di pubblico
description: Scopri come attivare i tipi di pubblico in Adobe Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: afe8560a12017c6b993f93cde8636288aa6e4991
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 2%

---

# Attiva tipi di pubblico

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L&#39;area di lavoro **[!UICONTROL Attiva]** è disponibile solo se il caso di utilizzo **Attivazione pubblico** è stato abilitato [durante il processo di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, consulta la guida [gestisci progetti](./manage-projects.md#project-use-cases).

L’attivazione del pubblico consente di attivare i tipi di pubblico da utilizzare nelle campagne. L&#39;attivazione può essere eseguita da uno dei collaboratori a seconda delle impostazioni di attivazione del pubblico [configurate nella connessione](/help/guide/connect/establishing-connections.md#configure-connection-settings). Dopo aver [individuato i tipi di pubblico migliori per la campagna](./discover.md), attiva i tipi di pubblico per renderli disponibili per l&#39;utilizzo. Quando attivi un pubblico, questo viene inviato alla destinazione preconfigurata del tuo collaboratore, ad esempio Adobe Experience Platform, dove diventa disponibile per l’utilizzo nelle campagne. Per ulteriori informazioni sulla configurazione delle destinazioni, consulta la guida [panoramica delle destinazioni](../destinations/overview.md).

## Attiva nuovi tipi di pubblico {#activate-new-audiences}

Per iniziare ad attivare i tipi di pubblico, passa alla scheda **[!UICONTROL Attiva]** nell&#39;area di lavoro del progetto.

>[!IMPORTANT]
>
>**Prima** di poter attivare un pubblico, il tuo collaboratore **deve** configurare una destinazione. Quando attivi un pubblico, questo viene inviato automaticamente alla destinazione configurata del tuo collaboratore. Se non è impostata alcuna destinazione, non puoi attivare i tipi di pubblico.
>
>![Attiva l&#39;area di lavoro quando il collaboratore non ha una destinazione configurata.](/help/assets/collaborate/activate/no-destination-configured.png)

Selezionare l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)), oppure l&#39;opzione **[!UICONTROL Attiva pubblico]** se non sono stati inviati tipi di pubblico precedenti per l&#39;attivazione.

![Attiva l&#39;area di lavoro in un progetto senza tipi di pubblico aggiunti.](/help/assets/collaborate/activate/activate-new-audiences.png)

Viene aperto il flusso di lavoro attiva tipi di pubblico, in cui è possibile selezionare il pubblico da inviare al collaboratore. Utilizza il menu a discesa per selezionare un pubblico o cercare un pubblico specifico. Per visualizzare ulteriori informazioni sui tipi di pubblico prima di effettuare la selezione, seleziona **[!UICONTROL Sfoglia tipi di pubblico]**

![Il flusso di lavoro di attivazione del pubblico con le opzioni del menu a discesa e Sfoglia pubblico evidenziate.](/help/assets/collaborate/activate/audience-activation.png)

In **[!UICONTROL Sfoglia tipi di pubblico]**, puoi visualizzare **[!UICONTROL Conteggio identità]**, **[!UICONTROL Identità sovrapposte]** e **[!UICONTROL Sovrapposizione %]** per ogni pubblico.

![Finestra di dialogo Sfoglia tipi di pubblico che mostra i tipi di pubblico disponibili.](/help/assets/collaborate/activate/browse-audiences.png)

>[!IMPORTANT]
>
>Quando si attivano tipi di pubblico in cui vengono utilizzate più chiavi di corrispondenza, se una o più chiavi di corrispondenza non presenta sovrapposizioni, nessun conteggio di pubblico o scende al di sotto della soglia, l’intera attivazione non riuscirà. Prima di attivare i tipi di pubblico, assicurati che abbiano una sovrapposizione sufficiente e che raggiungano la soglia minima di 1000 ID per tutte le chiavi di corrispondenza.

Selezionare il pubblico da attivare nelle campagne, quindi selezionare **[!UICONTROL Salva]**. Il pubblico è ora visualizzato ed è possibile visualizzare **[!UICONTROL il conteggio delle identità]**, **[!UICONTROL le identità sovrapposte]** e **[!UICONTROL la sovrapposizione %]** per il pubblico selezionato.

![Il flusso di lavoro di attivazione del pubblico con il pubblico selezionato è visualizzato.](/help/assets/collaborate/activate/audience-selected.png)

### Modifica chiavi di corrispondenza {#edit-match-keys}

Successivamente, puoi modificare le chiavi di corrispondenza del pubblico selezionando **[!UICONTROL Modifica chiavi di corrispondenza]** all&#39;interno del pubblico selezionato. Queste opzioni vengono ereditate dalle selezioni delle chiavi di corrispondenza quando è stata impostata inizialmente la connessione tra collaboratori. Puoi rimuovere le chiavi di corrispondenza selezionate se non sono applicabili a una campagna specifica, ma non puoi aggiungerne di nuove.

![Il flusso di lavoro di attivazione del pubblico con l&#39;opzione Modifica chiavi di corrispondenza evidenziata.](/help/assets/collaborate/activate/edit-match-keys.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Modifica chiavi di corrispondenza]**, in cui è possibile disattivare le chiavi di corrispondenza che non si desidera utilizzare. Seleziona **[!UICONTROL Salva]** per salvare le modifiche.

>[!NOTE]
>
>È necessario selezionare almeno una chiave di corrispondenza. Nella versione corrente, le uniche chiavi di corrispondenza disponibili sono **[!UICONTROL E-mail con hash]**, pertanto non è possibile rimuovere questa chiave di corrispondenza.

![Finestra di dialogo Modifica chiavi di corrispondenza nel flusso di lavoro di Audience Activation.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Impostare la frequenza di aggiornamento del pubblico {#set-audience-refresh-frequency}

Infine, imposta la frequenza e l’intervallo di date desiderati per l’aggiornamento del pubblico. Nella versione corrente, l&#39;unica opzione di frequenza supportata è **[!UICONTROL Once]**. La frequenza **[!UICONTROL Once]** indica che i tipi di pubblico vengono attivati una sola volta e non vengono aggiornati. L&#39;opzione **[!UICONTROL Data]** viene compilata automaticamente con la data corrente.

![Flusso di lavoro di attivazione del pubblico con la sezione Frequenza evidenziata.](/help/assets/collaborate/activate/audience-frequency.png)

Se sei soddisfatto delle tue selezioni, seleziona **[!UICONTROL Attiva]** per completare il flusso di lavoro.

## Attiva dashboard {#activate-dashboard}

Nella scheda **[!UICONTROL Attiva]** puoi visualizzare tutti i tipi di pubblico inviati al tuo collaboratore e tutti i tipi di pubblico attivati dal tuo collaboratore nella tua destinazione.

![Il dashboard di attivazione mostra le sezioni Pubblico inviato e Pubblico attivato.](/help/assets/collaborate/activate/activate-dashboard.png)

## Visualizza i tipi di pubblico inviati {#view-sent-audiences}

Nella sezione **[!UICONTROL Tipi di pubblico inviati a]** collaboratori, verranno elencati tutti i tipi di pubblico inviati. Al momento, i tipi di pubblico vengono inviati automaticamente alla destinazione configurata del tuo collaboratore dopo l’invio. Nella visualizzazione del tuo collaboratore, questi tipi di pubblico vengono visualizzati nella sezione **[!UICONTROL Tipi di pubblico attivati]**.

All’interno di ogni pubblico inviato, puoi visualizzare le metriche seguenti:

| Metrica | Descrizione |
|---------|----------|
| **[!UICONTROL Nome]** | Il nome del pubblico. |
| **[!UICONTROL Stato]** | Lo stato del pubblico inviato. |
| **[!UICONTROL Conteggio identità]** | Il numero di identità nel pubblico. |
| **[!UICONTROL Identità sovrapposte]** | Il numero di identità sovrapposte tra questo pubblico e la popolazione totale di profili nell’inventario del collaboratore. |
| **[!UICONTROL Creato]** | La data in cui il pubblico è stato inviato inizialmente. |
| **[!UICONTROL Ultimo invio]** | La data dell’ultimo invio del pubblico al tuo collaboratore. |
| **[!UICONTROL Corrispondenza chiavi]** | Indica la chiave di corrispondenza utilizzata per il pubblico. |

## Visualizzare il pubblico attivato {#view-activated-audiences}

Nella sezione **[!UICONTROL Tipi di pubblico attivati]** puoi visualizzare tutti i tipi di pubblico attivati nella tua destinazione.

All’interno di ogni pubblico attivato, puoi visualizzare le metriche seguenti:

| Metrica | Descrizione |
|---------|----------|
| **[!UICONTROL Nome]** | Il nome del pubblico. |
| **[!UICONTROL Stato]** | Lo stato del pubblico attivato. |
| **[!UICONTROL Conteggio identità]** | Il numero di identità attivate, in base alle identità sovrapposte quando il collaboratore ha inviato il pubblico. |
| **[!UICONTROL Creato]** | La data in cui il pubblico è stato attivato. |
| **[!UICONTROL Ultimo aggiornamento]** | La data dell’ultimo aggiornamento del pubblico, in base alla pianificazione di aggiornamento scelta durante l’attivazione. |
| **[!UICONTROL Destinazione]** | La destinazione in cui è stato attivato il pubblico. |
| **[!UICONTROL Corrispondenza chiavi]** | Indica la chiave di corrispondenza utilizzata per il pubblico. |

## Elimina i tipi di pubblico inviati {#delete-sent-audiences}

Puoi eliminare i tipi di pubblico inviati che non desideri più attivare. Quando elimini un pubblico inviato, questo viene rimosso dalla sezione **[!UICONTROL Tipi di pubblico inviati a]** e non verrà più attivato nella destinazione del tuo collaboratore.

Per eliminare un pubblico inviato, seleziona l&#39;icona **[!UICONTROL Elimina]** (![Elimina.](/help/assets/icons/delete.png)) accanto al pubblico nella sezione **[!UICONTROL Tipi di pubblico inviati a]**.

![Opzione Elimina nella sezione Tipi di pubblico inviati a.](/help/assets/collaborate/activate/delete-sent-audiences.png)

Viene visualizzata una finestra di dialogo di conferma in cui viene richiesto di confermare l’eliminazione. Seleziona **[!UICONTROL Elimina]** per confermare.

![Finestra di conferma eliminazione.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

## Passaggi successivi {#next-steps}

Dopo aver attivato i tipi di pubblico e aver eseguito le campagne, collabora con il team di abilitazione e progettazione di Adobe per caricare i dati di misurazione e visualizzare i [rapporti di misurazione](/help/guide/collaborate/measure.md) corrispondenti.
