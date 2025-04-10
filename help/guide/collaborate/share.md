---
title: Condividi tipi di pubblico
description: Scopri come condividere i tipi di pubblico con i tuoi collaboratori per le campagne pubblicitarie.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0fdf0598-89c9-452d-a2e3-ce868df0b9d2
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 1%

---

# Condividi tipi di pubblico

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L&#39;area di lavoro **[!UICONTROL Condividi]** è disponibile solo se il caso di utilizzo **Condivisione e attivazione del pubblico** è stato abilitato [durante il processo di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, consulta la guida [gestisci progetti](./manage-projects.md#project-use-cases).

In qualità di inserzionista, scopri come condividere i tipi di pubblico con gli editori in modo che possano eseguire campagne. Se la tua collaborazione ha abilitato il caso d&#39;uso **Discover audiences**, inizia eseguendo rapporti di sovrapposizione nella [scheda Discover](/help/guide/collaborate/discover.md) per identificare i tipi di pubblico migliori per la condivisione.

## Condividere nuovi tipi di pubblico

Per iniziare a condividere i tipi di pubblico, passa alla scheda **[!UICONTROL Condividi]** nell&#39;area di lavoro del progetto. Solo le **organizzazioni inserzioniste** possono condividere i tipi di pubblico per le campagne. In questo scheda, puoi esaminare e gestire i tipi di pubblico condivisi.

Seleziona il **simbolo più (+)** o l&#39;opzione **[!UICONTROL Condividi pubblico]** se nessun pubblico precedente è stato condiviso, per iniziare il processo di condivisione del pubblico.

![Visualizzazione predefinita senza pubblico condiviso.](/help/assets/collaborate/share/share-new-audiences.png)

Viene visualizzato un nuovo pannello in cui puoi selezionare i tipi di pubblico che desideri condividere con il tuo collaboratore.

![Condividi nuovi tipi di pubblico workflow.](/help/assets/collaborate/share/share-audiences-workflow.png)

### Selezionare i tipi di pubblico da condividere

Nella finestra di selezione del pubblico, puoi ricerca tipi di pubblico specifici da condividere immettendo il nome del pubblico nella barra dei ricerca. Seleziona **[!UICONTROL Sfoglia tipi di]** pubblico e utilizza le opzioni di ordinamento disponibili per trovare esattamente i tipi di pubblico di cui hai bisogno.

