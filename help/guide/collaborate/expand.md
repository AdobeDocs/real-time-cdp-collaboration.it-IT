---
title: Creare tipi di pubblico di espansione in Espandi
description: Scopri come creare tipi di pubblico di espansione da un pubblico di seed utilizzando la popolazione di pubblico di un collaboratore in Adobe Real-Time CDP Collaboration.
source-git-commit: d2585628407acf10ad8388231259c77991a9a0b0
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 1%
---
# (Beta) Creare tipi di pubblico di espansione in Espandi

Utilizza la scheda **[!UICONTROL Espandi]** all&#39;interno di un progetto per creare un pubblico di espansione da uno dei tuoi tipi di pubblico. Collaboration utilizza la popolazione di pubblico del tuo collaboratore per trovare profili simili al pubblico di partenza, consentendoti di raggiungere nuovi potenziali clienti senza esporre i dati di pubblico sottostanti del tuo collaboratore. Il pubblico di espansione risultante viene inviato al tuo collaboratore per l’attivazione.

## Prerequisiti {#prerequisites}

Prima di poter utilizzare la scheda **[!UICONTROL Espandi]**, è necessario disporre di:

* [Originato](/help/guide/setup/onboard-audiences.md) almeno un pubblico da utilizzare come pubblico di seed
* [Connesso](/help/guide/connect/establishing-connections.md) a un collaboratore
* [Ha creato un progetto](/help/guide/collaborate/manage-projects.md) con quel collaboratore
* Se ricevi un pubblico di espansione, una [destinazione](/help/guide/destinations/overview.md) configurata per ricevere i tipi di pubblico attivati

## Espandi panoramica {#expand-overview}

Passa a **[!UICONTROL Collabora]** > **[!UICONTROL Progetti personali]**, apri un progetto e seleziona la scheda **[!UICONTROL Espandi]**.

La pagina **[!UICONTROL Espandi]** mostra i tipi di pubblico di espansione creati per questo collaboratore e l&#39;opzione per crearne uno nuovo.

![Scheda Espandi che mostra la tabella Tipi di pubblico di espansione con le colonne Nome, Stato, Dimensione modello, Raggiungimento pubblico e Ultimo aggiornamento.](/help/assets/collaborate/expand/expand-overview.png){zoomable="yes"}

