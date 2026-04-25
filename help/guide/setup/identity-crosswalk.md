---
title: Crosswalk delle identità
description: Scopri tutte le informazioni sui crosswalk di identità in Real-Time CDP Collaboration, tra cui come inserire i crosswalk di identità da origini diverse e come gestirli
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hide: true
exl-id: a51f112d-3da7-4482-a24a-6d9f269d28d1
TQID: https://experienceleague.adobe.com/0vUk3-vtaZvCoBmzkbrfMQF1NFaFg2NqsjJIje1sVcg
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 546
ht-degree: 22%

---

# Crosswalk delle identità

{{limited-availability-release-note}}

Scopri tutte le informazioni sui crosswalk di identità in Real-Time CDP Collaboration, tra cui come inserire i crosswalk di identità da origini diverse e come gestire i crosswalk di identità.

I crosswalk di identità facilitano il collegamento sicuro e conforme alla privacy delle identità dei clienti su più set di dati e piattaforme. Utilizzando gli identificatori con hash, Real-Time CDP Collaboration garantisce che gli utenti possano sincronizzare e riconciliare le identità senza esporre informazioni personali identificabili (PII, Personal Identifiable Information). Ciò consente una visione unificata del cliente per una migliore collaborazione e attività di marketing mirate.

Come primo passo, devi importare le crosswalk di identità in Real-Time CDP Collaboration. Per importare le crosswalk di identità in Real-Time CDP Collaboration, leggi la sezione seguente:

>[!NOTE]
>
>Nella versione beta di Real-Time CDP Collaboration, puoi importare i crosswalk di identità dai set di dati in Real-Time CDP. Ulteriori opzioni saranno disponibili nelle versioni successive.

## Importare crosswalks di identità in Real-Time CDP Collaboration {#import-crosswalk}

Passa alla scheda **[!UICONTROL Configurazione]** > **[!UICONTROL Percorsi incrociati di identità]**, seleziona l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) e seleziona **[!UICONTROL Percorsi incrociati di identità]**

![Registrazione di come accedere alla schermata per aggiungere crosswalks di identità](/help/assets/setup/identity-crosswalks/import-identity-crosswalk.gif)

### Seleziona origine crosswalk

Seleziona un’origine da cui importare il crosswalk dell’identità. Nella prima versione di Real-Time CDP Collaboration, Experience Platform è l’unica origine supportata per l’importazione di crosswalk.

>[!TIP]
>
>In Platform, i crosswalk che si stanno importando da Experience Platform sono denominati *set di dati*.

Dopo aver selezionato Experience Platform come origine dei crosswalk, seleziona la [sandbox Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/sandbox/home) da cui stai importando il crosswalk delle identità.

![Registrazione della modalità di selezione di un&#39;origine del crosswalk](/help/assets/setup/identity-crosswalks/select-crosswalk-source.gif)

### Seleziona crosswalk

Dopo aver selezionato Experience Platform come origine delle tue crosswalks,

### Fornisci dettagli

Fornisci un nome e una descrizione per il crosswalk di identità che stai importando nel prodotto.

### Selezionare una chiave di unione {#select-join-key}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_crosswalk_join_key"
>title="Chiave di unione"
>abstract="Una chiave di unione è un identificatore univoco utilizzato per associare e collegare record tra set di dati diversi. Permette di associare con precisione i dati provenienti da diverse origini alla stessa persona o entità. Una qualsiasi delle intestazioni di colonna dal crosswalk selezionato può fungere da chiave di unione."

Una chiave di unione è un identificatore univoco utilizzato per associare e collegare record tra set di dati diversi. Permette di associare con precisione i dati provenienti da diverse origini alla stessa persona o entità. Selezionando la chiave di unione appropriata, puoi unire e riconciliare in modo efficace i dati, migliorando la precisione e la completezza delle campagne.

Una qualsiasi delle intestazioni di colonna dal crosswalk selezionato può fungere da chiave di unione.

Selezionare la chiave di join desiderata per la tabella del percorso incrociato e selezionare **[!UICONTROL Avanti]** per procedere al passaggio successivo.

### Rivedi

Controlla le selezioni effettuate nelle schermate precedenti. Una volta effettuata la selezione, seleziona **[!UICONTROL Avanti]** per completare il flusso di lavoro.

## Passaggi successivi

Dopo aver appreso come importare le crosswalk di identità in Real-Time CDP, puoi visualizzare tutte le crosswalk di identità che hai aggiunto finora a Real-Time CDP Collaboration. You can also now use the identity crosswalks that you have imported when importing audiences into Real-Time CDP Collaboration.
