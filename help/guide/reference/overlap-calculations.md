---
title: Calcolo dei conteggi e delle percentuali di sovrapposizione
description: Scopri come vengono calcolati i conteggi e le percentuali di sovrapposizione in varie aree di Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 23dc33af83366806f7d99161b4b713a33daeec76
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 1%

---


# Calcolo dei conteggi e delle percentuali di sovrapposizione

Ad Adobe Real-Time CDP Collaboration, comprendere la sovrapposizione dei tipi di pubblico è fondamentale per ottimizzare le strategie di marketing e garantire un’efficace collaborazione tra inserzionisti e editori. Questo documento spiega come vengono calcolati i conteggi e le percentuali di sovrapposizione in varie aree di prodotto utilizzando dati di esempio.

## Dati di esempio - Conteggio identità

### Ipotesi a scopo di calcolo

Per questo esempio, supponiamo che:

* L’inserzionista dispone di tre tipi di pubblico (A1, A2, A3).
* L’editore dispone di tre tipi di pubblico (P1, P2, P3).
* Tutte le identità chiave di corrispondenza si escludono a vicenda tra tutti i tipi di pubblico.

>[!NOTE]
>
>In realtà, ci sarebbe qualche sovrapposizione tra le identità chiave della corrispondenza di ogni pubblico, ma per semplicità, questo esempio presuppone che siano esclusive in questo caso.

### Pubblico inserzionista

| Pubblico inserzionista | A1 | A2 | A3 | TUTTO |
|----------------------|------|------|------|------|
| Identità e-mail con hash | 300 K | 450 K | 250 K | 1 M |
| Identità ID lampada | 500 K | 200.000 | 700 K | 1,4 M |
| Conteggio identità totale | 800 K | 650 K | 950 K | 2,4 M |

### Pubblico di Publisher

| Pubblico di Publisher | P1 | P2 | P3 | TUTTO |
|---------------------|------|------|------|------|
| Identità e-mail con hash | 150 K | 600 K | 550 K | 1,3 M |
| Identità ID Liveramp | 400 K | 350 K | 100.000 | 850 K |
| Conteggio identità totale | 550 K | 950 K | 800 K | 2,3 M |

## Calcolo dei conteggi e delle percentuali di sovrapposizione

### Dati di esempio - Conteggio sovrapposizioni

#### Inserzionista ogni vs. editore ogni

|                     | A1 - P1 | A2 - P2 | A3 - P3 |
|---------------------|---------|---------|---------|
| Sovrapposizione per e-mail con hash | 100.000 | 300 K | 150 K |
| Sovrapposizione per ID Liveramp | 200.000 | 150 K | 50 K |
| Sovrapposizione totale | 300 K | 450 K | 200.000 |

#### Advertiser Each vs Publisher ALL

|                     | A1 - P TUTTO | A2 - P TUTTO | A3 - P TUTTO |
|---------------------|------------|------------|------------|
| Sovrapposizione per e-mail con hash | 250 K | 400 K | 200.000 |
| Sovrapposizione per ID Liveramp | 350 K | 150 K | 230 K |
| Sovrapposizione totale | 600 K | 550 K | 430 K |

#### Inserzionista TUTTO vs Editore ciascuno

|                     | A ALL - P1 | A ALL - P2 | A ALL - P3 |
|---------------------|------------|------------|------------|
| Sovrapposizione per e-mail con hash | 120 K | 530 K | 200.000 |
| Sovrapposizione per ID Liveramp | 350 K | 330 K | 50 K |
| Sovrapposizione totale | 470 K | 860 K | 250 K |

#### Advertiser (Inserzionista) TUTTI e Publisher TUTTI

|                     | A ALL - P ALL |
|---------------------|---------------|
| Sovrapposizione per e-mail con hash | 850 K |
| Sovrapposizione per ID Liveramp | 730 K |
| Sovrapposizione totale | 1,58 M |

## Scopri modulo

Il modulo **[!UICONTROL Discover]** in Adobe Real-Time CDP Collaboration fornisce informazioni utili sui dati del pubblico. Comprendendo le sovrapposizioni di pubblico, puoi identificare potenziali opportunità di collaborazione tra editori e inserzionisti. La sezione **[!UICONTROL Audience Insights]** all&#39;interno del modulo **[!UICONTROL Discover]** consente di analizzare i conteggi e le percentuali di sovrapposizione tra tipi di pubblico diversi.

![Modulo di individuazione del flusso di lavoro di collaborazione.](/help/assets/reference/overlap-calculations/discover-module-overlap-calculations.png)

Di seguito sono riportati alcuni esempi di calcoli e formule per vari scenari di sovrapposizione.

### Tutti i tipi di pubblico degli inserzionisti e tutti i tipi di pubblico degli editori

