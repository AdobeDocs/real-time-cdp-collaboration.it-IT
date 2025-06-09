---
title: Attiva tipi di pubblico
description: Scopri come attivare i tipi di pubblico in Adobe Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: f19aff1b7d10a446dd209721e7a6fdf537c9d63e
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# Attiva tipi di pubblico

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L&#39;area di lavoro **[!UICONTROL Attiva]** è disponibile solo se il caso di utilizzo **Attivazione pubblico** è stato abilitato [durante il processo di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, consulta la guida [gestisci progetti](./manage-projects.md#project-use-cases).

L’attivazione del pubblico consente di attivare i tipi di pubblico nelle campagne. Il processo di attivazione è una collaborazione tra inserzionisti e editori. Dopo aver [individuato i tipi di pubblico migliori per la campagna](./discover.md), i tipi di pubblico possono quindi attivare quelli target. I tipi di pubblico attivati vengono inviati alla destinazione preconfigurata dell’editore, ad esempio Adobe Experience Platform, per l’utilizzo nelle campagne. Per ulteriori informazioni sulla configurazione della destinazione, consulta la guida [panoramica delle destinazioni](../destinations/overview.md).

>[!IMPORTANT]
>
>Attualmente, quando gli inserzionisti attivano i tipi di pubblico, questi vengono automaticamente attivati nella destinazione configurata dall’editore per la loro organizzazione. L&#39;editore **deve** configurare una destinazione *prima* che l&#39;inserzionista attivi un pubblico. Se non è configurata alcuna destinazione, il pubblico verrà inviato all’editore, ma non potrà essere attivato in alcuna campagna.

## Attiva nuovi tipi di pubblico

Per iniziare ad attivare i tipi di pubblico, passa alla scheda **[!UICONTROL Attiva]** nell&#39;area di lavoro del progetto.

Selezionare l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)), oppure l&#39;opzione **[!UICONTROL Attiva pubblico]** se non sono stati inviati tipi di pubblico precedenti per l&#39;attivazione.

