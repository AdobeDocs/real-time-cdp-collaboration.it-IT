---
title: Measure performance
description: Measure the performance of your campaigns across different channels. Learn how to use and interpret various reports.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
TQID: https://experienceleague.adobe.com/pr-qF4sd-NHd55kxh1dCstHRnVCUEhIvtv-47-ljiu4
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2: id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 2612
ht-degree: 5%

---

# Measure performance

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L&#39;area di lavoro **[!UICONTROL Measure]** è disponibile solo se il caso di utilizzo **Measurement** è stato abilitato [durante il processo di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, consulta la guida [gestisci progetti](./manage-projects.md#project-use-cases).

Learn about the available reports in Adobe Real-Time CDP Collaboration and understand how to measure and analyze the performance of your marketing campaigns across various channels.

## Prerequisiti {#prerequisites}

Before you can access the measurement reports in Collaboration, you must:

* [Connect](/help/guide/connect/establishing-connections.md) with a collaborator with the **Measurement** use case enabled
* Collaborate on at least one project with your collaborator. Scopri come [creare un progetto](/help/guide/collaborate/manage-projects.md#create-project).
* Esegui la campagna e assicurati che sia fornito l&#39;ID [campagna per la campagna](../collaborate/manage-projects.md#manage-campaign-id):
   * Se sei un editore, inserisci l’ID campagna collegato alla campagna dell’inserzionista.
   * If you are an advertiser, request that your collaborator (publisher) provide the Campaign ID. Questa operazione è necessaria per [generare report nell&#39;area di lavoro di misura](#create-measurement-report).
* [Upload measurement data](/help/guide/setup/onboard-measurement-data.md) into Collaboration if you want to [create Attribution reports](#create-attribution-report).

## Visualizzazione dei rapporti {#view-reports}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report_campaignID"
>title="ID campagna"
>abstract="Segnaposto per aggiungere informazioni rilevanti nell’interfaccia utente su cosa sono gli ID campagna."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report"
>title="ID campagna"
>abstract="Segnaposto per aggiungere informazioni rilevanti nell’interfaccia utente su cosa sono gli ID campagna."

To view the reports available in the measurement tab:

1. Navigate to **[!UICONTROL Collaborate]** > **[!UICONTROL My projects]**.
2. Per il progetto desiderato e selezionare **[!UICONTROL Visualizza]**.
3. Nel progetto, seleziona la scheda **[!UICONTROL Misura]**.

Seleziona **[!UICONTROL Visualizza report completo]** per accedere ai vari report disponibili, descritti più avanti.

![Come accedere alla scheda di misurazione in un progetto.](/help/assets/collaborate/measure/measurement.gif)

### Visualizzazione Riepilogo

La vista dall’alto della pagina nella scheda di misurazione mostra un riepilogo della campagna con alcuni numeri di alto livello a cui puoi fare riferimento:

**[!UICONTROL Impression]**: il numero totale di volte in cui è stata visualizzata la creatività.
**[!UICONTROL Raggiungimento univoco]**: numero di singole identità che hanno visualizzato il contenuto creativo.
**[!UICONTROL Frequenza media totale]**: numero di impression diviso per identità univoche raggiunto. Questa figura indica quanto spesso ogni identità è stata visualizzata nella creatività.

![Visualizzazione riepilogo campagna](/help/assets/collaborate/measure/campaign-summary.png)

### Metriche nel tempo {#metrics-over-time}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measure_metricsovertime"
>title="Metriche nel tempo"
>abstract="Utilizza la vista delle metriche nel tempo per comprendere il numero totale di impression visualizzate per la creatività durante il periodo della campagna. Puoi selezionare un massimo di due dimensioni da visualizzare nel rapporto."

Utilizza la vista delle metriche nel tempo per comprendere il numero totale di impression visualizzate per la creatività durante il periodo della campagna. Puoi selezionare un massimo di due metriche da visualizzare e analizzare nel rapporto.

![Visualizzazione metriche nel tempo.](/help/assets/collaborate/measure/metrics-over-time.png)

### Distribuzione frequenza {#frequency-distribution}

Utilizza la vista di distribuzione della frequenza per comprendere il raggruppamento del numero di impression mostrate a ogni utente univoco. Questa vista può aiutarti nelle campagne future a decidere da quale punto iniziare a eliminare i tipi di pubblico. Ad esempio, potrebbe essere utile eliminare i profili che hanno già visto un contenuto creativo tre volte.

![Visualizzazione distribuzione frequenza.](/help/assets/collaborate/measure/frequency-distribution.gif)

### Metrica per dimensione {#metric-by-dimension}

Analizza metriche diverse come impression, impression visualizzabili, portata unica, costo e altro nel contesto del mezzo di posizionamento. Analizza quale mezzo (ad esempio streaming mobile, CTV programmatico o altri) produce i risultati migliori per le tue campagne.

![Metrica per dimensione.](/help/assets/collaborate/measure/metric-by-dimension.png)

### Curva di portata cumulativa {#cumulative-reach-curve}

Con l’avanzare della campagna e l’aumentare del numero di impression, verifica se è aumentato anche il numero di utenti che sei riuscito a raggiungere. Un pattern comune nelle campagne è che dopo un certo punto viene raggiunto un plateau in cui il contenuto creativo viene mostrato più e più volte alle stesse persone. Questa visualizzazione può aiutarti a regolare la lunghezza delle campagne future, a seconda del momento in cui le nuove persone non venivano più raggiunte.

![Curva di portata cumulativa.](/help/assets/collaborate/measure/cumulative-reach-curve.png)

### Impression per posizionamento {#impressions-by-placement}

Scopri quale mezzo sta guidando le impression per la tua creatività. Questo può aiutarti a decidere dove investire la spesa pubblicitaria nelle campagne future.

![Impression per posizionamento.](/help/assets/collaborate/measure/impressions-by-placement.png)

### Conversioni cumulative {#cumulative-conversions}

Questa vista fornisce una suddivisione dettagliata degli eventi di conversione che scegli di misurare in formato tabulare. La tabella include:

* **Evento di conversione**: nome di ogni evento di conversione che si sta monitorando.
* **Conteggio conversioni**: conteggio totale delle conversioni verificatesi per ogni evento.
* **Entrate stimate**: valore stimato attribuito a ciascun evento di conversione.

Consulta questa tabella per valutare l’efficacia della campagna nel condurre le azioni desiderate.

![Conversioni cumulative.](/help/assets/collaborate/measure/cumulative-conversions.png)

### Conversioni per giorno {#conversions-by-day}

Questo grafico fornisce un raggruppamento giornaliero delle conversioni per ogni evento impostato durante la creazione di un rapporto di attribuzione. Utilizza questa visualizzazione per scoprire i pattern giornalieri, identificare i periodi di attività di conversione alta o bassa e confrontare il modo in cui diversi eventi di conversione vengono eseguiti nella timeline della campagna.

![Conversioni per giorno.](/help/assets/collaborate/measure/conversions-by-day.gif)

## Crea un rapporto di misurazione {#create-measurement-report}

In Collaboration è possibile creare due tipi principali di rapporti di misurazione:

* **Riepilogo campagna**: fornisce metriche di alto livello come portata, impression, frequenza media e consegna per canale, fornendo una rapida panoramica delle prestazioni complessive della campagna.
* **Attribuzione**: misura il modo in cui le esposizioni alle campagne guidano azioni a valle come conversioni o acquisti, aiutandoti a comprendere l&#39;efficacia della campagna.

Puoi eseguire il rapporto di riepilogo delle campagne da solo, mentre il rapporto di attribuzione richiede che entrambi i tipi di rapporto siano selezionati insieme.

### Creare un rapporto di riepilogo della campagna {#create-campaign-summary-report}

Sia gli editori che gli inserzionisti possono generare **report di riepilogo campagne** per valutare le prestazioni della campagna. Utilizza questi report per ottenere informazioni sulle metriche chiave come [reach](#cumulative-reach-curve), [frequency](#frequency-distribution) e [impression](#impressions-by-placement) e capire come è stata distribuita la tua campagna e il suo impatto complessivo.

Per generare un report **Riepilogo campagna**, passare all&#39;area di lavoro del progetto dall&#39;area di lavoro **[!UICONTROL Collaborator]**. Dalla scheda **[!UICONTROL Misura]**, seleziona l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) e quindi selezionare **[!UICONTROL Misura]**.

Se si tratta del primo report, è possibile selezionare anche l&#39;opzione **[!UICONTROL Esegui report]**.

![La scheda Misura evidenzia le opzioni Esegui report e Misura.](/help/assets/collaborate/measure/run-measure-report.png)

Viene visualizzata la schermata **[!UICONTROL Crea report di misurazione]** con informazioni e campi di input raggruppati in **[!UICONTROL Dettagli fatturazione]**, **[!UICONTROL Dettagli campagna]** e **[!UICONTROL Dettagli report]**.

#### Dettagli fatturazione {#billing-details}

Questa sezione spiega come vengono utilizzati i crediti durante la generazione dei rapporti di misurazione. La responsabilità del credito è stata stabilita durante [l&#39;impostazione della connessione](../connect/establishing-connections.md#credit-split). Prima di eseguire qualsiasi rapporto, assicurati di rivedere e confermare le impostazioni di suddivisione del credito e i ruoli di reporting con il tuo collaboratore.

#### Dettagli della campagna {#campaign-details}

Nella sezione **[!UICONTROL Dettagli campagna]**, seleziona il **ID inserzionista** appropriato da associare al report. I nomi o gli ID degli inserzionisti sono stati aggiunti durante la [configurazione della connessione](../connect/establishing-connections.md#advertiser-names). Se è stato configurato un solo nome, questo viene visualizzato per impostazione predefinita. Se non è stato impostato alcun nome, il campo **[!UICONTROL ID inserzionista (nome)]** è disabilitato e precompilato con il nome dell&#39;account dell&#39;inserzionista.

![La schermata Crea report di misurazione mostra l&#39;opzione ID inserzionista (nome) disabilitata.](/help/assets/collaborate/measure/advertiser-id.png)

Quindi, seleziona la campagna desiderata dal menu a discesa **[!UICONTROL ID campagna]**. Questo menu elenca tutti gli ID campagna immessi dall’editore per il progetto. Se la campagna necessaria non è disponibile, [aggiungerla nell&#39;interfaccia utente](./manage-projects.md#manage-campaign-id) prima di generare il report.

![La schermata Crea report di misurazione mostra il menu a discesa ID campagna espanso.](/help/assets/collaborate/measure/campaign-id.png)

Quindi, specifica il periodo che desideri che venga coperto dal rapporto. Seleziona **[!UICONTROL Intervallo date report]**, quindi utilizza il calendario per scegliere le date di inizio e di fine.

![La schermata Crea report di misurazione mostra il calendario dell&#39;intervallo di date del report.](/help/assets/collaborate/measure/report-date-range.png)

#### Dettagli rapporto {#report-details}

**Data di esecuzione report**

Nella sezione **[!UICONTROL Dettagli report]**, scegliere la data in cui deve essere eseguito il report. Seleziona **[!UICONTROL Data di esecuzione report]** e scegli la data preferita dal calendario.

* Se scegli la data odierna o una data passata, il rapporto **Riepilogo campagna** viene eseguito immediatamente.
* Se si sceglie una data futura, il report **Riepilogo campagna** verrà eseguito in tale giorno.

![La schermata Crea report di misurazione mostra il calendario della data di esecuzione del report.](/help/assets/collaborate/measure/report-run-date.png)

**Tipo di report**

* Se sei un inserzionista, puoi selezionare il tipo di rapporto **[!UICONTROL Riepilogo campagna]** tra le opzioni disponibili. Solo gli inserzionisti possono generare rapporti di attribuzione.
* Se sei un editore, il tipo di report **[!UICONTROL Riepilogo campagna]** è preselezionato e non può essere modificato. Al momento, gli editori non possono eseguire rapporti di attribuzione.

![La schermata Crea report di misurazione mostra l&#39;opzione di riepilogo della campagna come tipo di report preselezionato e non modificabile.](/help/assets/collaborate/measure/cs-report-type.png)

Infine, controlla le impostazioni e seleziona **[!UICONTROL Crea]**. Il rapporto di riepilogo della campagna viene generato immediatamente se la data di esecuzione è oggi o prima o nella data futura selezionata. Puoi modificare il rapporto pianificato prima della sua data di esecuzione. Per istruzioni dettagliate, consulta la sezione [Modifica report di misurazione].

Una volta disponibile, puoi visualizzare il report in qualsiasi momento nella scheda **[!UICONTROL Misura]** nell&#39;area di lavoro del progetto.

![Nella schermata Crea report di misurazione sono evidenziate le informazioni e l&#39;opzione Crea.](/help/assets/collaborate/measure/cs-review.png)

### Creare un rapporto di attribuzione {#create-attribution-report}

In qualità di inserzionista, puoi generare rapporti di **attribuzione** per valutare in che modo le esposizioni della tua campagna contribuiscono a risultati chiave come abbonamenti o acquisti. Utilizza questi rapporti per comprendere le interazioni degli utenti con la campagna, identificare i punti di contatto che producono il maggiore impatto e informare strategie di marketing più efficaci.

>[!IMPORTANT]
>
> Prima di generare i rapporti di attribuzione, devi [creare l&#39;origine dei dati di misurazione](../setup/onboard-measurement-data.md#add-measurement-data) in Collaboration.
>![Scheda Misura con i requisiti per i dati di misurazione e l&#39;opzione di misura disabilitata.](/help/assets/collaborate/measure/require-measurement-data.png)

Per generare un report **Attribuzione**, passare all&#39;area di lavoro del progetto dall&#39;area di lavoro **[!UICONTROL Collaborator]**. Dalla scheda **[!UICONTROL Misura]**, seleziona l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) e quindi selezionare **[!UICONTROL Misura]**.

Se si tratta del primo report, è possibile selezionare anche l&#39;opzione **[!UICONTROL Esegui report]**.

![La scheda Misura evidenzia le opzioni Esegui report e Misura.](/help/assets/collaborate/measure/run-measure-report-attribution.png)

Viene visualizzata la schermata **[!UICONTROL Crea report di misurazione]** con informazioni e campi di input raggruppati in **[!UICONTROL Dettagli fatturazione]**, **[!UICONTROL Dettagli campagna]** e **[!UICONTROL Dettagli report]**.

Leggi e segui i passaggi descritti nella sezione [Creare un rapporto di riepilogo della campagna](#create-campaign-summary-report) per configurare le seguenti impostazioni:

* [Dettagli fatturazione](#billing-details)
* [Dettagli della campagna](#campaign-details)

#### Dettagli del rapporto per i rapporti di attribuzione {#report-details-attribution}

**Data di esecuzione report**

>[!IMPORTANT]
>
> Per i rapporti di attribuzione, la data di esecuzione del rapporto deve essere una data futura e deve essere successiva di almeno un giorno alla data di fine dell’intervallo di date del rapporto più l’intera durata dell’intervallo di lookback definito.
> **Data di esecuzione report ≥ data di fine report + intervallo di lookback + 1**
> 
> Ad esempio, se l’intervallo di date del rapporto termina il 15 giugno e l’intervallo di lookback è di 14 giorni, la data di esecuzione del rapporto è il 30 giugno o successiva.

Nella sezione **[!UICONTROL Dettagli report]**, scegliere la data in cui deve essere eseguito il report. Seleziona **[!UICONTROL Data di esecuzione report]** e scegli la data preferita dal calendario.

**Tipo di report**

In qualità di inserzionista, puoi selezionare **[!UICONTROL Attribuzione]** come tipo di report oltre a **[!UICONTROL Riepilogo campagna]**. Quando scegli il rapporto Attribuzione, i risultati includono sia metriche di riepilogo delle campagne standard che analisi di attribuzione dettagliate, che forniscono una panoramica completa delle prestazioni della campagna.

![Nella schermata Crea report di misurazione sono evidenziati sia il riepilogo della campagna che i tipi di report di attribuzione selezionati.](/help/assets/collaborate/measure/attribution-report-type.png)

Quando selezioni **[!UICONTROL Attribuzione]** come tipo di report, viene visualizzata una sezione di configurazione **[!UICONTROL Attribuzione]** con le impostazioni aggiuntive richieste:

* **Intervallo di lookback tra giorni**: definisce il periodo di tempo trascorso il quale il rapporto considera le impression della campagna prima di ogni conversione. Solo le impression all’interno di questo periodo sono idonee per il credito di attribuzione.
* **Eventi di conversione**: specifica le azioni di conversione da misurare, ad esempio acquisti o iscrizioni. Questi eventi devono essere impostati in anticipo quando [inserisci i dati di misurazione](../setup/onboard-measurement-data.md#add-conversion-event) in Collaboration.

Immettere innanzitutto un valore per il campo **[!UICONTROL Intervallo di lookback in giorni]** oppure regolarlo con le opzioni di incremento/decremento.

![La schermata Crea report di misurazione evidenzia il valore dell&#39;intervallo di lookback in giorni.](/help/assets/collaborate/measure/lookback-window-in-days.png)

Quindi, scegli fino a **3** eventi di conversione dall&#39;elenco disponibile. Per ulteriori informazioni su un evento specifico, selezionare l&#39;icona **[!UICONTROL i]** per visualizzarne i dettagli.

![La schermata Crea report di misurazione evidenzia gli eventi di conversione selezionati e le informazioni dell&#39;evento di acquisto.](/help/assets/collaborate/measure/attribution-conversion-events.png)

Infine, controlla le impostazioni e seleziona **[!UICONTROL Crea]** per pianificare il rapporto. Il rapporto di attribuzione verrà generato alla data di esecuzione specificata. Puoi modificare il rapporto pianificato prima della sua data di esecuzione. Per istruzioni dettagliate, consulta la sezione [Modifica report di misurazione].

Una volta disponibile, puoi visualizzare il report in qualsiasi momento nella scheda **[!UICONTROL Misura]** nell&#39;area di lavoro del progetto.

![Nella schermata Crea report di misurazione sono evidenziate le informazioni e l&#39;opzione Crea.](/help/assets/collaborate/measure/attribution-review.png)

## Modifica rapporto di misurazione {#edit-measurement-report}

>[!IMPORTANT]
>
>È possibile modificare le impostazioni di un rapporto di misurazione solo se è pianificata l&#39;esecuzione futura. Per i rapporti già eseguiti, le impostazioni non possono essere modificate.

Aggiorna le impostazioni di un rapporto di misurazione per garantire che fornisca l’analisi corretta della campagna in un periodo specifico ed esegua in una data desiderata.

Per iniziare, passare all&#39;area di lavoro del rapporto di misurazione che si desidera aggiornare. Selezionare l&#39;icona Modifica (![icona Modifica](/help/assets/icons/edit.png)) accanto all&#39;icona Elimina.

![Area di lavoro report di misurazione con l&#39;icona Modifica evidenziata.](/help/assets/collaborate/measure/edit-report.png)

>[!TIP]
>
>Nella scheda **[!UICONTROL Misura]**, passa alla sezione del report che desideri modificare. Seleziona l&#39;icona Modifica (![icona Modifica](/help/assets/icons/edit.png)) accanto a **[!UICONTROL Visualizza report completo]** per aggiornarne le impostazioni.
>![Scheda Misura che evidenzia l&#39;icona Modifica all&#39;interno di una sezione di report.](/help/assets/collaborate/measure/measure-tab-edit-report.png)

La finestra di dialogo **[!UICONTROL Modifica report di misurazione]** viene visualizzata con le impostazioni correnti del report nelle sezioni seguenti:

* [**Dettagli fatturazione**](#billing-details): visualizza informazioni sui crediti durante l&#39;esecuzione dei report di misurazione. Non è richiesta alcuna configurazione.
* [**Dettagli campagna**](#campaign-details): visualizza le impostazioni per l&#39;inserzionista, l&#39;ID campagna, il periodo di reporting e un nome di report intuitivo.
* [**Dettagli report**](#report-details): visualizza le impostazioni per il tipo di report, la data di esecuzione del report e le opzioni di configurazione specifiche per i report di attribuzione.

![La finestra di dialogo Modifica report di misurazione mostra le impostazioni correnti nelle sezioni Dettagli fatturazione, Dettagli campagna e Dettagli report.](/help/assets/collaborate/measure/edit-measurement-report-dialog.png)

### Modifica dettagli campagna {#edit-campaign-details}

Nella finestra di dialogo **[!UICONTROL Modifica report di misurazione]**, utilizza i menu a discesa **[!UICONTROL ID inserzionista (nome)]** e **[!UICONTROL ID campagna]** per modificare l&#39;inserzionista e l&#39;ID campagna per il report.

![Viene aperta la finestra di dialogo Modifica report di misurazione che evidenzia il menu a discesa ID campagna.](/help/assets/collaborate/measure/edit-campaign-id.png)

Quindi, selezionare **[!UICONTROL Intervallo date report]** e utilizzare il calendario per modificare le date di inizio e di fine del report.

![Viene aperta la finestra di dialogo Modifica report di misurazione che evidenzia il calendario dell&#39;intervallo di date del report.](/help/assets/collaborate/measure/edit-report-date-range.png)

Inserisci un nome di rapporto descrittivo aggiornato per acquisire le modifiche recenti. Questo ti aiuta a riconoscere e trovare questo rapporto in futuro.

![La finestra di dialogo Modifica report di misurazione evidenzia il nome del report descrittivo aggiornato.](/help/assets/collaborate/measure/edit-friendly-report-name.png)

### Modifica dettagli report {#edit-report-details}

Per pianificare il report per una data diversa, passare alla sezione **[!UICONTROL Dettagli report]**. Selezionare l&#39;opzione della data di esecuzione corrente, quindi utilizzare il calendario per scegliere la data desiderata.

![La finestra di dialogo Modifica report di misurazione evidenzia il calendario della data di esecuzione del report.](/help/assets/collaborate/measure/edit-report-run-date.png)

In qualità di inserzionista, puoi selezionare o rimuovere il tipo di report **[!UICONTROL Attribuzione]** oltre a **[!UICONTROL Riepilogo campagna]**. Se scegli **[!UICONTROL Attribuzione]**, il rapporto di attribuzione include sia le metriche di riepilogo delle campagne standard che approfondimenti attribuzione. Per ulteriori informazioni sui tipi di report **Riepilogo campagna** e **Attribuzione**, consulta la sezione [Crea report di misurazione](#create-measurement-report).

>[!IMPORTANT]
>
>Se sei un **editore**, il tipo di report predefinito è **[!UICONTROL Riepilogo campagna]** e non può essere modificato in questo momento.

* Se scegli **[!UICONTROL Attribuzione]** come tipo di report, devi compilare i campi obbligatori nella sezione **[!UICONTROL Attribuzione]**. Per istruzioni di configurazione, consulta la sezione [Dettagli del rapporto di attribuzione](#report-details-attribution).
* Se in precedenza hai configurato le impostazioni di attribuzione durante la creazione del rapporto, puoi scegliere di modificare l’intervallo di lookback (misurato in giorni) e selezionare gli eventi di conversione su cui generare il rapporto.

Per aggiornare **[!UICONTROL Intervallo di lookback in giorni]**, immettere un valore numerico o regolarlo con le opzioni di incremento/decremento. Quindi, seleziona gli eventi di conversione su cui desideri generare il rapporto. È possibile scegliere fino a **3** conversioni dall&#39;elenco disponibile.

![La finestra di dialogo Modifica report di misurazione evidenzia gli eventi di conversione aggiornati.](/help/assets/collaborate/measure/edit-conversion-events.png)

Al termine, controlla gli aggiornamenti e seleziona **[!UICONTROL Modifica]** per applicare le modifiche.

![Finestra di dialogo Modifica report di misurazione con l&#39;opzione Modifica evidenziata.](/help/assets/collaborate/measure/edit-report-confirm.png)

Una finestra di dialogo di conferma conferma conferma che il report è stato salvato correttamente.

## Elimina report di misurazione {#delete-measurement-report}

Se si elimina un rapporto di misurazione in Collaboration, questo viene rimosso definitivamente dal sistema. Questa azione non può essere annullata. A questo scopo, seleziona il report da eliminare nella scheda **[!UICONTROL Misura]**.

Nell&#39;area di lavoro report di misurazione, selezionare l&#39;icona Elimina (![icona Elimina](/help/assets/common/delete.svg)).

![Area di lavoro report di misurazione con l&#39;icona Elimina evidenziata.](/help/assets/collaborate/measure/delete-report.png)

Viene visualizzata la finestra di dialogo **[!UICONTROL Elimina report]** in cui viene richiesto di confermare l&#39;eliminazione. Seleziona **[!UICONTROL Elimina]**.

![Finestra di dialogo Elimina report con l&#39;opzione Elimina evidenziata.](/help/assets/collaborate/measure/delete-report-confirm.png)

Una finestra di dialogo di conferma conferma conferma che il report è stato eliminato correttamente.
