---
title: Condividi tipi di pubblico
description: Scopri come condividere i tipi di pubblico con i tuoi collaboratori per le campagne pubblicitarie.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0fdf0598-89c9-452d-a2e3-ce868df0b9d2
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 6%

---

# Condividi tipi di pubblico

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L&#39;area di lavoro **[!UICONTROL Condividi]** è disponibile solo se il caso di utilizzo **Condivisione e attivazione del pubblico** è stato abilitato [durante il processo di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, consulta la guida [gestisci progetti](./manage-projects.md#project-use-cases).

In qualità di inserzionista, scopri come condividere i tipi di pubblico con gli editori in modo che possano eseguire campagne. Se la tua collaborazione ha abilitato il caso d&#39;uso **Discover audiences**, inizia eseguendo rapporti di sovrapposizione nella [scheda Discover](/help/guide/collaborate/discover.md) per identificare i tipi di pubblico migliori per la condivisione.

## Condividere nuovi tipi di pubblico

Per iniziare a condividere i tipi di pubblico, passa alla scheda **[!UICONTROL Condividi]** nell&#39;area di lavoro del progetto. Solo le **organizzazioni inserzioniste** possono condividere i tipi di pubblico per le campagne. In questa scheda puoi rivedere e gestire i tipi di pubblico condivisi.

Per iniziare il processo di condivisione del pubblico, seleziona il simbolo **Plus (+)** o l&#39;opzione **[!UICONTROL Condividi pubblico]** se non sono stati condivisi tipi di pubblico precedenti.

![Visualizzazione predefinita senza tipi di pubblico condivisi.](/help/assets/collaborate/share/share-new-audiences.png)

Viene visualizzato un nuovo pannello in cui è possibile selezionare i tipi di pubblico che si desidera condividere con il collaboratore.

![Condividi nuovo flusso di lavoro tipi di pubblico.](/help/assets/collaborate/share/share-audiences-workflow.png)

### Seleziona i tipi di pubblico da condividere

Nella finestra di selezione del pubblico, puoi cercare tipi di pubblico specifici da condividere immettendo il nome del pubblico nella barra di ricerca. Seleziona **[!UICONTROL Sfoglia tipi di pubblico]** e utilizza le opzioni di ordinamento disponibili per trovare i tipi di pubblico esatti necessari.

![Sfoglia visualizzazione tipi di pubblico con tipi di pubblico selezionati.](/help/assets/collaborate/share/browse-audiences-view.png)

### Modifica le chiavi di corrispondenza e imposta le opzioni di targeting

Dopo aver selezionato i tipi di pubblico desiderati da condividere, ora puoi selezionare altre opzioni di configurazione per l’attività di condivisione.

![Il selettore di destinazione e le chiavi di corrispondenza sono evidenziati](/help/assets/collaborate/share/match-keys-and-targeting.png)

Seleziona **[!UICONTROL Modifica chiavi di corrispondenza]** per indicare quali chiavi di corrispondenza devono essere utilizzate per le identità nel pubblico. Queste opzioni vengono ereditate dalle impostazioni selezionate al momento della configurazione iniziale della connessione tra collaboratori. Puoi rimuovere le chiavi di corrispondenza selezionate in quel momento se non sono applicabili a questa campagna specifica, ma a questo punto non puoi aggiungere nuove chiavi di corrispondenza.

![Modifica chiavi di corrispondenza.](/help/assets/collaborate/share/update-match-keys.png)

Per ogni pubblico, seleziona se desideri che i membri del pubblico vengano targetizzati o soppressi nella campagna. I profili eliminati non faranno specificamente parte del pubblico attivato dall’editore.

### Impostare la frequenza e l&#39;intervallo di aggiornamento del pubblico

Infine, imposta la frequenza e l’intervallo di date desiderati per l’aggiornamento del pubblico. Le modalità attualmente supportate per l&#39;aggiornamento del pubblico sono **[!UICONTROL Una volta]** e **[!UICONTROL Ogni giorno]**.

Quando si seleziona **[!UICONTROL Una volta]**, l&#39;iscrizione al pubblico non viene aggiornata per tutta la durata di una campagna. Quando si seleziona **[!UICONTROL Giornaliero]**, l&#39;iscrizione al pubblico viene aggiornata una volta al giorno per tutta la durata di una campagna.

![Opzioni di frequenza evidenziate.](/help/assets/collaborate/share/audience-refresh-frequency.png)

Se sei soddisfatto delle tue selezioni, seleziona **[!UICONTROL Condividi]** per completare il flusso di lavoro.