![Attiva l&#39;area di lavoro in un progetto senza tipi di pubblico aggiunti.](/help/assets/collaborate/activate/activate-new-audiences.png)

Viene aperto il flusso di lavoro attiva tipi di pubblico, in cui è possibile selezionare il pubblico da inviare al collaboratore. Utilizza il menu a discesa per selezionare un pubblico o cercare un pubblico specifico. Per visualizzare ulteriori informazioni sui tipi di pubblico prima di effettuare la selezione, seleziona **[!UICONTROL Sfoglia tipi di pubblico]**

![Il flusso di lavoro di attivazione del pubblico con le opzioni del menu a discesa e Sfoglia pubblico evidenziate.](/help/assets/collaborate/activate/audience-activation.png)

In **[!UICONTROL Sfoglia tipi di pubblico]**, puoi visualizzare **[!UICONTROL Conteggio identità]**, **[!UICONTROL Identità sovrapposte]** e **[!UICONTROL Sovrapposizione %]** per ogni pubblico.

![Finestra di dialogo Sfoglia tipi di pubblico che mostra i tipi di pubblico disponibili.](/help/assets/collaborate/activate/browse-audiences.png)

Selezionare il pubblico da attivare nelle campagne, quindi selezionare **[!UICONTROL Salva]**. Il pubblico è ora visualizzato ed è possibile visualizzare **[!UICONTROL il conteggio delle identità]**, **[!UICONTROL le identità sovrapposte]** e **[!UICONTROL la sovrapposizione %]** per il pubblico selezionato.

![Il flusso di lavoro di attivazione del pubblico con il pubblico selezionato è visualizzato.](/help/assets/collaborate/activate/audience-selected.png)

### Modifica chiavi di corrispondenza

Successivamente, puoi modificare le chiavi di corrispondenza del pubblico selezionando **[!UICONTROL Modifica chiavi di corrispondenza]** all&#39;interno del pubblico selezionato. Queste opzioni vengono ereditate dalle selezioni delle chiavi di corrispondenza quando è stata impostata inizialmente la connessione tra collaboratori. Puoi rimuovere le chiavi di corrispondenza selezionate se non sono applicabili a una campagna specifica, ma non puoi aggiungerne di nuove.

![Il flusso di lavoro di attivazione del pubblico con l&#39;opzione Modifica chiavi di corrispondenza evidenziata.](/help/assets/collaborate/activate/edit-match-keys.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Modifica chiavi di corrispondenza]**, in cui è possibile disattivare le chiavi di corrispondenza che non si desidera utilizzare. Seleziona **[!UICONTROL Salva]** per salvare le modifiche.

>[!NOTE]
>
>È necessario selezionare almeno una chiave di corrispondenza. Nella versione corrente, le uniche chiavi di corrispondenza disponibili sono **[!UICONTROL E-mail con hash]**, pertanto non è possibile rimuovere questa chiave di corrispondenza.

![Finestra di dialogo Modifica chiavi di corrispondenza nel flusso di lavoro di Audience Activation.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Impostare la frequenza e l&#39;intervallo di aggiornamento del pubblico

Infine, imposta la frequenza e l’intervallo di date desiderati per l’aggiornamento del pubblico. Nella versione corrente, l&#39;unica opzione di frequenza supportata è **[!UICONTROL Once]**. La frequenza **[!UICONTROL Once]** indica che i tipi di pubblico vengono attivati una sola volta e non vengono aggiornati. L&#39;opzione **[!UICONTROL Data]** viene compilata automaticamente con la data corrente.

![Flusso di lavoro di attivazione del pubblico con la sezione Frequenza evidenziata.](/help/assets/collaborate/activate/audience-frequency.png)

Se sei soddisfatto delle tue selezioni, seleziona **[!UICONTROL Attiva]** per completare il flusso di lavoro. Il pubblico è ora attivato e puoi visualizzarlo nella scheda **[!UICONTROL Attiva]**. Sarà inoltre disponibile per il tuo collaboratore nella scheda **[!UICONTROL Attiva]**, dove potrà utilizzarlo nelle campagne.

È possibile modificare l&#39;icona di modifica del nome del pubblico (![Icona matita.](/help/assets/icons/edit.png)) o disattivare il pubblico selezionando **[!UICONTROL Disattiva]**.

![Scheda Attiva con il pubblico attivato visualizzato ed evidenziate le opzioni Modifica e Disattiva.](/help/assets/collaborate/activate/edit-activate-audience.png)

## Visualizzare il pubblico attivato

Nella scheda **[!UICONTROL Attiva]**, sia gli editori che gli inserzionisti possono visualizzare i tipi di pubblico attualmente attivati. Attualmente, i tipi di pubblico vengono inviati automaticamente alla destinazione configurata dall&#39;editore dopo che l&#39;inserzionista li ha attivati.

![Panoramica della scheda Attiva che mostra un pubblico attivato.](/help/assets/collaborate/activate/activate-overview.png)

All’interno di ogni pubblico attivato, puoi visualizzare le metriche seguenti:

| Metrica | Descrizione |
|---------|----------|
| **[!UICONTROL Identità attivate]** | Indica il numero di identità attivate all’interno del pubblico. |
| **[!UICONTROL Identità sovrapposte]** | Indica il numero di identità sovrapposte tra questo pubblico e la popolazione totale di profili nell’inventario del collaboratore. |
| **[!UICONTROL Corrispondenza con suddivisione chiave]** | Mostra il conteggio delle identità per ogni identità utilizzata nel pubblico. Ad esempio, un conteggio di identità totale di 500.000 utenti potrebbe essere costituito da 400.000 utenti ai quali è stata applicata l’identità e-mail con hash e da 100.000 utenti ai quali è stata applicata un’identità ID mobile. Tieni presente che nell’esempio qui descritto, la stessa persona potrebbe essere presente nel pubblico due volte con la propria e-mail e l’identità dell’ID mobile. |

## Passaggi successivi {#next-steps}

Dopo aver attivato i dati e aver eseguito le campagne, collabora con il team di abilitazione e progettazione di Adobe per caricare i dati di misurazione e visualizzare i [rapporti di misurazione](/help/guide/collaborate/measure.md) corrispondenti.