Nella tabella **[!UICONTROL Tipi di pubblico per l&#39;espansione]** sono elencati tutti i tipi di pubblico per l&#39;espansione creati nel progetto:

| Colonna | Descrizione |
|---|---|
| **[!UICONTROL Nome]** | Nome del pubblico di espansione. Viene impostato automaticamente sul nome del pubblico di partenza fino alla modifica. |
| **[!UICONTROL Stato]** | Lo stato corrente del pubblico di espansione. Per ulteriori dettagli, vedere [stato pubblico di espansione](#expansion-audience-status). |
| **[!UICONTROL Dimensioni modello]** | Dimensione del pubblico di espansione generato. Non disponibile fino al completamento dell&#39;elaborazione del modello. |
| **[!UICONTROL Destinazione pubblico]** | L’impostazione di portata del pubblico utilizzata per il pubblico di espansione. |
| **[!UICONTROL Ultimo aggiornamento]** | La data e l’ora dell’ultimo aggiornamento del pubblico di espansione. |

{style="table-layout:auto"}

### Stato del pubblico di espansione {#expansion-audience-status}

Un pubblico di espansione si sposta attraverso i seguenti stati:

| Stato | Descrizione |
|---|---|
| **[!UICONTROL Elaborazione]** | Il modello di espansione sta ancora generando il pubblico di espansione. |
| **[!UICONTROL Bozza]** | Il modello è stato completato e il pubblico di espansione è pronto per la revisione e l’invio al tuo collaboratore. |
| **[!UICONTROL Attivo]** | Hai inviato il pubblico dell’espansione al tuo collaboratore. |

{style="table-layout:auto"}

>[!NOTE]
>
>Lo stato non viene aggiornato in tempo reale. Riapri o aggiorna la scheda **[!UICONTROL Espandi]** per visualizzare lo stato più recente.

## Creare un pubblico di espansione {#create-expansion-audience}

Per creare un nuovo pubblico di espansione, seleziona l&#39;icona Aggiungi (![icona Aggiungi.](/help/assets/icons/plus.png)) nella pagina **[!UICONTROL Espandi]**, quindi seleziona **[!UICONTROL Crea un pubblico esteso]**.


Viene visualizzata la finestra di dialogo **[!UICONTROL Genera un pubblico di espansione]**. Completa ogni campo per generare il pubblico di espansione.

![Finestra di dialogo Genera espansione pubblico con i campi Pubblico di seed, Raggiungimento pubblico, Chiave di corrispondenza e Membri del pubblico di seed.](/help/assets/collaborate/expand/generate-expansion-audience-dialog.png){zoomable="yes"}

### Seleziona il pubblico seed {#select-seed-audience}

Seleziona uno dei tuoi tipi di pubblico dal menu a discesa **[!UICONTROL Seleziona il pubblico seed]**. Collaboration utilizza questo pubblico come base per trovare profili simili nella popolazione del tuo collaboratore.

![Campo Pubblico seed nella finestra di dialogo Genera espansione pubblico.](/help/assets/collaborate/expand/select-seed-audience.png){zoomable="yes"}

### Seleziona una chiave di corrispondenza {#select-match-key}

Abilita una chiave di corrispondenza per il pubblico di espansione. Non è possibile abilitarne più di uno.

| ID persona | ID dispositivo |
|---|---|
| **[!UICONTROL E-mail con hash]** | **[!UICONTROL IPv4 con hash]** |
| **[!UICONTROL Telefono con hash]** | **[!UICONTROL GAID]** |
| **[!UICONTROL ID fedeltà]** | **[!UICONTROL IDFA]** |
| **[!UICONTROL ID CRM]** | **[!UICONTROL ID demdex]** |

{style="table-layout:auto"}

>[!NOTE]
>
>Se il pubblico seed non include una determinata chiave di corrispondenza, tale opzione appare disabilitata e non può essere selezionata.

![Sezione Corrispondenza chiave nella finestra di dialogo Genera espansione pubblico con le opzioni disponibili per la chiave di corrispondenza.](/help/assets/collaborate/expand/select-match-key.png){zoomable="yes"}

### Seleziona la portata del pubblico {#select-audience-reach}

Utilizza il menu a discesa **[!UICONTROL Audience reach]** per bilanciare l&#39;analogia con il pubblico seed e la portata complessiva. Seleziona **[!UICONTROL Bilanciato]** per una via di mezzo tra somiglianza con il pubblico di partenza e la portata complessiva.

![Il campo Raggiungimento pubblico nella finestra di dialogo Genera espansione pubblico con l&#39;opzione Bilanciato selezionata e il testo della descrizione sottostante.](/help/assets/collaborate/expand/select-audience-reach.png){zoomable="yes"}

### Includere o escludere il pubblico seed {#include-exclude-seed-audience}

Utilizza i pulsanti di scelta **[!UICONTROL Pubblico seed]** per scegliere se il pubblico seed originale deve essere incluso o escluso dal pubblico di espansione finale.

![Il campo Membri del pubblico seed nella finestra di dialogo Genera espansione pubblico con i pulsanti di scelta Sì e No.](/help/assets/collaborate/expand/include-exclude-seed-audience.png){zoomable="yes"}

### Generare il pubblico di espansione {#generate-expansion-audience}

Una volta completati tutti i campi, selezionare **[!UICONTROL Genera pubblico di espansione]**. Un messaggio di conferma conferma conferma che Collaboration sta creando il pubblico di espansione e che puoi tracciarne l&#39;avanzamento nella pagina **[!UICONTROL Espandi]**.

## Rivedere e inviare un pubblico di espansione {#review-send-expansion-audience}

Quando lo stato di un pubblico di espansione diventa **[!UICONTROL Bozza]**, selezionane il nome dalla tabella **[!UICONTROL Tipi di pubblico di espansione]** per aprirlo.

![Pubblico di espansione Una pagina di dettaglio che mostra i metadati del pubblico, le dimensioni del modello, le dimensioni del pubblico di seed e il pulsante Invia.](/help/assets/collaborate/expand/expansion-audience-detail.png){zoomable="yes"}

Da questa vista puoi effettuare le seguenti operazioni:

* Modificare il nome del pubblico di espansione
* Visualizzare la data e l’ora di creazione
* Confrontare la dimensione del pubblico di seed con la dimensione del pubblico di espansione generato
* Rivedi la chiave di corrispondenza utilizzata per generare il pubblico

Quando sei pronto, seleziona **[!UICONTROL Invia al partner]** per inviare il pubblico di espansione al tuo collaboratore. Il pubblico rimane nello stato **[!UICONTROL Bozza]** finché non lo invii, quindi si aggiorna a **[!UICONTROL Attivo]**.

>[!NOTE]
>
>Se il tuo collaboratore non ha una destinazione configurata, **[!UICONTROL Invia al partner]** non è disponibile. Un messaggio spiega che il tuo collaboratore deve prima impostare una destinazione.

>[!IMPORTANT]
>
>Un pubblico di espansione scade 7 giorni dopo la sua generazione se non viene inviato al tuo collaboratore.

## Ricevere e attivare un pubblico di espansione {#receive-activate-expansion-audience}

Quando invii un pubblico di espansione, Collaboration lo consegna al tuo collaboratore in base all’impostazione di attivazione configurata per la connessione:

* Se è abilitata l&#39;attivazione automatica **1&rbrace;, Collaboration attiva automaticamente il pubblico di espansione nella destinazione configurata del collaboratore e lo visualizza nella relativa [scheda Attiva](./activate.md#activated-audiences).**
<!-- Beta release: automatic activation is the only available activation setting. Uncomment the manual activation guidance below when manual activation is introduced with the GA release. -->
<!-- * If **manual activation** is enabled, the expansion audience appears in your collaborator's [Received audiences](./activate.md#received-audiences) section of the **[!UICONTROL Activate]** tab, and your collaborator must manually activate it. -->

## Passaggi successivi

Dopo aver inviato il pubblico di espansione, utilizza la [scheda Discover](./discover.md) per confrontarla con altri tipi di pubblico oppure la [scheda Activate](./activate.md) per tracciarne l&#39;attivazione.
