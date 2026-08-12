---
title: Creare rapporti di misurazione di Amazon Marketing Cloud
description: Scopri come creare e interpretare i rapporti di misurazione per le campagne Amazon Marketing Cloud in Real-Time CDP Collaboration.
audience: advertiser
keywords: AMC, Amazon Marketing Cloud, rapporti di misurazione, riepilogo della campagna, attribuzione, Real-Time CDP Collaboration
solution: Real-Time Customer Data Platform Collaboration
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 944914557c10b43abbe4915e061c219aca9f783f
workflow-type: tm+mt
source-wordcount: '1574'
ht-degree: 5%

---


# Crea [!DNL Amazon Marketing Cloud] report di misurazione {#amc-measurement-reports}

{{limited-availability-release-note}}

Utilizza la scheda **[!UICONTROL Misura]** in un progetto [!DNL Amazon Marketing Cloud] ([!DNL AMC]) per rivedere i risultati di portata, frequenza e conversione del pubblico. Dopo aver creato un progetto AMC, creare rapporti di misurazione per le campagne già eseguite utilizzando i dati disponibili nell&#39;istanza [!DNL AMC].

>[!IMPORTANT]
>
>Nella scheda **[!UICONTROL Misura]** viene visualizzato &quot;Nessun dato di misurazione disponibile&quot; fino al completamento delle query di impostazione dei dati in background. Questo processo può richiedere fino a 24 ore. Se il messaggio persiste dopo 24 ore, consulta la sezione [Risoluzione dei problemi](#troubleshooting).


## Creare un rapporto {#create-report}

Per creare un report di misurazione [!DNL AMC], seguire i passaggi descritti in [Crea report di riepilogo campagne](../measure.md#create-campaign-summary-report-create-campaign-summary-report).

![Modulo del report di misurazione che mostra i campi ID inserzionista, ID campagna, intervallo di date del report, data di esecuzione del report, nome del report e tipo di report.](../../../assets/collaborate/advertising-platforms/create-measurement-report.png){zoomable="yes"}

### Dettagli della campagna {#campaign}

L&#39;**[!UICONTROL ID inserzionista]** identifica l&#39;account [!DNL Amazon Advertising] associato all&#39;istanza [!DNL AMC]. [!DNL AMC] utilizza questo contesto dell&#39;account per recuperare le campagne per la misurazione.

L&#39;elenco **[!UICONTROL ID campagna]** viene popolato automaticamente con le campagne disponibili nell&#39;istanza [!DNL AMC] connessa. Una campagna viene visualizzata solo se rientra nell&#39;intervallo di lookback di individuazione predefinito e dispone di un numero sufficiente di utenti univoci per soddisfare la soglia minima di aggregazione di [!DNL AMC]. Selezionare la campagna di cui si desidera misurare l&#39;attività [!DNL Amazon Ads].

Se la campagna necessaria non è elencata, verificare che appartenga all&#39;account [!DNL Amazon Ads] connesso e rivedere [Risoluzione dei problemi](#troubleshooting). Per ulteriori informazioni sulla soglia, consulta la [documentazione sulla soglia di aggregazione AMC](https://advertising.amazon.com/API/docs/en-us/guides/amazon-marketing-cloud/aggregation-threshold).

#### Intervallo di date, data di esecuzione e nome del rapporto {#dates}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_report_date_range"
>title="Intervallo di date"
>abstract="Imposta le date di inizio e di fine per i dati della campagna da includere nel rapporto. L’intervallo di date è limitato a un intervallo di lookback di 365 giorni con un massimo di 90 giorni. Puoi creare rapporti solo sulle campagne passate."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_report_run_date"
>title="Data di esecuzione"
>abstract="Data in cui viene eseguito il report. Deve essere almeno un giorno dopo la data di fine del rapporto e può essere fino a 46 giorni in futuro."

>[!NOTE]
>
>Puoi generare rapporti solo sulle campagne già eseguite.

Imposta l&#39;**[!UICONTROL intervallo di date del report]** sul periodo in cui è stata eseguita la campagna [!DNL AMC] selezionata. [!DNL AMC] supporta un intervallo di lookback di 365 giorni con un massimo di 90 giorni.

Imposta la **[!UICONTROL data di esecuzione report]**. Questa è la data in cui viene eseguito il rapporto. La data di esecuzione deve essere successiva di almeno un giorno alla data di fine del rapporto e può essere successiva di un massimo di 46 giorni. Per il set completo di vincoli di data, vedere [Riferimento vincoli AMC](#constraints).

>[!TIP]
>
>Per i rapporti di attribuzione in cui l’intervallo di date rientra nei 30 giorni successivi alla data corrente, imposta la data di esecuzione su 30 giorni in modo che tutte le conversioni all’interno dell’intervallo di lookback fisso di 30 giorni siano state acquisite prima dell’esecuzione del rapporto.

#### Tipo di rapporto {#report-type}

Tutti i [!DNL AMC] report includono un **[!UICONTROL riepilogo campagna]**. Facoltativamente, puoi includere i dati di **[!UICONTROL attribuzione]** per misurare se le impression della campagna hanno portato ad azioni da parte del cliente, come acquisti o iscrizioni, entro una finestra di 30 giorni dopo l&#39;esposizione dell&#39;annuncio. L&#39;attribuzione richiede che gli eventi di conversione pertinenti siano disponibili nell&#39;istanza [!DNL AMC]. Per le campagne incentrate sulla portata o sulla consapevolezza, il **[!UICONTROL riepilogo campagne]** fornisce le metriche di consegna necessarie.

| Tipo di rapporto | Descrizione |
| --- | --- |
| **[!UICONTROL Riepilogo campagna]** | Fornisce la portata, la frequenza e le metriche di impression per la campagna selezionata. Sempre incluso. |
| **[!UICONTROL Attribuzione]** | Aggiunge i dati di conversione al rapporto. Disponibile solo se nell&#39;istanza [!DNL AMC] sono presenti eventi di conversione. Vedi [Eventi di conversione](#conversion-events). |

#### Eventi di conversione (solo attribuzione) {#conversion-events}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_attribution_lookback_period"
>title="Periodo di lookback dell’attribuzione"
>abstract="AMC applica un intervallo di attribuzione fisso di 30 giorni: le conversioni che si verificano fino a 30 giorni dopo l’ultima impression possono essere attribuite alle impression comprese nell’intervallo di date del rapporto. Non è possibile modificare questo valore; pianifica la data di esecuzione del rapporto almeno 30 giorni successivi alla fine dell’intervallo per garantire che tutte le conversioni idonee vengano acquisite."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_conversion_events"
>title="Eventi di conversione"
>abstract="Seleziona fino a tre eventi di conversione da includere nel rapporto di attribuzione. Gli eventi disponibili vengono rilevati automaticamente dall&#39;istanza [!DNL AMC]. Se non viene visualizzato alcun evento, è possibile che nell&#39;istanza [!DNL AMC] non siano presenti eventi di conversione registrati e che l&#39;attribuzione non sia disponibile."

>[!NOTE]
>
>I dati di attribuzione richiedono la configurazione degli eventi di conversione nell&#39;istanza [!DNL AMC]. Se [!UICONTROL Attribuzione] non è disponibile o non è stato selezionato, ignorare questa sezione e selezionare **[!UICONTROL Crea]** per inviare il modulo.

Per i report [!UICONTROL Attribution], [!DNL AMC] applica un intervallo di lookback di attribuzione fisso di 30 giorni. Questa impostazione non può essere regolata.

![La sezione Eventi di conversione della maschera del report di misurazione nello stato attivo, che mostra il campo dell&#39;intervallo di lookback impostato su 30 giorni e l&#39;elenco a selezione multipla degli eventi di conversione con gli eventi disponibili.](../../../assets/collaborate/advertising-platforms/conversion-events-active.png){zoomable="yes"}

Gli eventi di conversione rappresentano le azioni dei clienti nel sito monitorate da [!DNL Amazon Ads], ad esempio un acquisto, un&#39;aggiunta alla lista dei desideri, un&#39;azione del carrello o una visualizzazione dei dettagli del prodotto. I rapporti di attribuzione supportano fino a tre eventi. Seleziona gli eventi che sono in linea con i risultati della campagna che desideri misurare. Se l&#39;opzione [!UICONTROL Attribuzione] non è disponibile, vedere [Risoluzione dei problemi](#troubleshooting).

Dopo aver creato il report, questo viene visualizzato nella scheda **[!UICONTROL Misura]** con uno stato pianificato o in sospeso. Alla data di esecuzione configurata, [!DNL AMC] elabora la query del report e restituisce i risultati entro 24 ore.

![La scheda Misura mostra una nuova scheda del report di misurazione creata con un indicatore di stato pianificato, il nome del report, la data di esecuzione e il tipo di report visibili.](../../../assets/collaborate/advertising-platforms/measurement-report-pending.png){zoomable="yes"}


## Visualizzare un rapporto {#view-report}

Una volta eseguito un report, i risultati saranno disponibili nella scheda **[!UICONTROL Misura]** del progetto [!DNL AMC]. Individua il report e seleziona **[!UICONTROL Visualizza report completo]** per esaminare i risultati.

![Scheda Misura in un progetto [!DNL AMC] che mostra una scheda del report completata con data di esecuzione, tipo di report e pulsante Visualizza report completo evidenziati.](../../../assets/collaborate/advertising-platforms/view-full-report.png){zoomable="yes"}

Nel rapporto vengono visualizzati i risultati disponibili per il tipo di rapporto selezionato. I report **[!UICONTROL Riepilogo campagna]** mostrano i risultati di consegna per la campagna Amazon selezionata.

![Le visualizzazioni Riepilogo campagna mostrano i totali di riepilogo, la distribuzione delle impression, la distribuzione della frequenza, la curva di portata e le impression in base al posizionamento.](../../../assets/collaborate/advertising-platforms/campaign-summary-widgets.png){zoomable="yes"}

I rapporti che includono **[!UICONTROL Attribuzione]** mostrano anche l&#39;attività di conversione associata agli eventi di conversione di Amazon Ads selezionati.


![Le visualizzazioni Attribuzione che mostrano i grafici Conversioni cumulative e Conversioni per giorno.](../../../assets/collaborate/advertising-platforms/attribution-report-conversion-widgets.png){zoomable="yes"}

Per ulteriori informazioni sull&#39;interpretazione dei risultati del report, vedere [Misurare le prestazioni](../measure.md#view-reports-view-reports).

## Riferimento vincoli [!DNL AMC] {#constraints}

I seguenti vincoli si applicano a tutti i report di misurazione [!DNL AMC].

| Vincolo | Elemento “value” |
| --- | --- |
| Inizio primo intervallo di date del rapporto | 365 giorni prima della data corrente |
| Fine ultimo intervallo di date del rapporto | 45 giorni dopo la data corrente. Utilizza questa opzione per preconfigurare un rapporto per una campagna ancora in esecuzione che si concluderà entro i prossimi 45 giorni; il rapporto viene eseguito automaticamente alla data di esecuzione pianificata dopo la fine della campagna. |
| Intervallo date massimo per il rapporto | 90 giorni |
| Intervallo di lookback dell’attribuzione | 30 giorni (fisso per [!DNL AMC]) |
| Data esecuzione minima | Almeno 1 giorno dopo la data di fine del rapporto |
| Data di esecuzione massima | 46 giorni nel futuro |
| Numero massimo di eventi di conversione per report | 3 |
| Selezione campagna | Campagna singola per rapporto |
| Modifica del rapporto | Non disponibile. Il rapporto esistente viene mantenuto. [Crea un nuovo report](#create-report) quando sono necessarie modifiche |

## Risoluzione dei problemi {#troubleshooting}

**Nessun dato di misurazione disponibile**

La scheda **[!UICONTROL Misura]** mostra &quot;Nessun dato di misurazione disponibile&quot; fino al completamento delle query di impostazione dei dati in background attivate al momento della creazione del progetto. Questa operazione può richiedere fino a 24 ore. Se il messaggio &#39;Nessun dato di misurazione disponibile&#39; persiste dopo 24 ore, verificare che nell&#39;istanza [!DNL AMC] siano presenti campagne eseguite negli ultimi tre mesi, in quanto questo è l&#39;intervallo di lookback predefinito utilizzato durante l&#39;individuazione della campagna. Se esistono campagne idonee e il messaggio persiste, controlla lo stato della campagna nel tuo account [Amazon Ads](https://advertising.amazon.com/sign-in){target="_blank"}.

**Nessuna campagna visualizzata nel menu a discesa [!UICONTROL ID campagna]**

Le campagne possono essere assenti anche quando la scheda **[!UICONTROL Misura]** è visibile. [!DNL AMC] applica una soglia minima di utenti ai dati della campagna. Le campagne che non soddisfano la soglia minima di utenti univoci vengono escluse e le query di report non restituiranno alcun risultato. Verifica che le campagne su cui desideri creare rapporti abbiano una portata sufficiente. Per informazioni dettagliate sulle soglie di aggregazione di [!DNL AMC], consultare la [documentazione sulle soglie di aggregazione AMC](https://advertising.amazon.com/API/docs/en-us/guides/amazon-marketing-cloud/aggregation-threshold){target="_blank"}.

**Risultati non visibili dopo la data di esecuzione**

Consentire fino a 24 ore dopo la data di esecuzione pianificata per [!DNL AMC] di elaborare le query del report e restituire i risultati. Se il report rimane in sospeso dopo tale periodo, verificare che la data di esecuzione sia stata superata e che lo stato del report non sia più visualizzato come in sospeso.

**Gli eventi di conversione non sono disponibili e [!UICONTROL L&#39;attribuzione] è disattivata**

Ciò può verificarsi per tre motivi:

1. **Il monitoraggio delle conversioni non è abilitato.** È possibile che per l&#39;account dell&#39;inserzionista [!DNL AMC] non sia configurato il monitoraggio delle conversioni. Passa all&#39;[account Amazon Ads](https://advertising.amazon.com/sign-in){target="_blank"} e verifica che vengano tracciati gli eventi di conversione per le campagne pertinenti.
2. **Nessun evento di conversione registrato.** Anche se il tracciamento è abilitato, è possibile che l&#39;istanza [!DNL AMC] non abbia ancora registrato alcun evento di conversione.
3. **Soglia di aggregazione non raggiunta.** [!DNL AMC] applica una soglia minima ai dati di conversione. Se un tipo di evento di conversione non ha un numero sufficiente di occorrenze, non verrà restituito e non verrà visualizzato nell’elenco.

**Le conversioni appaiono inferiori al previsto**

Se la data di esecuzione del report è inferiore a 30 giorni dopo la fine dell&#39;intervallo di date, [!DNL AMC] potrebbe non aver acquisito tutte le conversioni all&#39;interno della finestra di attribuzione. [Crea un nuovo report](#create-report) con una data di esecuzione di almeno 30 giorni dopo la fine dell&#39;intervallo di date.

## Passaggi successivi {#next-steps}

Utilizzare i risultati del report per valutare le prestazioni della campagna e informare la pianificazione futura della campagna in [!DNL Amazon Advertising]. Ad esempio, puoi regolare il targeting, sopprimere i tipi di pubblico sovraesposti identificati nella distribuzione della frequenza o riallocare la spesa a posizionamenti con prestazioni elevate. Per analizzare una campagna o un periodo di reporting diverso, crea un altro rapporto di misurazione con le impostazioni appropriate.

Per una panoramica di tutte le funzionalità di collaborazione di [!DNL AMC] disponibili, vedere [[!DNL Amazon Marketing Cloud]](./amc.md).
