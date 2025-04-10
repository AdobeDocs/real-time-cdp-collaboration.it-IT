---
title: Misurare le prestazioni
description: Misura le prestazioni delle campagne su canali diversi. Scopri come utilizzare e interpretare vari rapporti.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 3%

---

# Misurare le prestazioni

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L&#39;area di lavoro **[!UICONTROL Measure]** è disponibile solo se il caso di utilizzo **Campaign measurement** è stato abilitato [durante il processo di connessione](../connect/establishing-connections.md#connection-settings). Per ulteriori informazioni sui casi d&#39;uso, consulta la guida [gestisci progetti](./manage-projects.md#project-use-cases).

Scopri i rapporti disponibili in Real-Time CDP Collaboration e come misurare e analizzare le prestazioni delle campagne di marketing su vari canali.

## Prerequisiti

Prima di poter accedere ai rapporti di misurazione in Real-Time CDP Collaboration, è necessario:

* [Connesso](/help/guide/connect/establishing-connections.md) a un inserzionista o editore desiderato con il caso d&#39;uso **Misurazione campagna** abilitato e ha iniziato a collaborare a [progetti](/help/guide/collaborate/manage-projects.md)
* Esegui una campagna e [dati di misurazione caricati](/help/guide/setup/onboard-measurement-data.md) in Real-Time CDP Collaboration.

## Visualizza rapporti

Per visualizzare i rapporti disponibili nella scheda Misurazione:

1. Passa a **[!UICONTROL Collabora]** > **[!UICONTROL Progetti personali]**.
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
>abstract="Utilizza la visualizzazione metriche nel tempo per comprendere il numero totale di impression visualizzate per il tuo contenuto creativo durante il periodo della campagna. Puoi selezionare un massimo di due dimensioni da visualizzare nel rapporto."

Utilizza la visualizzazione metriche nel tempo per comprendere il numero totale di impression visualizzate per il tuo contenuto creativo durante il periodo della campagna. Puoi selezionare un massimo di due metriche da visualizzare e analizzare nel rapporto.

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

## Passaggi successivi

![Rileva, attiva e misura per gli inserzionisti.](/help/assets/end-to-end-workflow/discover-activate-measure.png)

Nello spirito della ciclicità dell’immagine precedente, utilizza le informazioni ottenute visualizzando i rapporti per pianificare la tua prossima campagna. Se necessario, in qualità di inserzionista, torna alla scoperta di diversi editori ed esegui le sovrapposizioni per scoprire tipi di pubblico diversi per le tue campagne successive.
