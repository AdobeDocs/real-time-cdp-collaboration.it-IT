---
title: Amazon Marketing Cloud
description: Scopri come collaborare con Amazon Marketing Cloud in Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 1a1b8fec-384b-465f-832d-0772c518fdf1
TQID: https://experienceleague.adobe.com/jNTQWEaUuuvgqKboJWsUH4XoKStP49nB0GLUSze0eXw
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 665
ht-degree: 20%

---

# Amazon Marketing Cloud

{{limited-availability-release-note}}

Dopo aver creato una connessione con [!DNL Amazon Marketing Cloud] ([!DNL AMC]), gli inserzionisti possono [creare un progetto](../manage-projects.md#create-project) per collaborare con [!DNL AMC] per sfruttare le funzionalità di analisi avanzate. Dopo aver creato un progetto, puoi utilizzare la sezione **[!UICONTROL Discover]** per confrontare approfondimenti sul pubblico e scoprire tipi di pubblico rilevanti per le campagne.

>[!IMPORTANT]
>
>Gli unici casi d&#39;uso supportati con [!DNL AMC] sono **Individuazione pubblico** e **Misurazione**. Attualmente, nel tuo progetto con [!DNL AMC] è disponibile solo la sezione **[!UICONTROL Discover]**.

## Scopri {#discover}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_compare_audiences"
>title="Confronta i tipi di pubblico"
>abstract="Confronta il pubblico con tutti i consumatori raggiunti dai tuoi annunci Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_relevant_audiences"
>title="Tipi di pubblico pertinenti"
>abstract="Segmenti di targeting di Amazon per i quali esiste una maggiore sovrapposizione con il tuo pubblico, considerando solo le impression dalla DSP (il targeting di questi segmenti può essere eseguito solo nella DSP)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_resolved_ids"
>title="ID risolti"
>abstract="Numero di ID che sono stati risolti dal servizio Identity Resolution di Amazon utilizzando i dati del tuo pubblico."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="ID annuncio esposto e sovrapposto"
>abstract="Rappresenta il numero di “ID risolti” dal pubblico caricato che sono anche stati esposti a un annuncio tramite Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="Sovrapposizione %"
>abstract="Percentuale di “ID risolti” che sono stati esposti a un annuncio tramite Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Raggruppamento per annuncio pubblicitario Amazon"
>abstract="Raggruppamento di “ID sovrapposti ed esposti ad annunci” raggiunti dal prodotto sponsorizzato da Amazon Ads e/o dalla DSP di Amazon Ads."

Nella sezione **[!UICONTROL Discover]**, puoi confrontare il pubblico AMC con tutti i consumatori raggiunti dai tuoi annunci Amazon Ads. Puoi anche visualizzare i segmenti di targeting di Amazon con cui il pubblico ha le sovrapposizioni più elevate, considerando solo le impression di DSP (questi segmenti possono essere targetizzati solo in DSP).

>[!IMPORTANT]
>
>I dati sul pubblico vengono elaborati dai tipi di pubblico caricati sul tuo account [!DNL Amazon Ads]. Per informazioni su come inviare e utilizzare la funzionalità Destinazioni di Experience Platform per inviare i tuoi tipi di pubblico al tuo account [!DNL Amazon Ads], leggi la [guida alla connessione di Amazon Ads](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/advertising/amazon-ads).

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
