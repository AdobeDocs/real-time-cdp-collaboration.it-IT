---
title: Scopri le sovrapposizioni e confronta i tipi di pubblico
description: Scopri le sovrapposizioni tra il pubblico di e quello dei tuoi collaboratori. Scopri come scoprire i tipi di pubblico migliori da utilizzare nelle campagne.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: 3dd37dff0be104894cdfe42503b60056b25018e3
workflow-type: tm+mt
source-wordcount: '2069'
ht-degree: 17%

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
| **[!UICONTROL Indice pubblico]** | Un punteggio che indica quanto fortemente un pubblico si relaziona con un altro in base ai conteggi del pubblico sottostante e alle sovrapposizioni. Per ulteriori informazioni sul significato dei punteggi, consulta la sezione [Punteggio indice pubblico](#audience-index-score). I punteggi dell’indice del pubblico non sono disponibili quando si esegue il confronto con la linea di base del collaboratore (tutti i tipi di pubblico). |
| **[!UICONTROL Raggruppamento identità per chiave di corrispondenza]** | La suddivisione delle identità corrispondenti per ogni chiave di corrispondenza scelta nel progetto, in base ai tipi di pubblico selezionati per ogni collaboratore. |

{style="table-layout:auto"}

>[!NOTE]
>
>La percentuale di sovrapposizione e il punteggio dell’indice del pubblico potrebbero non essere sempre disponibili per tutti i tipi di pubblico. La visibilità della percentuale di sovrapposizione e del punteggio dell&#39;indice del pubblico dipende dall&#39;impostazione scelta dal collaboratore per un pubblico nella [sezione visibilità metadati](/help/guide/setup/onboard-audiences.md#metadata-visibility).

Se il tuo collaboratore non ha abilitato l’indice del pubblico o la percentuale di sovrapposizione, il pubblico non avrà alcun dato di confronto disponibile.

## Tipi di pubblico pertinenti {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Tipi di pubblico pertinenti"
>abstract="In base alle percentuali di sovrapposizione, questi tipi di pubblico potrebbero essere adatti alla tua campagna. <br><br> Il <b>conteggio identità</b> è la dimensione del pubblico del collaboratore. <br><br> La <b>sovrapposizione delle identità</b> rappresenta la sovrapposizione tra il pubblico consigliato e tutti i tuoi tipi di pubblico. <br><br> La <b>% di sovrapposizione</b> rappresenta il numero di identità sovrapposte diviso per la dimensione di <i>tutti</i> i tipi di pubblico."

La sezione **[!UICONTROL Tipi di pubblico rilevanti]** nella scheda **[!UICONTROL Scopri]** fornisce un elenco dei primi cinque tipi di pubblico in base alla percentuale di sovrapposizione tra il pubblico del collaboratore e tutti i tipi di pubblico. Questa funzione consente di identificare rapidamente i tipi di pubblico con la sovrapposizione più elevata, per indirizzare le campagne in modo più efficace. Passa da un pubblico all’altro utilizzando i selettori di pagina in alto a destra della sezione.

![Area di lavoro di individuazione con la sezione Tipi di pubblico rilevanti evidenziata.](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>La visibilità dei tipi di pubblico del collaboratore dipende dall&#39;impostazione scelta dal collaboratore per un pubblico nella [sezione accesso connessione](/help/guide/setup/onboard-audiences.md#connection-access) e nella [sezione visibilità metadati](/help/guide/setup/onboard-audiences.md#metadata-visibility). Se il tuo collaboratore ha impostato tutti i tipi di pubblico su privato, questa sezione non mostra alcun pubblico.

La sezione **[!UICONTROL Tipi di pubblico rilevanti]** visualizza le seguenti informazioni per ogni pubblico consigliato:

| Metrica | Descrizione |
|---------|----------|
| **[!UICONTROL Conteggio identità]** | Il numero di ID univoci all’interno del pubblico. |
| **[!UICONTROL Identità sovrapposte]** | Il numero di ID univoci che si sovrappongono tra il pubblico consigliato e tutti i tipi di pubblico. |
| **[!UICONTROL Sovrapposizione %]** | La percentuale di identità sovrapposte tra il pubblico consigliato e tutti i tipi di pubblico. |
| **[!UICONTROL Indice pubblico]** | Un punteggio che indica quanto fortemente un pubblico si relaziona con un altro in base ai conteggi del pubblico sottostante e alle sovrapposizioni. Per ulteriori informazioni sul significato dei punteggi, consulta la sezione [Punteggio indice pubblico](#audience-index-score). |
| **[!UICONTROL Categorie di pubblico]** | Le categorie assegnate al pubblico dal collaboratore. |
| **[!UICONTROL Corrispondenza chiavi]** | Le chiavi di corrispondenza selezionate dal collaboratore per il pubblico. |

{style="table-layout:auto"}

Se il punteggio dell’indice del pubblico è abilitato per uno dei tipi di pubblico del tuo collaboratore, i tipi di pubblico rilevanti saranno basati sul punteggio dell’indice del pubblico e tutti i tipi di pubblico in cui l’indice del pubblico non è stato abilitato non saranno inclusi. I tipi di pubblico rilevanti in base al punteggio dell’indice di pubblico sono ordinati in modo che venga visualizzato per primo il punteggio dell’indice più alto. Se l’indice del pubblico non è abilitato per nessuno dei tipi di pubblico del tuo collaboratore, i tipi di pubblico rilevanti saranno basati sulla percentuale di sovrapposizione.

## Scopri le sovrapposizioni {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Scopri le sovrapposizioni con i singoli tipi di pubblico"
>abstract="Ottieni informazioni approfondite sulle sovrapposizioni tra i tuoi tipi di pubblico e quelli del tuo collaboratore."

Scopri le sovrapposizioni per ottenere informazioni su come i tipi di pubblico si confrontano con quelli del tuo collaboratore. Per impostazione predefinita, in questa sezione vengono confrontati tutti i tipi di pubblico con quelli di ogni collaboratore. Utilizza il controllo di impaginazione nella parte inferiore della sezione per spostarti tra i tipi di pubblico disponibili.

![Area di lavoro di individuazione con la sezione Rileva sovrapposizioni evidenziata.](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>La visibilità dei tipi di pubblico del collaboratore dipende dall&#39;impostazione scelta dal collaboratore per un pubblico nella [sezione accesso connessione](/help/guide/setup/onboard-audiences.md#connection-access) e nella [sezione visibilità metadati](/help/guide/setup/onboard-audiences.md#metadata-visibility). Se il tuo collaboratore ha impostato tutti i tipi di pubblico su privato, questa sezione non mostra alcun pubblico.

Se il tuo collaboratore non ha abilitato l’indice del pubblico o la percentuale di sovrapposizione, il pubblico non verrà visualizzato.

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
| **[!UICONTROL Indice pubblico]** | Un punteggio che indica quanto fortemente un pubblico si relaziona con un altro in base ai conteggi del pubblico sottostante e alle sovrapposizioni. Per ulteriori informazioni sul significato dei punteggi, consulta la sezione [Punteggio indice pubblico](#audience-index-score). |
| **[!UICONTROL Categorie di pubblico]** | Le categorie assegnate al pubblico dal collaboratore. |
| **[!UICONTROL Corrispondenza chiavi]** | Le chiavi di corrispondenza selezionate dal collaboratore per il pubblico. |

{style="table-layout:auto"}

## Punteggio indice del pubblico {#audience-index-score}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_audience_index_score"
>title="Punteggio indice del pubblico"
>abstract="I punteggi dell’indice del pubblico sono una metrica dettagliata che mostra il livello di relazione di un pubblico rispetto a un altro, in base a conteggi e sovrapposizioni sottostanti del pubblico . Il punteggio dell’indice non elaborato si traduce in fasce di rilevanza, che classificano i punteggi dell’indice del pubblico da molto basso a molto alto. Questo consente di valutare rapidamente il livello di relazione tra il tuo pubblico e il pubblico del tuo collaboratore."

I punteggi dell’indice del pubblico sono una metrica dettagliata che mostra il livello di relazione di un pubblico rispetto a un altro, in base a conteggi e sovrapposizioni sottostanti del pubblico . Questo consente di contestualizzare gli approfondimenti sul pubblico e identificare tipi di pubblico ad alto potenziale per la ricerca di potenziali clienti e il targeting delle campagne.

Il punteggio dell’indice viene calcolato con la seguente formula:

![Formula per il calcolo del punteggio dell&#39;indice.](/help/assets/collaborate/discover/index-score-formula.png)

Immaginate che un produttore di automobili voglia lanciare una campagna pubblicitaria con un grande editore di televisori a colori per un nuovo modello di SUV. Il produttore di automobili dispone di dati su chi attualmente possiede un modello simile e vuole utilizzarlo per trovare ulteriori prospettive per convertirli in clienti. Il produttore dell&#39;auto esamina il pubblico dell&#39;editore di televisori a colori per trovare un pubblico rilevante che corrisponda molto ai proprietari di SUV attuali.

![Pubblico dell&#39;inserzionista dell&#39;auto rispetto a pubblico dell&#39;editore del CTV.](/help/assets/collaborate/discover/audience-index-score-example.png)

Vengono effettuati calcoli del punteggio dell’indice, che possono essere utilizzati per determinare il probabile successo della campagna:

| Pubblico editore CTV | Formula | Punteggio indice (i) | Interpretazione |
|------------------------|-------------|----------------|----------------|
| Linea di base (tutti i tipi di pubblico) | ((1,3 M / 1,3 M) / (50 M / 50 M)) * 100 | 100 | Questo funge da linea di base rispetto alla quale vengono confrontati gli altri tipi di pubblico del tuo collaboratore. |
| Binge Watchers | (500k / 1,3M) / (20M / 50M)) * 100 | 96 | Se si esegue il targeting di questo pubblico, si ha il 4% di probabilità in meno di raggiungere i proprietari di SUV rispetto alla linea di base. |
| Amanti della commedia | ((200 k / 1,3 M) / (6 M / 50 M)) * 100 | 128 | Se si esegue il targeting di questo pubblico, si ha il 28% di probabilità in più di raggiungere i proprietari di SUV rispetto alla linea di base. |
| Maschi 25-34 | ((700k / 1,3M) / (12M / 50M)) * 100 | 224 | Puntando a questo pubblico, hai il 124% di probabilità in più di raggiungere i proprietari di SUV rispetto alla linea di base. |
| Appassionati di tecnologia | ((500k / 1,3M) / (8M / 50M)) * 100 | 240 | Puntando a questo pubblico, hai il 140% di probabilità in più di raggiungere i proprietari di SUV rispetto alla linea di base. |

{style="table-layout:auto"}

Per comprendere meglio in che modo i punteggi dell’indice influiranno sulla campagna, oltre ai punteggi vengono fornite fasce di rilevanza.

### Bande di rilevanza {#audience-index-relevance-bands}

Per consentire un facile confronto tra diversi tipi di pubblico e campagne, Collaboration traduce i punteggi dell’indice in bande di rilevanza (da molto basso a molto alto). Questo consente di valutare rapidamente il livello di relazione tra il tuo pubblico e il pubblico del tuo collaboratore.

| Punteggio indice (i) | Banda di rilevanza | Descrizione |
|---------------|----------|-----------|
| i &lt; 60 | Molto basso | La sovrapposizione è molto meno prevalente nel pubblico di destinazione rispetto al pubblico, il che indica una relazione molto debole. I clienti che utilizzano questo pubblico hanno meno probabilità di raggiungere il pubblico di destinazione. |
| 60 &lt; i &lt; 80 | Basso | La sovrapposizione è un po’ meno prevalente nel pubblico di destinazione rispetto al pubblico, il che suggerisce una relazione debole. È meno probabile che i clienti che utilizzano questo pubblico raggiungano il pubblico di destinazione. |
| 80 &lt; i &lt; 120 | Canale | La sovrapposizione è prevalente nel pubblico di destinazione e nel pubblico, a indicare una relazione tipica. I clienti che utilizzano questo pubblico hanno una probabilità media di raggiungere il loro pubblico di destinazione. |
| 120 &lt; i &lt; 140 | Alto | La sovrapposizione è più prevalente nel pubblico di destinazione rispetto al pubblico, mostrando una forte relazione. È più probabile che i clienti che utilizzano questo pubblico raggiungano il pubblico di destinazione. |
| i > 140 | Molto alto | La sovrapposizione è molto più prevalente nel pubblico di destinazione rispetto al pubblico, il che riflette una relazione molto forte. È molto più probabile che i clienti che utilizzano questo pubblico raggiungano il pubblico di destinazione. |

{style="table-layout:auto"}

Nella sezione scoprire le sovrapposizioni, il punteggio dell’indice del pubblico visualizzerà la banda di rilevanza insieme al punteggio. La partitura sarà codificata con un colore per indicare la banda di rilevanza, facilitando l’identificazione immediata della forza della relazione. Le bande di rilevanza molto bassa e bassa sono visualizzate in arancione, le bande di rilevanza media in nero e le bande di rilevanza alta e molto alta in verde.

## Passaggi successivi

Dopo aver esplorato e individuato i tipi di pubblico desiderati, è ora di [attivare](/help/guide/collaborate/activate.md) i tipi di pubblico da utilizzare nelle campagne.