![Sfoglia visualizzazione Tipi di pubblico con l&#39;opzione Tipi di pubblico selezionati.](/help/assets/collaborate/share/browse-audiences-view.png)

### Modifica tasti corrispondenti e impostare targeting opzioni

Dopo aver selezionato i tipi di pubblico da condividere, ora puoi selezionare altre opzioni di configurazione per l&#39;attività di condivisione.

![Modifica tasti di corrispondenza e destinazione o sopprimere selettore evidenziato](/help/assets/collaborate/share/match-keys-and-targeting.png)

Seleziona **[!UICONTROL Modifica chiavi di corrispondenza]** per indicare quali chiavi di corrispondenza devono essere utilizzate per le identità nel pubblico. Queste opzioni vengono ereditate dalle impostazioni selezionate al momento della configurazione iniziale della connessione tra collaboratori. Puoi rimuovere le chiavi di corrispondenza selezionate in quel momento se non sono applicabili a questa campagna specifica, ma a questo punto non puoi aggiungere nuove chiavi di corrispondenza.

![Modifica chiavi di corrispondenza.](/help/assets/collaborate/share/update-match-keys.png)

Per ogni pubblico, scegli se desideri like che i membri di quel pubblico siano presi di mira o soppressi nella campagna. In particolare, i profili soppressi non faranno parte del pubblico attivato dall&#39;editore.

### Impostare la frequenza e l&#39;intervallo di aggiornamento del pubblico

Infine, imposta la frequenza e l’intervallo di date desiderati per l’aggiornamento del pubblico. Le modalità attualmente supportate per l&#39;aggiornamento del pubblico sono **[!UICONTROL Una volta]** e **[!UICONTROL Ogni giorno]**.

Quando si seleziona **[!UICONTROL Una volta]**, l&#39;iscrizione al pubblico non viene aggiornata per tutta la durata di una campagna. Quando si seleziona **[!UICONTROL Giornaliero]**, l&#39;iscrizione al pubblico viene aggiornata una volta al giorno per tutta la durata di una campagna.

![Opzioni di frequenza evidenziate.](/help/assets/collaborate/share/audience-refresh-frequency.png)

Se sei soddisfatto delle tue selezioni, seleziona **[!UICONTROL Condividi]** per completare il flusso di lavoro.

>[!SUCCESS]
>
>Ora puoi vedere una nuova attività di condivisione del **[!UICONTROL pubblico nel scheda Condivisione]** . Se necessario, puoi tornare indietro e modificare qualsiasi selezione effettuata.

## Visualizza tipi di pubblico attualmente condivisi

**[!UICONTROL Nella scheda Condivisione]** è possibile visualizzare i tipi di pubblico attualmente condivisi tra i collaboratori, raggruppati in attività di condivisione del pubblico.

![Panoramica dell&#39;scheda di condivisione.](/help/assets/collaborate/share/share-tab-overview.png)

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

All&#39;interno di ogni attività di condivisione del pubblico, puoi ottenere informazioni su ogni pubblico condiviso.

| Metrica | Descrizione |
|---------|----------|
| **[!UICONTROL Numero di identità]** | Indica il numero di profili per tutte le identità legate a questo pubblico, secondo l&#39;ultima valutazione del conteggio delle identità. Questi numeri vengono aggiornati ogni 24 ore. |
| **[!UICONTROL Identità sovrapposte]** | Indica il numero di identità sovrapposte tra i membri di questo pubblico e la popolazione totale di profili nell&#39;inventario del collaboratore. |
| **[!UICONTROL Corrispondenza con suddivisione chiave]** | Mostra il conteggio delle identità per ogni identità utilizzata nel pubblico. Ad esempio, un conteggio di identità totale di 500.000 utenti potrebbe essere costituito da 400.000 utenti ai quali è stata applicata l’identità e-mail con hash e da 100.000 utenti ai quali è stata applicata un’identità ID mobile. Tieni presente che nell’esempio qui descritto, la stessa persona potrebbe essere presente nel pubblico due volte con la propria e-mail e l’identità dell’ID mobile. |
| **[!UICONTROL Oggetto]** | **[!UICONTROL Sopprimere]** o **[!UICONTROL Target]**. Indica se i membri di un pubblico devono essere oggetto di targeting o esclusi dalle campagne. |

La pagina fornisce anche controlli per sospendere **[!UICONTROL la condivisione]** e **[!UICONTROL Modifica i tipi di]** pubblico.

## Modifica tipi di pubblico {#edit-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_share_edit_audiences_usecases"
>title="Target o sopprimere il caso d&#39;uso"
>abstract="<p>Seleziona **Target** se desideri che ai profili del pubblico vengano mostrati annunci pubblicitari nella campagna.</p> <p>Selezionate **Elimina** se desiderate escludere i profili del pubblico dalla campagna messaggistica.</p>"

Seleziona **[!UICONTROL Modifica tipi di]** pubblico per modificare i tipi di pubblico condivisi in un modulo di condivisione del pubblico, nonché per modificare diverse configurazioni relative al modo in cui i tipi di pubblico vengono condivisi.

![Visualizza della modalità di modifica dei tipi di pubblico](/help/assets/collaborate/share/edit-audiences-modal.png)

<!--

Search for audiences that you want to add to the sharing module. 

For each audience, you can select whether you'd like to target or suppress those profiles in campaigns. 

To remove an audience from the sharing module, select the trash can icon [TODO: add spectrum icon and folder].

Select how often you would like the audience membership to be refreshed and the date range within which you want the membership of the audience to be refreshed. 

TODO: are there any limitations for frequency in the M1 release?

-->

## Passaggi successivi

Una volta che il editore riceve i tipi di pubblico condivisi, li [attiva](/help/guide/collaborate/activate.md) nelle pubblicità digitale campagne.
