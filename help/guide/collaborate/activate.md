---
title: Attiva tipi di pubblico
description: Scopri come inviare tipi di pubblico ai collaboratori e attivare manualmente quelli ricevuti nelle destinazioni in Adobe Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
TQID: https://experienceleague.adobe.com/bfPHtcW8Mf6RhIlg5fKcJmPSEKDyAODjbNRJ5D3SMkQ
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 5d12a5004a6854392c130fd6b93a841fb22cf6ab
workflow-type: tm+mt
source-wordcount: 1565
ht-degree: 2%

---

# Attiva tipi di pubblico

Utilizza la scheda **[!UICONTROL Attiva]** all&#39;interno di un progetto per inviare i tipi di pubblico al tuo collaboratore, esaminare quelli ricevuti dal tuo collaboratore e attivare quelli ricevuti per la consegna a una destinazione configurata. Per configurare e gestire le destinazioni dall&#39;area di lavoro **[!UICONTROL Activation]** di primo livello, vedere la [panoramica delle destinazioni](../destinations/overview.md).

>[!IMPORTANT]
>
>La scheda **[!UICONTROL Attiva]** è disponibile solo se il caso di utilizzo **Attivazione pubblico** è stato abilitato [durante il processo di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, vedere [Gestione progetti](./manage-projects.md#project-use-cases).

Utilizza la [scheda Discover](./discover.md) per identificare i tipi di pubblico che meglio corrispondono alla tua campagna, quindi inviali al tuo collaboratore. Il collaboratore ricevente seleziona una destinazione configurata e pianifica l’attivazione del pubblico ricevuto.

L&#39;invio e l&#39;attivazione sono azioni separate. L’invio offre al tuo collaboratore l’accesso a un pubblico. Il collaboratore ricevente seleziona quindi una destinazione e attiva manualmente il pubblico ricevuto.

Le sezioni e le azioni disponibili dipendono dal fatto che l’organizzazione invii o riceva tipi di pubblico nel progetto. La scheda **[!UICONTROL Attiva]** contiene le sezioni seguenti:

| Sezione | Descrizione |
|---|---|
| **[!UICONTROL Pubblico inviato a [collaboratore]]** | Tipi di pubblico inviati al tuo collaboratore. |
| **[!UICONTROL Pubblico ricevuto]** | Tipi di pubblico che il tuo collaboratore ti ha inviato e che sono disponibili per l’attivazione. |
| **[!UICONTROL Tipi di pubblico attivati]** | Hai ricevuto tipi di pubblico che hai attivato in una destinazione. |

![Scheda Attiva a livello di progetto con i conteggi di riepilogo nelle sezioni Pubblico inviato, Pubblico ricevuto e Pubblico attivato nella parte superiore ed espansa. In ogni sezione vengono visualizzati i conteggi dello stato e una tabella dei dettagli del pubblico.](/help/assets/collaborate/activate/activate-dashboard.png)

## Prerequisiti {#prerequisites}

Prima di inviare o attivare i tipi di pubblico, assicurati di:

- I tipi di pubblico provengono e sono disponibili per l’invio. Per ulteriori informazioni, consulta [Source e gestire i tipi di pubblico](../setup/onboard-audiences.md).
- Se devi attivare i tipi di pubblico ricevuti, è configurata almeno una destinazione. Per ulteriori informazioni, consulta la [panoramica delle destinazioni](../destinations/overview.md).

## Invia tipi di pubblico {#send-audiences}

Invia un pubblico per consentire al tuo collaboratore di accedervi. Dopo l&#39;invio, il pubblico viene visualizzato nella sezione **[!UICONTROL Tipi di pubblico inviati a [Collaboratore]]** e nella sezione **[!UICONTROL Tipi di pubblico ricevuti]** del collaboratore.

Passa a **[!UICONTROL Collabora]**, apri un progetto, quindi seleziona la scheda **[!UICONTROL Attiva]**.

Nella sezione **[!UICONTROL Tipi di pubblico inviati a [collaboratore]]**, selezionare l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)). Se non è stato inviato alcun pubblico, seleziona **[!UICONTROL Invia pubblico]** dalla visualizzazione vuota.

![Scheda Attiva a livello di progetto quando non è stato inviato alcun pubblico. Il messaggio di visualizzazione vuoto spiega che non hai inviato un pubblico e visualizza un pulsante Invia pubblico.](/help/assets/collaborate/activate/activate-new-audiences.png)

Verrà aperto il flusso di lavoro **[!UICONTROL Invia pubblico]**. Utilizza il selettore del pubblico per trovare un pubblico, oppure seleziona **[!UICONTROL Sfoglia i tipi di pubblico]** per confrontare i tipi di pubblico disponibili.

![Il flusso di lavoro Invia tipi di pubblico con un selettore di pubblico e un pulsante Sfoglia tipi di pubblico. Il flusso di lavoro consente al mittente di scegliere un pubblico prima di configurare le chiavi di corrispondenza e le impostazioni di accesso.](/help/assets/collaborate/activate/audience-activation.png)