>[!SUCCESS]
>
>Ora puoi visualizzare una nuova attività di condivisione del pubblico nella scheda **[!UICONTROL Condivisione]**. Se lo desideri, puoi tornare indietro e modificare qualsiasi selezione effettuata.

## Visualizzare i tipi di pubblico attualmente condivisi

Nella scheda **[!UICONTROL Condivisione]**, puoi visualizzare i tipi di pubblico attualmente condivisi tra i collaboratori, raggruppati in attività di condivisione del pubblico.

![Panoramica della scheda Condivisione.](/help/assets/collaborate/share/share-tab-overview.png)

<!--

The banner at the top of the page shows figures across all audience sharing activities. 

![The hero banner in the sharing tab.](/help/assets/collaborate/share/share-hero-banner.png)


|Metric | Description |
|---------|----------|
| **[!UICONTROL Shared audiences]** | Indicates the number of audiences shared between collaborators in this project, across all audience sharing modules. |
| **[!UICONTROL Estimated addressable reach]** | Indicates the approximate number of profiles that you can reach across all the audiences that are currently shared in the project. [TODO: ADD INFORMATION ABOUT HOW THIS IS CALCULATED] |
| **[!UICONTROL Target identities]** | The number of identities across all audiences shared in this project for which you selected to target the profiles. |
| **[!UICONTROL Suppress identities]** | The number of identities across all audiences shared in this project for which you selected to suppress the profiles and thereby not target them in campaigns. |

-->

All’interno di ogni attività di condivisione del pubblico, puoi ottenere informazioni su ogni pubblico condiviso.

| Metrica | Descrizione |
|---------|----------|
| **[!UICONTROL Conteggio identità]** | Indica il numero di profili per tutte le identità associate a questo pubblico, in base all’ultima valutazione del conteggio delle identità. Questi numeri vengono aggiornati ogni 24 ore. |
| **[!UICONTROL Identità sovrapposte]** | Indica il numero di identità sovrapposte tra i membri di questo pubblico e la popolazione totale di profili nell&#39;inventario del collaboratore. |
| **[!UICONTROL Corrispondenza con suddivisione chiave]** | Mostra il conteggio delle identità per ogni identità utilizzata nel pubblico. Ad esempio, un conteggio di identità totale di 500.000 utenti potrebbe essere costituito da 400.000 utenti ai quali è stata applicata l’identità e-mail con hash e da 100.000 utenti ai quali è stata applicata un’identità ID mobile. Tieni presente che nell’esempio qui descritto, la stessa persona potrebbe essere presente nel pubblico due volte con la propria e-mail e l’identità dell’ID mobile. |
| **[!UICONTROL Oggetto]** | **[!UICONTROL Elimina]** o **[!UICONTROL Destinazione]**. Indica se i membri di un pubblico devono essere oggetto di targeting o esclusi dalle campagne. |

La pagina fornisce inoltre i controlli per **[!UICONTROL Sospendere la condivisione]** e **[!UICONTROL Modificare i tipi di pubblico]**.

## Modifica i tipi di pubblico {#edit-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_share_edit_audiences_usecases"
>title="Targeting o soppressione del caso d’uso"
>abstract="<p>Se desideri che ai profili nel pubblico vengano mostrati gli annunci nella campagna, seleziona **Targeting**.</p> <p>Se desideri escludere i profili nel pubblico dai messaggi della campagna, seleziona **Soppressione**.</p>"

Seleziona **[!UICONTROL Modifica tipi di pubblico]** per modificare quali tipi di pubblico sono condivisi in un modulo di condivisione del pubblico e per modificare diverse configurazioni relative al modo in cui i tipi di pubblico vengono condivisi.

![Visualizzazione del modale di modifica dei tipi di pubblico](/help/assets/collaborate/share/edit-audiences-modal.png)

<!--

Search for audiences that you want to add to the sharing module. 

For each audience, you can select whether you'd like to target or suppress those profiles in campaigns. 

To remove an audience from the sharing module, select the trash can icon [TODO: add spectrum icon and folder].

Select how often you would like the audience membership to be refreshed and the date range within which you want the membership of the audience to be refreshed. 

TODO: are there any limitations for frequency in the M1 release?

-->

## Passaggi successivi

Dopo che l&#39;editore avrà ricevuto i tipi di pubblico condivisi, adesso li [attiverà](/help/guide/collaborate/activate.md) nelle campagne pubblicitarie digitali.
