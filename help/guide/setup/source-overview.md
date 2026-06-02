---
title: Panoramica sulle origini
description: Scopri i connettori sorgente in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
source-git-commit: 07666bc6d001e602c270a611ad1da3ea5f301dbd
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 6%

---

# Panoramica sulle origini

Ad Adobe Real-Time CDP Collaboration, per sorgente (o connessione dati) si intende il luogo da cui provengono i dati sul pubblico. Puoi connetterti a vari tipi di origine, ad esempio applicazioni Adobe, archivi basati su cloud o file dal sistema locale, per [generare e gestire i tipi di pubblico](./onboard-audiences.md) per i tuoi progetti Collaboration. Durante il flusso di lavoro di audience sourcing, puoi scegliere e impostare l’origine preferita in base alle esigenze della tua organizzazione.

## Collega un’origine {#connect-a-source}

Per collegare un&#39;origine, è necessario inserire il flusso di lavoro Acquisti. Innanzitutto, passa alla scheda **[!UICONTROL I miei tipi di pubblico]** nell&#39;area di lavoro **[!UICONTROL Configurazione]**.

Seleziona l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) e quindi seleziona **[!UICONTROL Pubblico]** per avviare il flusso di lavoro Acquisti.

![Area di lavoro Tipi di pubblico personali con le opzioni Aggiungi e Tipi di pubblico evidenziate.](/help/assets/setup/add-manage-audiences/add-audiences.png)

Durante il flusso di lavoro, verrà richiesto di aggiungere una nuova connessione dati selezionando un&#39;origine. La sorgente scelta determina il modo in cui i dati del pubblico vengono portati in Collaboration. Per un elenco di tutte le origini supportate, vedere la tabella [origini disponibili](#available-sources).

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione Aggiungi una nuova connessione dati evidenziata.](/help/assets/setup/add-manage-audiences/add-data-connection.png)

Dopo aver selezionato un’origine, il flusso di lavoro ti guida attraverso i passaggi di configurazione specifici della connessione, tra cui autenticazione, mappatura dei campi, pianificazione e selezione del pubblico.

### Origini disponibili {#available-sources}

In Collaboration sono disponibili le seguenti origini. Per visualizzare la guida dettagliata alla determinazione dell&#39;origine per tale origine, selezionare il nome dell&#39;origine nella tabella seguente. Se ti interessa un’origine attualmente non disponibile, contatta il tuo rappresentante Adobe.

| Origine | Descrizione | Disponibilità |
| --- | --- | --- |
| [Adobe Experience Platform](./onboard-audiences.md) | Importa i tipi di pubblico dalla tua istanza di Experience Platform connessa e riutilizza i segmenti di clienti esistenti. | Disponibile |
| [Amazon S3](./configure-aws-s3-audience-sourcing.md) | Connetti i bucket S3 per sorgente set di dati di prime parti di grandi dimensioni dalla tua infrastruttura cloud. | Disponibile |
| [[!DNL Snowflake]](./configure-snowflake-audience-sourcing.md) | Connetti [!DNL Snowflake Secure Data Share] per inserire set di dati di pubblico su larga scala. | Disponibile |
| [[!DNL Google Cloud Storage]](./configure-gcs-audience-sourcing.md) | Connetti i bucket GCS per inserire i dati del pubblico memorizzati nell&#39;ambiente [!DNL Google Cloud]. | Disponibile |
| [Caricamento file CSV](./upload-csv-audience-sourcing.md) | Carica un file CSV formattato direttamente dal sistema locale. | Disponibile |
| Adobe Audience Manager | Inserisci segmenti Audience Manager esistenti nei progetti Collaboration. | *In arrivo* |
| [!DNL Azure Blob Storage] | Connetti i contenitori [!DNL Azure Blob Storage] ai set di dati di prime parti di origine dall&#39;ambiente [!DNL Microsoft Azure]. | *In arrivo* |
| [!DNL Azure Data Lake Storage] | Connetti il tuo account [!DNL Azure Data Lake Storage Gen 2] per inserire i dati del pubblico memorizzati nel tuo data lake [!DNL Azure]. | *In arrivo* |

{style="table-layout:auto"}

## Passaggi successivi

Dopo aver collegato una sorgente e aver richiamato i tipi di pubblico, puoi visualizzare i dettagli, aggiornare le configurazioni o eliminare le sorgenti esistenti. Per ulteriori informazioni, vedere la guida [Gestione connessioni dati](./manage-data-connection.md).