Nella finestra di dialogo **[!UICONTROL Sfoglia tipi di pubblico]**, controlla **[!UICONTROL Numero identità]**, **[!UICONTROL Identità sovrapposte]** e **[!UICONTROL Sovrapposizione %]** per ogni pubblico.

![La finestra di dialogo Sfoglia tipi di pubblico elenca i tipi di pubblico disponibili con il relativo conteggio di identità, il conteggio di identità sovrapposto e la percentuale di sovrapposizione.](/help/assets/collaborate/activate/browse-audiences.png)

>[!IMPORTANT]
>
>Se un pubblico utilizza più chiavi di corrispondenza, ogni chiave di corrispondenza selezionata deve soddisfare la soglia di sovrapposizione richiesta. Utilizza la [scheda Discover](./discover.md) per verificare che il pubblico soddisfi i requisiti di sovrapposizione prima di inviarlo.

Selezionare il pubblico da inviare, quindi selezionare **[!UICONTROL Salva]**.

Il pubblico selezionato viene visualizzato nel flusso di lavoro con le relative informazioni di identità e sovrapposizione.

![Il flusso di lavoro Invia tipi di pubblico con un pubblico selezionato mostra il relativo conteggio identità, il conteggio identità sovrapposto, la percentuale di sovrapposizione, le chiavi di corrispondenza e l&#39;opzione Modifica chiavi di corrispondenza.](/help/assets/collaborate/activate/audience-selected.png)

### Modifica chiavi di corrispondenza {#edit-match-keys}

Utilizza le chiavi di corrispondenza configurate per la connessione collaboratore oppure rimuovi eventuali chiavi di corrispondenza non applicabili al pubblico.

Seleziona **[!UICONTROL Modifica chiavi di corrispondenza]** nel pubblico selezionato.

![Il pubblico selezionato nel flusso di lavoro Invia tipi di pubblico con l&#39;opzione Modifica chiavi di corrispondenza evidenziata.](/help/assets/collaborate/activate/edit-match-keys.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Modifica chiavi di corrispondenza]**. Disattivare le chiavi di corrispondenza che non si desidera utilizzare, quindi selezionare **[!UICONTROL Salva]**.

>[!NOTE]
>
>Deve rimanere selezionata almeno una chiave di corrispondenza.

![La finestra di dialogo Modifica chiavi di corrispondenza con i controlli di attivazione/disattivazione per le chiavi di corrispondenza disponibili tramite la connessione collaborator e un pulsante Salva.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Configurare l’accesso del pubblico {#configure-audience-access}

Configura il modo in cui il pubblico viene inviato e per quanto tempo il collaboratore può accedervi.

Utilizzare il controllo **[!UICONTROL Durata accesso]** per selezionare una delle opzioni seguenti:

- **[!UICONTROL Invia ora (una sola volta)]**: invia il pubblico una sola volta. Il collaboratore ricevente può attivarla una volta.
- **[!UICONTROL Pianificazione dell&#39;invio di un pubblico ricorrente]**: aggiorna il pubblico durante un periodo di accesso specificato. Utilizzare il controllo **[!UICONTROL Intervallo date]** per selezionare le date di inizio e di fine.

![Il passaggio della durata di accesso nel flusso di lavoro Invia tipi di pubblico con le opzioni per inviare il pubblico una volta o pianificare un invio ricorrente. L&#39;opzione ricorrente visualizza i controlli data per la definizione del periodo di accesso.](/help/assets/collaborate/activate/activation-frequency.png)

Al termine delle impostazioni relative al pubblico e all&#39;accesso, selezionare **[!UICONTROL Invia]**.

Il pubblico viene visualizzato nella sezione **[!UICONTROL Tipi di pubblico inviati a [collaboratore]]**. Il tuo collaboratore può esaminarlo nella sezione **[!UICONTROL Tipi di pubblico ricevuti]**.

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

![La sezione Tipi di pubblico inviati con l&#39;icona Elimina visualizzata accanto a una riga di pubblico.](/help/assets/collaborate/activate/delete-sent-audiences.png)

Viene visualizzata una finestra di dialogo di conferma. Seleziona **[!UICONTROL Elimina]** per confermare.

![La finestra di dialogo di conferma dell&#39;eliminazione del pubblico inviato spiega che il pubblico verrà rimosso e il collaboratore perderà l&#39;accesso, con i pulsanti Annulla ed Elimina.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

Il pubblico viene rimosso dalla sezione e il tuo collaboratore non è più in grado di accedervi.

## Visualizzare i tipi di pubblico ricevuti {#received-audiences}

Utilizza la sezione **[!UICONTROL Tipi di pubblico ricevuti]** per esaminare i tipi di pubblico che il tuo collaboratore ti ha inviato. Un pubblico ricevuto deve essere attivato manualmente prima che i relativi dati vengano inviati a una destinazione.

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

![La sezione Tipi di pubblico ricevuti con conteggi dei pubblici attivi e scaduti. Ogni riga del pubblico mostra il nome, lo stato, le informazioni sull&#39;identità, l&#39;ultima esecuzione del flusso di dati, la durata dell&#39;accesso, le chiavi di corrispondenza e un&#39;icona di aggiunta utilizzata per iniziare l&#39;attivazione.](/help/assets/collaborate/activate/received-audiences-section.png)

### Attivare un pubblico ricevuto {#activate-received-audience}

Attiva un pubblico ricevuto per inviare i suoi dati a una delle destinazioni configurate.

Nella sezione **[!UICONTROL Tipi di pubblico ricevuti]**, seleziona l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) accanto al pubblico che desideri attivare.

Viene visualizzata la finestra di dialogo **[!UICONTROL Attiva pubblico]**.

Utilizza **[!UICONTROL Destinazione]** per selezionare la destinazione che riceve i dati del pubblico. Se l&#39;elenco di destinazione è vuoto, configura una destinazione prima di continuare. Per istruzioni, consulta la [panoramica delle destinazioni](../destinations/overview.md).

Utilizza **[!UICONTROL Data]** per selezionare la data di esecuzione dell&#39;attivazione, quindi seleziona **[!UICONTROL Attiva]**.

![La finestra di dialogo Attiva pubblico è stata aperta da un pubblico ricevuto. La finestra di dialogo contiene un elenco a discesa Destinazione per selezionare una destinazione configurata, un campo Data con un controllo calendario e i pulsanti Annulla e Attiva.](/help/assets/collaborate/activate/activate-received-audience.png)

La finestra di dialogo si chiude e l&#39;attivazione viene visualizzata nella sezione **[!UICONTROL Tipi di pubblico attivati]**. Il pubblico ricevuto rimane disponibile nella sezione **[!UICONTROL Tipi di pubblico ricevuti]** mentre il relativo accesso rimane attivo.

## Visualizzare il pubblico attivato {#activated-audiences}

Utilizza la sezione **[!UICONTROL Tipi di pubblico attivati]** per verificare quali tipi di pubblico ricevuti sono stati attivati e rivederne lo stato di destinazione e di consegna.

Ogni pubblico attivato visualizza le seguenti informazioni:

| Colonna | Descrizione |
|---|---|
| **[!UICONTROL Nome pubblico]** | Nome del pubblico attivato. |
| **[!UICONTROL Stato]** | Stato di attivazione corrente. |
| **[!UICONTROL Conteggio attivati]** | Il numero di identità attivate nella destinazione. |
| **[!UICONTROL Ultimo aggiornamento]** | La data e l’ora dell’ultimo aggiornamento del pubblico attivato. |
| **[!UICONTROL Destinazione]** | La destinazione che riceve i dati sul pubblico. |
| **[!UICONTROL Frequenza]** | La frequenza di attivazione. Le attivazioni manuali vengono visualizzate **[!UICONTROL Una volta]**. |
| **[!UICONTROL Data]** | La data in cui viene eseguita l’attivazione. |
| **[!UICONTROL Corrispondenza chiavi]** | Le chiavi di corrispondenza incluse nel pubblico attivato. |

![Sezione Tipi di pubblico attivati con conteggi di attivazione attivi, archiviati e in pausa. Ogni riga mostra il nome del pubblico, lo stato, il conteggio attivato, la data dell&#39;ultimo aggiornamento, la destinazione, la frequenza, la data di attivazione, le chiavi di corrispondenza e un&#39;icona di eliminazione.](/help/assets/collaborate/activate/activated-audiences-section.png)

### Eliminare un pubblico attivato {#delete-activated-audience}

Elimina un pubblico attivato per rimuovere l&#39;attivazione dalla sezione **[!UICONTROL Tipi di pubblico attivati]**.

Selezionare l&#39;icona Elimina (![Icona Elimina.](/help/assets/icons/delete.png)) accanto al pubblico attivato.

Viene visualizzata una finestra di dialogo di conferma. Seleziona **[!UICONTROL Elimina]** per confermare.

![La finestra di dialogo di conferma dell&#39;eliminazione del pubblico attivato indica che il pubblico verrà rimosso dall&#39;elenco dei tipi di pubblico attivati e potrà essere riattivato in seguito, con i pulsanti Annulla ed Elimina.](/help/assets/collaborate/activate/delete-activated-audience-confirmation.png)

L&#39;attivazione viene rimossa dall&#39;elenco. Puoi attivare nuovamente il pubblico ricevuto finché il suo accesso rimane attivo.

## Passaggi successivi {#next-steps}

Dopo aver inviato o attivato i tipi di pubblico, monitorane lo stato nelle sezioni **[!UICONTROL Tipi di pubblico inviati a [Collaboratori]]** e **[!UICONTROL Tipi di pubblico attivati]**. Al termine delle campagne, contatta il team di abilitazione e progettazione di Adobe per caricare i dati di misurazione e visualizzare i [rapporti di misurazione](./measure.md) corrispondenti.