| Pubblico inserzionista | Pubblico di Publisher | Conteggio identità (A) | Identità sovrapposte (B) | Percentuale di sovrapposizione | Raggruppamento chiave di corrispondenza | % raggruppamento chiave di corrispondenza |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| TUTTO | TUTTO | Conteggio identità totale di TUTTI i tipi di pubblico degli inserzionisti <br> Conteggio identità = 1M + 1,4M = 2,4M | Sovrapposizione totale tra TUTTI i tipi di pubblico degli inserzionisti e TUTTI i tipi di pubblico degli editori per tutte le chiavi di corrispondenza <br> Identità sovrapposte = 1,58M | Percentuale di identità sovrapposte sul conteggio identità totale di TUTTI i tipi di pubblico degli inserzionisti <br> % sovrapposizione = (B / A) * 100 = (1,58 M / 2,4 M) * 100 = 65,83% <br> Percentuale sovrapposizione = 65,83% | Sovrapposizione di identità per chiave di corrispondenza <br> Sovrapposizione per e-mail con hash = 850K <br> Sovrapposizione per ID Liveramp = 730K | Percentuale di sovrapposizione chiave di corrispondenza sul totale delle identità sovrapposte <br> % chiave di corrispondenza per e-mail con hash = (850K / 1,58M) * 100 = 53,8% <br> per ID Liveramp = (730K / 1,58M) * 100 = 46,2% |

### Tutti i tipi di pubblico degli inserzionisti e un pubblico dell’editore

| Pubblico inserzionista | Pubblico di Publisher | Conteggio identità (A) | Identità sovrapposte (B) | Percentuale di sovrapposizione | Raggruppamento chiave di corrispondenza | % raggruppamento chiave di corrispondenza |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| TUTTO | 1 P2 | Conteggio identità totale di tutti i tipi di pubblico degli inserzionisti <br> Conteggio identità = 1M + 1,4M = 2,4M | Sovrapposizione totale tra TUTTI i tipi di pubblico dell&#39;inserzionista e il pubblico dell&#39;editore selezionato P2 per tutte le chiavi di corrispondenza <br> Identità sovrapposte = 860K | Percentuale di identità sovrapposte sul conteggio identità totale di TUTTI i tipi di pubblico degli inserzionisti <br> % sovrapposizione = (B / A) * 100 = (860K / 2,4M) * 100 = 35,83% <br> Percentuale sovrapposizione = 35,83% | Sovrapposizione di identità per chiave di corrispondenza <br> Sovrapposizione per e-mail con hash = 530K <br> Sovrapposizione per ID Liveramp = 330K | Percentuale di sovrapposizione chiave di corrispondenza sul totale delle identità sovrapposte <br> Chiave di corrispondenza % per e-mail con hash = (530K/860K) * 100 = 61,62% <br> per ID Liveramp = (330K/860K) * 100 = 38,38% |

### Un solo pubblico inserzionista e tutti i tipi di pubblico dell’editore

| Pubblico inserzionista | Pubblico di Publisher | Conteggio identità (A) | Identità sovrapposte (B) | Percentuale di sovrapposizione | Raggruppamento chiave di corrispondenza | % raggruppamento chiave di corrispondenza |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| 1 A1 | TUTTO | Numero totale di identità del pubblico selezionato dall&#39;inserzionista A1 <br> Numero di identità = 300K + 500K = 800K | Sovrapposizione totale tra il pubblico dell&#39;inserzionista A1 e TUTTI i tipi di pubblico dell&#39;editore per tutte le chiavi di corrispondenza <br> Identità sovrapposte = 600K | Percentuale di identità sovrapposte sul conteggio identità del pubblico selezionato dall&#39;inserzionista (A1) <br> % sovrapposizione = (B / A) * 100 = (600K / 800K) * 100 = 75% <br> Percentuale sovrapposizione = 75% | Sovrapposizione di identità per chiave di corrispondenza <br> Sovrapposizione per e-mail con hash = 250K <br> Sovrapposizione per ID Liveramp = 350K | Percentuale di sovrapposizione chiave di corrispondenza sul totale delle identità sovrapposte <br> Chiave di corrispondenza % per e-mail con hash = (250K/600K) * 100 = 41,67% <br> per ID Liveramp = (350K/600K) * 100 = 58,33% |

### Un pubblico di inserzionisti e un pubblico di editori

| Pubblico inserzionista | Pubblico di Publisher | Conteggio identità (A) | Identità sovrapposte (B) | Percentuale di sovrapposizione | Raggruppamento chiave di corrispondenza | % raggruppamento chiave di corrispondenza |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| 1 A2 | 1 P2 | Numero totale di identità del pubblico selezionato dall&#39;inserzionista A2 <br> Numero di identità = 450K + 200K = 650K | Sovrapposizione totale tra il pubblico dell&#39;inserzionista A2 selezionato e il pubblico dell&#39;editore P2 selezionato per tutte le chiavi di corrispondenza <br> Identità sovrapposte = 450K | Percentuale di identità sovrapposte sul conteggio identità del pubblico selezionato (A2) <br> % sovrapposizione = (B / A) * 100 = (450K / 650K) * 100 = 69,23% <br> Percentuale sovrapposizione = 69,23% | Sovrapposizione di identità per chiave di corrispondenza <br> Sovrapposizione per e-mail con hash = 300K <br> Sovrapposizione per ID Liveramp = 150K | Percentuale di sovrapposizione chiave di corrispondenza sul totale delle identità sovrapposte <br> Chiave di corrispondenza % per e-mail con hash = (300K/450K) * 100 = 66,67% <br> per ID Liveramp = (150K/450K) * 100 = 33,33% |
