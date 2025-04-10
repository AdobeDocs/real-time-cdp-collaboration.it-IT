---
title: Scopri le sovrapposizioni e confronta i tipi di pubblico
description: Scopri le sovrapposizioni tra il pubblico di e quello dei tuoi collaboratori. Scopri come scoprire i tipi di pubblico migliori da utilizzare nelle campagne.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 1%

---

# Scopri le sovrapposizioni e confronta i tipi di pubblico

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L&#39;area di lavoro **[!UICONTROL Discover]** è disponibile solo se il caso di utilizzo **Audience Discovery** è stato abilitato [durante il processo di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, consulta la guida [gestisci progetti](./manage-projects.md#project-use-cases).

Dopo aver [creato un progetto](/help/guide/collaborate/manage-projects.md) all&#39;interno di uno spazio di collaborazione tra un inserzionista e un editore, ora puoi confrontare i tipi di pubblico con quelli del tuo collaboratore. In questo modo, puoi scoprire le sovrapposizioni tra tipi di pubblico e ottenere informazioni suddivise per chiavi di corrispondenza o identità. In questo modo gli inserzionisti possono decidere quali tipi di pubblico condividere con gli editori per l’attivazione.

>[!IMPORTANT]
>
>Tutti gli [schizzi di dati](/help/guide/glossary.md#sketches) non aggiornati o non aggiornati verranno eliminati dopo 7 giorni. In questo caso, i dati visualizzati nei vari rapporti di sovrapposizione di questa pagina diventano pari a zero e la condivisione dei tipi di pubblico non è più disponibile per questi tipi di pubblico scaduti. Gli schizzi dei dati vengono aggiornati automaticamente per i tipi di pubblico con un [programmare](/help/guide/setup/onboard-audiences.md#schedule) di aggiornamento attivo.

![Discover sovrapposizioni](/help/assets/collaborate/discover-overlaps/discover-overlaps.png)

Le chiavi di corrispondenza utilizzate per scoprire e confrontare i tipi di pubblico vengono impostate quando ti [connetti a un editore](/help/guide/connect/establishing-connections.md#connection-settings). Per modificare le percentuali di sovrapposizione indicate in preparazione per la pubblicazione di campagne, puoi rimuovere le chiavi corrispondenza, ma al momento non puoi aggiungere nuove chiavi di corrispondenza. Per fare ciò, vai alle impostazioni](/help/guide/connect/establishing-connections.md#connection-settings) di [connessione tra i collaboratori.

![Modifica schermata dei tasti di corrispondenza](/help/assets/collaborate/discover-overlaps/edit-match-keys.png)

## Prerequisiti {#prerequisites}

Per utilizzare completamente la funzionalità nella scheda **[!UICONTROL Discover]** del flusso di lavoro **[!UICONTROL Collaborate]**, sono già disponibili:

* [Tipi di pubblico importati](/help/guide/setup/onboard-audiences.md)
* [Connessione](/help/guide/connect/establishing-connections.md) con un inserzionista o un editore desiderato con il caso d&#39;uso **Individuazione pubblico** abilitato
* [Ha creato un progetto](/help/guide/collaborate/manage-projects.md) tra te e un collaboratore

Una volta soddisfatti i prerequisiti sopra indicati, puoi iniziare a esplorare e confrontare la sovrapposizione tra il pubblico tuo e quello del tuo collaboratore.

## Confronta i tipi di pubblico {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Confronta i tipi di pubblico"
>abstract="Scopri le sovrapposizioni tra il pubblico dell’e quello del tuo collaboratore. Puoi regolare le impostazioni nel selettore a discesa per scoprire le sovrapposizioni tra uno o più tipi di pubblico rispetto a uno o più tipi di pubblico del tuo collaboratore."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Conteggio delle identità"
>abstract="Il numero di profili con l’identità selezionata che fanno parte del pubblico selezionato"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Conteggio identità collaboratore"
>abstract="Il numero di profili con l&#39;identità selezionata che fanno parte del pubblico selezionato del collaboratore"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Conteggio identità sovrapposte"
>abstract="Il numero di profili con l’identità selezionata presenti sia nel pubblico che nel pubblico del tuo collaboratore"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Percentuale di sovrapposizione delle identità"
>abstract="La percentuale di profili che si sovrappongono tra il pubblico selezionato di e quello del collaboratore."

Utilizza la scheda Confronta tipi di pubblico per ottenere informazioni dettagliate sulla sovrapposizione tra il pubblico tuo e quello del tuo collaboratore. Puoi scegliere di confrontare una delle seguenti combinazioni di pubblico:

* Uno dei tuoi tipi di pubblico contro il pubblico di un collaboratore
* Uno dei tuoi tipi di pubblico contro tutti quelli del tuo collaboratore
* Tutti i tuoi tipi di pubblico rispetto a quelli di un collaboratore
* Tutti i tuoi tipi di pubblico contro tutti i tipi di pubblico dei tuoi collaboratori

Le informazioni visualizzate si riferiscono a:

| Metrica | Descrizione |
|---------|----------|
| **[!UICONTROL Conteggio identità]** (tuo) | Il numero di profili con un&#39;identità selezionata che fanno parte del pubblico selezionato. |
| **[!UICONTROL Conteggio identità]** (tuo collaboratore) | Il numero di profili con un’identità selezionata che fanno parte del pubblico selezionato del tuo collaboratore. |
| **[!UICONTROL Identità sovrapposte]** | Il numero di profili con un’identità selezionata presenti sia nel pubblico che nel pubblico del tuo collaboratore. |
| **[!UICONTROL Percentuale di sovrapposizione]** | La percentuale di profili che si sovrappongono tra il pubblico selezionato di e quello del collaboratore. |
| **[!UICONTROL Identità breakdown da un tasto di corrispondenza]** | In base alle chiavi di corrispondenza concordate con il tuo collaboratore per il progetto, visualizza la composizione delle identità nei calcoli di sovrapposizione per singole chiavi di corrispondenza. |

{style="table-layout:auto"}

>[!TIP]
>
>La percentuale di sovrapposizione potrebbe non essere sempre disponibile per tutti i tipi di pubblico. La visibilità dell&#39;indicatore percentuale di sovrapposizione dipende dall&#39;impostazione scelta dal collaboratore per un pubblico nella [sezione](/help/guide/setup/onboard-audiences.md#metadata-visibility) Visibilità metadati.

## Tipi di pubblico rilevanti {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Tipi di pubblico rilevanti"
>abstract="In base alle percentuali di sovrapposizione, questi tipi di pubblico dell’editore potrebbero essere adatti alla tua campagna. <br><br> Il <b>conteggio identità</b> è la dimensione del pubblico dell&#39;editore. <br><br> <b>La sovrapposizione di identità</b> rappresenta la sovrapposizione tra il pubblico dell&#39;editore consigliato e tutti i tipi di pubblico dell&#39;inserzionista. <br><br> <b>Sovrapposizione %</b> rappresenta il numero di identità sovrapposte diviso per la dimensione di <i>tutti</i> i tipi di pubblico degli inserzionisti."

La visualizzazione **[!UICONTROL Tipi di pubblico rilevanti]** nel modulo **[!UICONTROL Discover]** fornisce un elenco dei primi cinque tipi di pubblico in base alla percentuale di sovrapposizione. Questa funzione consente di identificare rapidamente i tipi di pubblico con la più alta sovrapposizione con i dati correnti, per indirizzare le campagne in modo più efficace.

* **[!UICONTROL Il conteggio]** delle identità corrisponde alla dimensione dell&#39;audience del editore.
* **[!UICONTROL La sovrapposizione di identità]** rappresenta la sovrapposizione tra il pubblico dell&#39;editore consigliato e tutti i tipi di pubblico dell&#39;inserzionista.
* **[!UICONTROL La sovrapposizione %]** rappresenta il numero di identità sovrapposte diviso per la dimensione di *tutti* i tipi di pubblico degli inserzionisti.

![Visualizzazione tipi di pubblico rilevanti](/help/assets/collaborate/discover-overlaps/relevant-audiences-highlighted.png)

## Individuare le sovrapposizioni {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Scopri le sovrapposizioni con i singoli tipi di pubblico"
>abstract="Ottieni informazioni sulla popolazione di questo pubblico e sulle sue sovrapposizioni con l&#39;universo di identità del collaboratore."

![Rileva sovrapposizioni con diverse visualizzazioni del pubblico](/help/assets/collaborate/discover-overlaps/discover-overlaps-cards-view.png)

Ottieni informazioni complete su qualsiasi pubblico del tuo collaboratore e visualizza informazioni di sovrapposizione confrontando questi tipi di pubblico con il numero totale di persone presenti in tutti i tipi di pubblico oppure con tipi di pubblico specifici.

>[!TIP]
>
>Alcuni dei numeri indicati nella schermata potrebbero non essere sempre disponibili per tutti i tipi di pubblico. La loro visibilità dipende dall&#39;impostazione scelta dal collaboratore per un pubblico nella [sezione visibilità metadati](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Passaggi successivi

Dopo aver esplorato e scoperto i tipi di pubblico desiderati, è il momento di [condividere](/help/guide/collaborate/share.md) con il editore i tipi di pubblico da utilizzare nelle campagne.
