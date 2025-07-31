---
title: Scopri le sovrapposizioni e confronta i tipi di pubblico
description: Scopri le sovrapposizioni tra il pubblico di e quello dei tuoi collaboratori. Scopri come scoprire i tipi di pubblico migliori da utilizzare nelle campagne.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 20%

---

# Scopri le sovrapposizioni e confronta i tipi di pubblico

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L&#39;area di lavoro **[!UICONTROL Discover]** è disponibile solo se il caso di utilizzo **Audience Discovery** è stato abilitato [durante il processo di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, consulta la guida [gestisci progetti](./manage-projects.md#project-use-cases).

Dopo la [creazione di un progetto](/help/guide/collaborate/manage-projects.md), puoi confrontare i tuoi tipi di pubblico con i tuoi collaboratori. Questo consente di identificare i tipi di pubblico rilevanti per le campagne e decidere quali inviare ai collaboratori per l’attivazione.

>[!IMPORTANT]
>
>Tutti gli [schizzi di dati](/help/guide/glossary.md#sketches) non aggiornati o non aggiornati verranno eliminati dopo 7 giorni. In questo caso, i dati visualizzati nei vari rapporti di sovrapposizione di questa pagina diventano pari a zero e la condivisione dei tipi di pubblico non è più disponibile per questi tipi di pubblico scaduti. Gli schizzi di dati vengono aggiornati automaticamente per i tipi di pubblico con [pianificazione di aggiornamento attiva](/help/guide/setup/onboard-audiences.md#schedule).

Le chiavi di corrispondenza utilizzate per individuare e confrontare i tipi di pubblico sono impostate [durante il processo di connessione](/help/guide/connect/establishing-connections.md#connection-settings). I tasti di corrispondenza consentono di calcolare la sovrapposizione tra i tipi di pubblico e possono essere attivati e disattivati. Per modificare le chiavi di corrispondenza, selezionare l&#39;opzione **[!UICONTROL Modifica chiavi di corrispondenza]**.

![Area di lavoro della scheda Rileva, in cui sono visualizzate le informazioni sul pubblico.](/help/assets/collaborate/discover/discover-overview.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Modifica chiavi di corrispondenza]**, in cui è possibile disattivare le chiavi di corrispondenza che non si desidera utilizzare. Seleziona **[!UICONTROL Salva]** per salvare le modifiche.

![Finestra di dialogo Modifica chiavi di corrispondenza nell&#39;area di lavoro di individuazione.](/help/assets/collaborate/discover/edit-match-keys.png)

## Prerequisiti {#prerequisites}

Per iniziare a utilizzare la scheda **[!UICONTROL Discover]** all&#39;interno del progetto, è necessario disporre di:

* [Pubblico di origine](/help/guide/setup/onboard-audiences.md) nel tuo account
* [Connesso](/help/guide/connect/establishing-connections.md) con un collaboratore con il caso d&#39;uso **Individuazione pubblico** abilitato
* [Ha creato un progetto](/help/guide/collaborate/manage-projects.md) tra te e un collaboratore

Una volta soddisfatti questi prerequisiti, puoi iniziare a esplorare e confrontare le sovrapposizioni tra te e il pubblico del tuo collaboratore.

## Confronta i tipi di pubblico {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Confronta i tipi di pubblico"
>abstract="Scopri le sovrapposizioni tra il tuo pubblico e quello del tuo collaboratore. Puoi regolare le impostazioni nel selettore a discesa per scoprire le sovrapposizioni tra uno o più tipi del tuo pubblico rispetto a uno o più tipi di pubblico del tuo collaboratore."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Conteggio identità personale"
>abstract="Il numero di ID univoci all’interno del pubblico selezionato, in base alle chiavi di corrispondenza concordate tra te e il tuo collaboratore per il progetto."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Conteggio identità collaboratore"
>abstract="Il numero di ID univoci all’interno del pubblico del tuo collaboratore, in base alle chiavi di corrispondenza concordate tra te e il collaboratore per il progetto."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Conteggio identità sovrapposte"
>abstract="Il numero di ID univoci presenti sia nel tuo pubblico che in quello del tuo collaboratore, in base alle chiavi di corrispondenza concordate tra te e il collaboratore per il progetto."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Percentuale di sovrapposizione delle identità"
>abstract="La percentuale di identità che si sovrappongono tra il tuo pubblico selezionato e quello del tuo collaboratore."

Utilizza la sezione confronto tipi di pubblico per ottenere informazioni dettagliate sulla sovrapposizione tra i tipi di pubblico dell’utente e quelli del collaboratore. Per modificare la selezione del pubblico, utilizza il selettore a discesa nella parte superiore della sezione **[!UICONTROL Confronta tipi di pubblico]**. Puoi selezionare uno o tutti i tipi di pubblico e uno o tutti i tipi di pubblico del tuo collaboratore da confrontare tra loro.

![L&#39;area di lavoro di individuazione con il selettore del pubblico evidenziato nella sezione Confronta tipi di pubblico.](/help/assets/collaborate/discover/compare-audiences-selector.png)

Nella sezione confrontare tipi di pubblico, puoi visualizzare le metriche seguenti, basate sulle chiavi di corrispondenza concordate tra te e il tuo collaboratore per il progetto:

| Metrica | Descrizione |
|---------|----------|
| **[!UICONTROL Conteggio identità]** (tuo) | Il numero di ID univoci all&#39;interno dei tipi di pubblico selezionati. |
| **[!UICONTROL Conteggio identità]** (tuo collaboratore) | Il numero di ID univoci all’interno del pubblico del collaboratore. |
| **[!UICONTROL Identità sovrapposte]** | Il numero di ID univoci presenti sia nel pubblico dell’utente che in quello del collaboratore. |
| **[!UICONTROL Sovrapposizione %]** | La percentuale di profili che si sovrappongono tra il tuo pubblico selezionato e quello del tuo collaboratore. |
| **[!UICONTROL Raggruppamento identità per chiave di corrispondenza]** | La suddivisione delle identità per ogni chiave di corrispondenza scelta nel progetto, in base ai tipi di pubblico selezionati per ogni collaboratore. |

{style="table-layout:auto"}

>[!NOTE]
>
>La percentuale di sovrapposizione potrebbe non essere sempre disponibile per tutti i tipi di pubblico. La visibilità dell&#39;indicatore della percentuale di sovrapposizione dipende dall&#39;impostazione scelta dal collaboratore per un pubblico nella [sezione visibilità metadati](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Tipi di pubblico pertinenti {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Tipi di pubblico pertinenti"
>abstract="In base alle percentuali di sovrapposizione, questi tipi di pubblico potrebbero essere adatti alla tua campagna. <br><br> Il <b>conteggio identità</b> è la dimensione del pubblico del collaboratore. <br><br> La <b>sovrapposizione delle identità</b> rappresenta la sovrapposizione tra il pubblico consigliato e tutti i tuoi tipi di pubblico. <br><br> La <b>% di sovrapposizione</b> rappresenta il numero di identità sovrapposte diviso per la dimensione di <i>tutti</i> i tipi di pubblico."

La sezione **[!UICONTROL Tipi di pubblico rilevanti]** nella scheda **[!UICONTROL Scopri]** fornisce un elenco dei primi cinque tipi di pubblico in base alla percentuale di sovrapposizione tra il pubblico del collaboratore e tutti i tipi di pubblico. Questa funzione consente di identificare rapidamente i tipi di pubblico con la sovrapposizione più elevata, per indirizzare le campagne in modo più efficace. Passa da un pubblico all’altro utilizzando i selettori di pagina in alto a destra della sezione.

![Area di lavoro di individuazione con la sezione Tipi di pubblico rilevanti evidenziata.](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>La visibilità dei tipi di pubblico del collaboratore dipende dall&#39;impostazione scelta dal collaboratore per un pubblico nella [sezione visibilità metadati](/help/guide/setup/onboard-audiences.md#metadata-visibility). Se il tuo collaboratore ha impostato tutti i tipi di pubblico su privato, questa sezione non mostra alcun pubblico.

La sezione **[!UICONTROL Tipi di pubblico rilevanti]** visualizza le seguenti informazioni per ogni pubblico consigliato:

| Metrica | Descrizione |
|---------|----------|
| **[!UICONTROL Conteggio identità]** | Il nome degli ID univoci all’interno del pubblico. |
| **[!UICONTROL Identità sovrapposte]** | Il numero di ID univoci che si sovrappongono tra il pubblico consigliato e tutti i tipi di pubblico. |
| **[!UICONTROL Sovrapposizione %]** | La percentuale di identità sovrapposte tra il pubblico consigliato e tutti i tipi di pubblico. |
| **[!UICONTROL Categorie di pubblico]** | Le categorie assegnate al pubblico dal collaboratore. |
| **[!UICONTROL Corrispondenza chiavi]** | Le chiavi di corrispondenza selezionate dal collaboratore per il pubblico. |

{style="table-layout:auto"}

## Scopri le sovrapposizioni {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Scopri le sovrapposizioni con i singoli tipi di pubblico"
>abstract="Ottieni informazioni approfondite sulle sovrapposizioni tra i tuoi tipi di pubblico e quelli del tuo collaboratore."

Scopri le sovrapposizioni per ottenere informazioni su come i tipi di pubblico si confrontano con quelli del tuo collaboratore. Per impostazione predefinita, in questa sezione vengono confrontati tutti i tipi di pubblico con quelli di ogni collaboratore. Utilizza il controllo di impaginazione nella parte inferiore della sezione per spostarti tra i tipi di pubblico disponibili.

![Area di lavoro di individuazione con la sezione Rileva sovrapposizioni evidenziata.](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>La visibilità dei tipi di pubblico del collaboratore dipende dall&#39;impostazione scelta dal collaboratore per un pubblico nella [sezione visibilità metadati](/help/guide/setup/onboard-audiences.md#metadata-visibility). Se il tuo collaboratore ha impostato tutti i tipi di pubblico su privato, questa sezione non mostra alcun pubblico.

Per modificare la selezione del pubblico, seleziona **[!UICONTROL Cambia pubblico]**.

![Area di lavoro di individuazione con l&#39;opzione Cambia pubblico evidenziata.](/help/assets/collaborate/discover/change-audience.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Modifica pubblico]**, in cui è possibile selezionare un pubblico specifico da confrontare con quelli del collaboratore. Seleziona i tipi di pubblico desiderati o cancella le selezioni per selezionare tutti i tipi di pubblico, quindi seleziona **[!UICONTROL Salva]**.

![Finestra di dialogo Modifica pubblico nell&#39;area di lavoro di individuazione.](/help/assets/collaborate/discover/change-audience-selection.png)

Dopo aver selezionato i tipi di pubblico desiderati, nella sezione **[!UICONTROL Individua sovrapposizioni]** vengono visualizzate le seguenti informazioni per ogni pubblico:

| Metrica | Descrizione |
|---------|----------|
| **[!UICONTROL Conteggio identità]** | Il numero di ID univoci all’interno del pubblico. |
| **[!UICONTROL Identità sovrapposte]** | Il numero di ID univoci che si sovrappongono tra il pubblico consigliato e tutti i tipi di pubblico. |
| **[!UICONTROL Sovrapposizione %]** | La percentuale di identità sovrapposte tra il pubblico consigliato e tutti i tipi di pubblico. |
| **[!UICONTROL Categorie di pubblico]** | Le categorie assegnate al pubblico dal collaboratore. |
| **[!UICONTROL Corrispondenza chiavi]** | Le chiavi di corrispondenza selezionate dal collaboratore per il pubblico. |

{style="table-layout:auto"}

## Passaggi successivi

Dopo aver esplorato e individuato i tipi di pubblico desiderati, è ora di [attivare](/help/guide/collaborate/activate.md) i tipi di pubblico da utilizzare nelle campagne.
