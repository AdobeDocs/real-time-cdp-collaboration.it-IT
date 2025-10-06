---
title: Amazon Marketing Cloud
description: Scopri come collaborare con Amazon Marketing Cloud in Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 57b847c25edbf88f4708bda74be41fe6141472a7
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 4%

---

# Amazon Marketing Cloud

{{limited-availability-release-note}}

Dopo aver creato una connessione con [!DNL Amazon Marketing Cloud] ([!DNL AMC]), gli inserzionisti possono [creare un progetto](../manage-projects.md#create-project) per collaborare con [!DNL AMC] per sfruttare le funzionalità di analisi avanzate. Dopo aver creato un progetto, puoi utilizzare la sezione **[!UICONTROL Discover]** per confrontare approfondimenti sul pubblico e scoprire tipi di pubblico rilevanti per le campagne.

>[!IMPORTANT]
>
>Gli unici casi d&#39;uso supportati con [!DNL AMC] sono **Individuazione pubblico** e **Misurazione**. Attualmente, nel tuo progetto con **[!UICONTROL è disponibile solo la sezione]** Discover[!DNL AMC].

## Scopri {#discover}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_compare_audiences"
>title="Confronta i tipi di pubblico"
>abstract="Confronta il pubblico con tutti i consumatori raggiunti dai tuoi annunci Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_relevant_audiences"
>title="Tipi di pubblico pertinenti"
>abstract="Il targeting dei segmenti di Amazon per i quali il pubblico ha le sovrapposizioni più elevate, considerando solo le impression di DSP (questi segmenti possono essere targetizzati solo in DSP)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_resolved_ids"
>title="ID risolti"
>abstract="Il numero di ID che la risoluzione dell’identità di Amazon è stata in grado di risolvere utilizzando i dati del pubblico."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="ID annuncio esposto e sovrapposto"
>abstract="Rappresenta il numero di &quot;ID risolti&quot; dal pubblico caricato che sono stati esposti a un annuncio tramite Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="Sovrapposizione %"
>abstract="La proporzione di &quot;ID risolti&quot; che sono stati esposti a un annuncio tramite Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Raggruppamento per annuncio pubblicitario Amazon"
>abstract="Raggruppamento degli &quot;ID sovrapposti esposti agli annunci&quot; raggiunti dal prodotto sponsorizzato da Amazon Ads e/o dal DSP di Amazon Ads."

Nella sezione **[!UICONTROL Discover]**, puoi confrontare il pubblico AMC con tutti i consumatori raggiunti dai tuoi annunci Amazon Ads. Puoi anche visualizzare i segmenti di targeting di Amazon con cui il pubblico ha le sovrapposizioni più elevate, considerando solo le impression di DSP (questi segmenti possono essere targetizzati solo in DSP).

>[!IMPORTANT]
>
>I dati sul pubblico vengono elaborati dai tipi di pubblico caricati sul tuo account [!DNL Amazon Ads]. Per informazioni su come inviare e utilizzare la funzionalità Destinazioni di Experience Platform per inviare i tuoi tipi di pubblico al tuo account [!DNL Amazon Ads], leggi la [guida alla connessione di Amazon Ads](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/amazon-ads).

![Sezione di individuazione in un progetto con Amazon Marketing Cloud.](/help/assets/collaborate/advertising-platforms/amc-discover.png){zoomable="yes"}

### Confronta i tipi di pubblico {#compare-audiences}

La sezione **[!UICONTROL Confronto tipi di pubblico]** fornisce approfondimenti su come il pubblico [!DNL AMC] si sovrappone ai consumatori raggiunti dai tuoi annunci Amazon Ads. Nella sezione **[!UICONTROL Confronto tipi di pubblico]** è possibile visualizzare le metriche seguenti:

| Metrica | Descrizione |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID risolti] | Il numero di ID [!DNL Amazon’s Identity Resolution] che è stato possibile risolvere utilizzando i dati del pubblico. |
| [!UICONTROL ID sovrapposti esposti ad] | Il numero di [!UICONTROL ID risolti] dal pubblico caricato che sono stati esposti a un annuncio tramite [!DNL Amazon Ads]. |
| [!UICONTROL Sovrapposizione %] | Percentuale di [!UICONTROL ID risolti] che sono stati esposti a un annuncio tramite [!DNL Amazon Ads]. |
| [!UICONTROL Raggruppamento per prodotto annuncio Amazon] | Raggiunto raggruppamento di [!UICONTROL ID sovrapposti esposti ad] da [!UICONTROL Prodotto sponsorizzato] e/o [!UICONTROL DSP]. Ciascuno di essi è rappresentato come una singola percentuale rispetto al numero totale di ID esposti all’annuncio. Poiché un ID può appartenere sia a [!UICONTROL Prodotti sponsorizzati] che a [!UICONTROL DSP], la somma delle percentuali potrebbe non essere 100%. |


### Tipi di pubblico pertinenti {#relevant-audiences}

La sezione **[!UICONTROL Tipi di pubblico rilevanti]** fornisce informazioni approfondite su [!DNL Amazon] segmenti di targeting, o tipi di pubblico, con cui il pubblico ha le sovrapposizioni più elevate, considerando solo le impression di DSP (questi segmenti possono essere targetizzati solo in DSP). Puoi passare da un pubblico all’altro e, all’interno di ogni sezione, visualizzare le metriche seguenti:

| Metrica | Descrizione |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID risolti] | Il numero di ID [!DNL Amazon’s Identity Resolution] che è stato possibile risolvere utilizzando i dati del pubblico. |
| [!UICONTROL ID sovrapposti esposti ad] | Rappresenta il numero di [!UICONTROL ID risolti] dal pubblico caricato che sono stati esposti a un annuncio tramite [!DNL Amazon Ads]. Questo considera solo le impression di DSP. |
| [!UICONTROL Sovrapposizione %] | Percentuale di [!UICONTROL ID risolti] che sono stati esposti a un annuncio tramite [!DNL Amazon Ads]. |
| [!UICONTROL Categorie] | La categoria o le categorie a cui appartiene il pubblico. Un pubblico può appartenere a più categorie. |

### Rileva sovrapposizioni con [!DNL Amazon Marketing Cloud] {#discover-overlaps}

La sezione **[!UICONTROL Scopri le sovrapposizioni con Amazon Marketing Cloud]** fornisce approfondimenti sulla sovrapposizione dei tipi di pubblico con [!DNL Amazon] segmenti di targeting o tipi di pubblico. Puoi visualizzare le metriche seguenti:

| Metrica | Descrizione |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID risolti] | Il numero di ID [!DNL Amazon’s Identity Resolution] che è stato possibile risolvere utilizzando i dati del pubblico. |
| [!UICONTROL ID sovrapposti esposti ad] | Rappresenta il numero di [!UICONTROL ID risolti] dal pubblico caricato che sono stati esposti a un annuncio tramite [!DNL Amazon Ads]. Questo considera solo le impression di DSP. |
| [!UICONTROL Sovrapposizione %] | Percentuale di [!UICONTROL ID risolti] che sono stati esposti a un annuncio tramite [!DNL Amazon Ads]. |