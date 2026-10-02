---
title: Attiva tipi di pubblico
description: Scopri come inviare tipi di pubblico e attivare automaticamente o manualmente quelli ricevuti nelle destinazioni in Adobe Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
TQID: https://experienceleague.adobe.com/bfPHtcW8Mf6RhIlg5fKcJmPSEKDyAODjbNRJ5D3SMkQ
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
    internal-label: Use cases
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: df0c7fe0d09203a02a192931135abaa1715e593f
workflow-type: tm+mt
source-wordcount: '2043'
ht-degree: 1%
---
# Attiva tipi di pubblico

Utilizza la scheda **[!UICONTROL Attiva]** all&#39;interno di un progetto per inviare i tipi di pubblico al tuo collaboratore, esaminare quelli ricevuti dal tuo collaboratore e attivare quelli ricevuti per la consegna a una destinazione configurata. L’attivazione può essere creata automaticamente quando il pubblico viene ricevuto o manualmente dal collaboratore ricevente. Per configurare e gestire le destinazioni dall&#39;area di lavoro **[!UICONTROL Activation]** di primo livello, vedere la [panoramica delle destinazioni](../destinations/overview.md).

>[!IMPORTANT]
>
>La scheda **[!UICONTROL Attiva]** è disponibile solo se il caso di utilizzo **Attivazione pubblico** è stato abilitato [durante il processo di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, vedere [Gestione progetti](./manage-projects.md#project-use-cases).

Utilizza la [scheda Discover](./discover.md) per identificare i tipi di pubblico che meglio corrispondono alla tua campagna, quindi inviali al tuo collaboratore.

Se il ricevitore configura una destinazione di attivazione automatica nelle impostazioni di connessione, il mittente seleziona una pianificazione di attivazione durante l’invio del pubblico. La destinazione è di sola lettura per il mittente. Quando il pubblico viene ricevuto, viene attivato automaticamente nella destinazione configurata dal destinatario in base alla pianificazione di attivazione del mittente. Per le istruzioni di configurazione della connessione, vedere [Configurare una destinazione di attivazione automatica](../connect/manage-connections.md#configure-auto-activation-destination).

Se il ricevitore non ha configurato una destinazione di attivazione automatica, l&#39;invio e l&#39;attivazione rimangono azioni separate. L’invio dà al ricevitore l’accesso a un pubblico e il ricevitore seleziona una destinazione e una pianificazione al momento dell’attivazione manuale. Solo le destinazioni preconfigurate possono essere selezionate per l’attivazione all’interno di un progetto. Per istruzioni sulla configurazione della destinazione, vedi [Gestire le destinazioni](../destinations/manage-destinations.md).

Le sezioni e le azioni disponibili dipendono dal fatto che l’organizzazione invii o riceva tipi di pubblico nel progetto. La scheda **[!UICONTROL Attiva]** contiene le sezioni seguenti:

| Sezione | Descrizione |
|---|---|
| **[!UICONTROL Pubblico inviato a [collaboratore]]** | Tipi di pubblico inviati al tuo collaboratore. |
| **[!UICONTROL Pubblico ricevuto]** | Tipi di pubblico che il tuo collaboratore ti ha inviato e che sono disponibili per l’attivazione. |
| **[!UICONTROL Tipi di pubblico attivati]** | Pubblico ricevuto con attivazioni create automaticamente o manualmente. |

![Scheda Attiva a livello di progetto con i conteggi di riepilogo nelle sezioni Pubblico inviato, Pubblico ricevuto e Pubblico attivato nella parte superiore ed espansa. In ogni sezione vengono visualizzati i conteggi dello stato e una tabella dei dettagli del pubblico.](/help/assets/collaborate/activate/activate-dashboard.png){zoomable="yes"}

## Prerequisiti {#prerequisites}

Prima di inviare o attivare i tipi di pubblico, assicurati di:

- I tipi di pubblico provengono e sono disponibili per l’invio. Per ulteriori informazioni, consulta [Source e gestire i tipi di pubblico](../setup/onboard-audiences.md).
- I tipi di pubblico soddisfano la soglia minima di sovrapposizione di 1000 identità richiesta per l’invio e l’attivazione.
- I tipi di pubblico sono configurati con le chiavi di corrispondenza richieste quando si utilizzano tipi di pubblico con più chiavi di corrispondenza.
- Se devi attivare i tipi di pubblico ricevuti, è configurata almeno una destinazione. Per ulteriori informazioni, consulta la [panoramica delle destinazioni](../destinations/overview.md).
- Per l&#39;attivazione automatica, il destinatario possiede una destinazione attiva e l&#39;ha selezionata come [destinazione di attivazione automatica](../connect/manage-connections.md#configure-auto-activation-destination) della connessione.

## Invia tipi di pubblico {#send-audiences}

Invia un pubblico per consentire al tuo collaboratore di accedervi. Dopo l&#39;invio, il pubblico viene visualizzato nella sezione **[!UICONTROL Tipi di pubblico inviati a [Collaboratore]]** e nella sezione **[!UICONTROL Tipi di pubblico ricevuti]** del collaboratore.

Passa a **[!UICONTROL Collabora]**, apri un progetto, quindi seleziona la scheda **[!UICONTROL Attiva]**.

Nella sezione **[!UICONTROL Tipi di pubblico inviati a [collaboratore]]**, selezionare l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)). Se non è stato inviato alcun pubblico, seleziona **[!UICONTROL Invia pubblico]** dalla visualizzazione vuota.

![Scheda Attiva a livello di progetto quando non è stato inviato alcun pubblico. Il messaggio di visualizzazione vuoto spiega che non hai inviato un pubblico e visualizza un pulsante Invia pubblico.](/help/assets/collaborate/activate/activate-new-audiences.png){zoomable="yes"}

Verrà aperto il flusso di lavoro **[!UICONTROL Invia pubblico]**. Utilizza il selettore del pubblico per trovare un pubblico, oppure seleziona **[!UICONTROL Sfoglia i tipi di pubblico]** per confrontare i tipi di pubblico disponibili.

>[!IMPORTANT]
>
>Per l’attivazione sono disponibili solo i tipi di pubblico con più di 1000 identità sovrapposte. Se le sovrapposizioni di pubblico sono vicine alla soglia di identità 1000, l’attivazione potrebbe non riuscire.

![Il flusso di lavoro Invia tipi di pubblico con un selettore di pubblico e un pulsante Sfoglia tipi di pubblico. Il flusso di lavoro consente al mittente di scegliere un pubblico prima di configurare le chiavi di corrispondenza e le impostazioni di accesso.](/help/assets/collaborate/activate/audience-activation.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL Sfoglia tipi di pubblico]**, controlla **[!UICONTROL Numero identità]**, **[!UICONTROL Identità sovrapposte]** e **[!UICONTROL Sovrapposizione %]** per ogni pubblico.

![La finestra di dialogo Sfoglia tipi di pubblico elenca i tipi di pubblico disponibili con il relativo conteggio di identità, il conteggio di identità sovrapposto e la percentuale di sovrapposizione.](/help/assets/collaborate/activate/browse-audiences.png){zoomable="yes"}

>[!IMPORTANT]
>
>Se un pubblico utilizza più chiavi di corrispondenza, ogni chiave di corrispondenza selezionata deve soddisfare la soglia di sovrapposizione richiesta. Utilizza la [scheda Discover](./discover.md) per verificare che il pubblico soddisfi i requisiti di sovrapposizione prima di inviarlo.

Selezionare il pubblico da inviare, quindi selezionare **[!UICONTROL Salva]**.

Il pubblico selezionato viene visualizzato nel flusso di lavoro con le relative informazioni di identità e sovrapposizione.

![Il flusso di lavoro Invia tipi di pubblico con un pubblico selezionato mostra il relativo conteggio identità, il conteggio identità sovrapposto, la percentuale di sovrapposizione, le chiavi di corrispondenza e l&#39;opzione Modifica chiavi di corrispondenza.](/help/assets/collaborate/activate/audience-selected.png){zoomable="yes"}

### Modifica chiavi di corrispondenza {#edit-match-keys}

Utilizza le chiavi di corrispondenza configurate per la connessione collaboratore oppure rimuovi eventuali chiavi di corrispondenza non applicabili al pubblico.

Seleziona **[!UICONTROL Modifica chiavi di corrispondenza]** nel pubblico selezionato.

![Il pubblico selezionato nel flusso di lavoro Invia tipi di pubblico con l&#39;opzione Modifica chiavi di corrispondenza evidenziata.](/help/assets/collaborate/activate/edit-match-keys.png){zoomable="yes"}

Viene visualizzata la finestra di dialogo **[!UICONTROL Modifica chiavi di corrispondenza]**. Disattivare le chiavi di corrispondenza che non si desidera utilizzare, quindi selezionare **[!UICONTROL Salva]**.

>[!NOTE]
>
>Deve rimanere selezionata almeno una chiave di corrispondenza.

![La finestra di dialogo Modifica chiavi di corrispondenza con i controlli di attivazione/disattivazione per le chiavi di corrispondenza disponibili tramite la connessione collaborator e un pulsante Salva.](/help/assets/collaborate/activate/edit-match-keys-selection.png){zoomable="yes"}

### Configurare l’accesso del pubblico {#configure-audience-access}

Configura il modo in cui il pubblico viene inviato e per quanto tempo il collaboratore può accedervi.

Utilizzare il controllo **[!UICONTROL Durata accesso]** per selezionare una delle opzioni seguenti:

- **[!UICONTROL Invia ora (una sola volta)]**: invia il pubblico una sola volta. Il collaboratore ricevente può attivarla una volta.
- **[!UICONTROL Pianificazione dell&#39;invio di un pubblico ricorrente]**: aggiorna il pubblico durante un periodo di accesso specificato. Utilizzare il controllo **[!UICONTROL Intervallo date]** per selezionare le date di inizio e di fine.

![Il passaggio della durata di accesso nel flusso di lavoro Invia tipi di pubblico con le opzioni per inviare il pubblico una volta o pianificare un invio ricorrente. L&#39;opzione ricorrente visualizza i controlli data per la definizione del periodo di accesso.](/help/assets/collaborate/activate/activation-frequency.png)

### Scegli una pianificazione di attivazione automatica {#auto-activation-schedule}

Se il tuo collaboratore ha configurato una destinazione di attivazione automatica per la connessione, la sezione **[!UICONTROL Activation]** indica che **[!UICONTROL Auto-Activate]** è abilitato. La destinazione selezionata dal ricevitore viene visualizzata in sola lettura. In qualità di mittente, utilizza **[!UICONTROL Frequenza]** per scegliere quando eseguire l&#39;attivazione:

- **[!UICONTROL Attiva ora (una tantum)]**: esegui l&#39;attivazione una volta quando il pubblico viene ricevuto.
- **[!UICONTROL Pianificazione dell&#39;attivazione di un pubblico una tantum]**: esegui l&#39;attivazione una volta alla data e all&#39;ora future selezionate.
- **[!UICONTROL Pianifica attivazione ricorrente]**: esegui l&#39;attivazione in base alla pianificazione configurata durante l&#39;intervallo di date selezionato.

![Il flusso di lavoro Invia tipi di pubblico con l&#39;attivazione automatica abilitata e il menu Frequenza che mostra le opzioni di attivazione immediata, futura e ricorrente.](/help/assets/collaborate/activate/choose-auto-activation-schedule.png){zoomable="yes"}

Per un’attivazione ricorrente, configura la pianificazione di attivazione, l’ora di inizio e l’intervallo di date. L&#39;attivazione automatica supporta pianificazioni immediate, future, una tantum o ricorrenti; non è richiesta la ricorrenza.

![Il flusso di lavoro Invia tipi di pubblico è configurato con una pianificazione di attivazione giornaliera ricorrente, un&#39;ora di inizio e un intervallo di date.](/help/assets/collaborate/activate/configure-recurring-auto-activation.png){zoomable="yes"}

Al termine delle impostazioni relative al pubblico e all&#39;accesso, selezionare **[!UICONTROL Invia]**.

Il pubblico viene visualizzato nella sezione **[!UICONTROL Tipi di pubblico inviati a [collaboratore]]**. Il tuo collaboratore può esaminarlo nella sezione **[!UICONTROL Tipi di pubblico ricevuti]**. Se l&#39;attivazione automatica è abilitata, Collaboration crea anche l&#39;attivazione per il ricevitore e l&#39;attivazione viene eseguita in base alla pianificazione selezionata.

## Visualizza i tipi di pubblico inviati {#view-sent-audiences}

Utilizza la sezione **[!UICONTROL Tipi di pubblico inviati a [collaboratore]]** per rivedere i tipi di pubblico inviati e monitorarne lo stato di accesso corrente.

Ogni pubblico inviato visualizza le seguenti informazioni:

| Colonna | Descrizione |
|---|---|
| **[!UICONTROL Nome pubblico]** | Nome del pubblico inviato. |
| **[!UICONTROL Stato]** | Lo stato di accesso corrente del pubblico. |
| **[!UICONTROL Conteggio identità]** | Il numero di identità nel pubblico. |
| **[!UICONTROL Identità sovrapposte]** | Il numero di identità che si sovrappongono all&#39;inventario del tuo collaboratore. |
| **[!UICONTROL Creato]** | La data e l’ora del primo invio del pubblico. |
| **[!UICONTROL Ultimo invio]** | La data e l’ora dell’ultimo invio dei dati sul pubblico al tuo collaboratore. |
| **[!UICONTROL Durata dell&#39;accesso]** | L’impostazione di accesso configurata al momento dell’invio del pubblico. |
| **[!UICONTROL Corrispondenza chiavi]** | Le chiavi di corrispondenza utilizzate durante l’invio del pubblico. |

### Eliminare un pubblico inviato {#delete-sent-audience}

Elimina un pubblico inviato per rimuoverlo dall’elenco dei tipi di pubblico inviati e revocare l’accesso del tuo collaboratore.

Selezionare l&#39;icona Elimina (![Icona Elimina.](/help/assets/icons/delete.png)) accanto al pubblico nella sezione **[!UICONTROL Pubblico inviato a [collaboratore]]**.

![La sezione Tipi di pubblico inviati con l&#39;icona Elimina visualizzata accanto a una riga di pubblico.](/help/assets/collaborate/activate/delete-sent-audiences.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo di conferma. Seleziona **[!UICONTROL Elimina]** per confermare.

![La finestra di dialogo di conferma dell&#39;eliminazione del pubblico inviato spiega che il pubblico verrà rimosso e il collaboratore perderà l&#39;accesso, con i pulsanti Annulla ed Elimina.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

Il pubblico viene rimosso dalla sezione e il tuo collaboratore non è più in grado di accedervi.

## Visualizzare i tipi di pubblico ricevuti {#received-audiences}

Utilizza la sezione **[!UICONTROL Tipi di pubblico ricevuti]** per esaminare i tipi di pubblico che il tuo collaboratore ti ha inviato. Se prima dell’invio del pubblico è stata configurata una destinazione di attivazione automatica, Collaboration crea automaticamente un’attivazione alla ricezione del pubblico. Per le attivazioni automatiche ricorrenti, puoi anche creare un’ulteriore attivazione manuale in un’altra destinazione. Per ulteriori informazioni, vedere [Attivare manualmente un pubblico ricevuto](#activate-received-audience). Se non è stata configurata alcuna destinazione di attivazione automatica, attiva manualmente il pubblico.

Ogni pubblico ricevuto visualizza le seguenti informazioni:

| Colonna | Descrizione |
|---|---|
| **[!UICONTROL Nome pubblico]** | Nome del pubblico ricevuto. |
| **[!UICONTROL Stato]** | Lo stato di accesso corrente del pubblico. |
| **[!UICONTROL Conteggio identità]** | Il numero di identità nel pubblico. |
| **[!UICONTROL Identità sovrapposte]** | Il numero di identità che si sovrappongono al tuo inventario. |
| **[!UICONTROL Ultima esecuzione del flusso di dati]** | La data e l’ora del flusso di dati più recente eseguito per il pubblico. |
| **[!UICONTROL Durata dell&#39;accesso]** | L’impostazione di accesso configurata dal collaboratore che ha inviato il pubblico. |
| **[!UICONTROL Corrispondenza chiavi]** | Le chiavi di corrispondenza utilizzate per il pubblico. |

![La sezione Tipi di pubblico ricevuti con conteggi dei pubblici attivi e scaduti. Ogni riga del pubblico mostra il nome, lo stato, le informazioni sull&#39;identità, l&#39;ultima esecuzione del flusso di dati, la durata dell&#39;accesso, le chiavi di corrispondenza e un&#39;icona di aggiunta utilizzata per iniziare l&#39;attivazione.](/help/assets/collaborate/activate/received-audiences-section.png){zoomable="yes"}

### Attivare manualmente un pubblico ricevuto {#activate-received-audience}

Attiva manualmente un pubblico ricevuto per inviare i suoi dati a una delle destinazioni configurate.

Nella sezione **[!UICONTROL Tipi di pubblico ricevuti]**, seleziona l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) accanto al pubblico che desideri attivare.

Viene visualizzata la finestra di dialogo **[!UICONTROL Attiva pubblico]**.

Utilizza **[!UICONTROL Destinazione]** per selezionare la destinazione che riceve i dati del pubblico. Se l&#39;elenco di destinazione è vuoto, configura una destinazione prima di continuare. Per istruzioni, consulta la [panoramica delle destinazioni](../destinations/overview.md).

Configura la **[!UICONTROL Frequenza]** e i controlli di pianificazione disponibili per scegliere quando e con quale frequenza eseguire l&#39;attivazione. Quindi seleziona **[!UICONTROL Attiva]**.

L&#39;esempio seguente mostra il flusso di lavoro di attivazione manuale con **[!UICONTROL Esportazioni pubblico Northstar]** selezionata come destinazione.

![Esempio della finestra di dialogo Attiva pubblico manuale per i clienti Northstar Fall Campaign, con le esportazioni di pubblico Northstar selezionate e una pianificazione giornaliera, un&#39;ora di inizio e un intervallo di date configurati.](/help/assets/collaborate/activate/manually-activate-received-audience.png){zoomable="yes"}

>[!NOTE]
>
>Per un pubblico ricevuto con un’attivazione automatica ricorrente, puoi creare manualmente un’ulteriore attivazione per tale pubblico su una destinazione diversa. L&#39;attivazione automatica ricorrente continua in modo indipendente.

La finestra di dialogo si chiude e l&#39;attivazione viene visualizzata nella sezione **[!UICONTROL Tipi di pubblico attivati]**. Il pubblico ricevuto rimane disponibile nella sezione **[!UICONTROL Tipi di pubblico ricevuti]** mentre il relativo accesso rimane attivo.

## Visualizzare il pubblico attivato {#activated-audiences}

Utilizza la sezione **[!UICONTROL Tipi di pubblico attivati]** per confermare quali tipi di pubblico ricevuti hanno creato automaticamente o manualmente le attivazioni e rivederne lo stato di destinazione e di consegna. Le attivazioni create automaticamente vengono visualizzate qui senza richiedere al ricevitore di completare il flusso di lavoro di attivazione manuale.

![La scheda Attiva mostra i clienti di Northstar Fall Campaign nei tipi di pubblico ricevuti e la relativa attivazione giornaliera creata automaticamente per le esportazioni di pubblico Northstar nei tipi di pubblico attivati.](/help/assets/collaborate/activate/view-auto-activated-audience.png){zoomable="yes"}

Ogni pubblico attivato visualizza le seguenti informazioni:

| Colonna | Descrizione |
|---|---|
| **[!UICONTROL Nome pubblico]** | Nome del pubblico attivato. |
| **[!UICONTROL Stato]** | Stato di attivazione corrente. |
| **[!UICONTROL Conteggio attivati]** | Il numero di identità attivate nella destinazione. |
| **[!UICONTROL Ultimo aggiornamento]** | La data e l’ora dell’ultimo aggiornamento del pubblico attivato. |
| **[!UICONTROL Destinazione]** | La destinazione che riceve i dati sul pubblico. |
| **[!UICONTROL Frequenza]** | La frequenza di attivazione, ad esempio una pianificazione una tantum o ricorrente. |
| **[!UICONTROL Data]** | La data o l’intervallo di date in cui viene eseguita l’attivazione. |
| **[!UICONTROL Corrispondenza chiavi]** | Le chiavi di corrispondenza incluse nel pubblico attivato. |

![Sezione Tipi di pubblico attivati con conteggi di attivazione attivi, archiviati e in pausa. Ogni riga mostra il nome del pubblico, lo stato, il conteggio attivato, la data dell&#39;ultimo aggiornamento, la destinazione, la frequenza, la data di attivazione, le chiavi di corrispondenza e un&#39;icona di eliminazione.](/help/assets/collaborate/activate/activated-audiences-section.png){zoomable="yes"}

### Eliminare un pubblico attivato {#delete-activated-audience}

Elimina un pubblico attivato per rimuovere l&#39;attivazione dalla sezione **[!UICONTROL Tipi di pubblico attivati]**.

Selezionare l&#39;icona Elimina (![Icona Elimina.](/help/assets/icons/delete.png)) accanto al pubblico attivato.

Viene visualizzata una finestra di dialogo di conferma. Seleziona **[!UICONTROL Elimina]** per confermare.

![La finestra di dialogo di conferma dell&#39;eliminazione del pubblico attivato indica che il pubblico verrà rimosso dall&#39;elenco dei tipi di pubblico attivati e potrà essere riattivato in seguito, con i pulsanti Annulla ed Elimina.](/help/assets/collaborate/activate/delete-activated-audience-confirmation.png)

L&#39;attivazione viene rimossa dall&#39;elenco. Puoi attivare nuovamente il pubblico ricevuto finché il suo accesso rimane attivo.

## Passaggi successivi {#next-steps}

Dopo aver inviato o attivato i tipi di pubblico, monitorane lo stato nelle sezioni **[!UICONTROL Tipi di pubblico inviati a [Collaboratori]]** e **[!UICONTROL Tipi di pubblico attivati]**. Al termine delle campagne, contatta il team di abilitazione e progettazione di Adobe per caricare i dati di misurazione e visualizzare i [rapporti di misurazione](./measure.md) corrispondenti.
