---
title: Requisiti di connessione della destinazione
description: Esamina le informazioni di connessione necessarie per configurare le destinazioni supportate in Real-Time CDP Collaboration.
audience: admin, publisher
source-git-commit: c84582bb81289ce761c664af7db177535ff00a00
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 1%

---

# Requisiti di connessione della destinazione

Prima di configurare una destinazione in Real-Time CDP Collaboration, è necessario ottenere le credenziali e le informazioni di connessione richieste dal provider di destinazione.

In questa pagina sono riepilogati i metodi di autenticazione disponibili in Collaboration. Per istruzioni sulla creazione delle credenziali, sull’assegnazione delle autorizzazioni, sulla configurazione dell’accesso alla rete o sulla preparazione del sistema di destinazione, consulta la documentazione collegata sulla destinazione di Adobe Experience Platform.

>[!NOTE]
>
>La documentazione Adobe Experience Platform collegata descrive il flusso di lavoro di destinazione standard. Alcuni passaggi, campi o opzioni potrebbero non essere applicabili durante la configurazione della destinazione in Real-Time CDP Collaboration.

## Panoramica dei requisiti {#requirements-at-a-glance}

| Destinazione | Metodo di autenticazione o connessione | Prepara prima di iniziare | Requisiti dettagliati |
|---|---|---|---|
| [!DNL Amazon S3] | Chiave di accesso e chiave segreta, o ruolo presunto | coppia di chiavi di accesso AWS o ruolo IAM ARN; informazioni su bucket e cartelle | [[!DNL Amazon S3] documentazione di destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3) |
| SFTP | Password o chiave SSH | Dominio del server, porta, nome utente, credenziali di autenticazione e percorso della cartella | [Documentazione di destinazione SFTP](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/cloud-storage/sftp) |
| [!DNL Azure Blob Storage] | Stringa di connessione | Informazioni su stringa di connessione di archiviazione Azure, contenitore e cartella | [[!DNL Azure Blob Storage] documentazione di destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob) |
| [!DNL Google Cloud Storage] | ID chiave di accesso e chiave di accesso segreta | Credenziali di interoperabilità, bucket e informazioni sulla cartella [!DNL Google Cloud Storage] | [[!DNL Google Cloud Storage] documentazione di destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage) |
| [!DNL Snowflake Batch] | Condivisione dati [!DNL Snowflake] | ID account [!DNL Snowflake], area geografica, stato del collegamento privato e accesso alle inserzioni private | [[!DNL Snowflake Batch] documentazione di destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch) |
| [!DNL Data Landing Zone] | Non è richiesta alcuna autenticazione separata | Percorso della cartella di destinazione e preferenze di output dei file | [[!DNL Data Landing Zone] documentazione di destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone) |

## Note del connettore {#connector-notes}

Prima di configurare una destinazione, controlla i seguenti metodi di autenticazione specifici per il connettore e le differenze del flusso di lavoro.

### [!DNL Amazon S3] {#amazon-s3}

Collaboration supporta l&#39;autenticazione **[!UICONTROL Chiave di accesso]** e **[!UICONTROL Ruolo assunto]**. L’autenticazione tramite chiave di accesso richiede una chiave di accesso e una chiave di accesso segreta. L’autenticazione con ruolo assunto richiede l’ARN di un ruolo AWS IAM che Adobe può assumere.

Per le credenziali, i ruoli e le autorizzazioni, vedere [Autentica nella [!DNL Amazon S3] destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#authenticate).

### SFTP {#sftp}

Collaboration supporta **[!UICONTROL SFTP con password]** e **[!UICONTROL SFTP con chiave SSH]**. Entrambi i metodi richiedono il dominio del server, la porta e il nome utente. La porta predefinita è `22`.

Per i requisiti relativi a formato chiave SSH, server, rete e inserisco nell&#39;elenco Consentiti di rete, vedere [Informazioni sull&#39;autenticazione SFTP](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/cloud-storage/sftp#authentication-information).

### [!DNL Azure Blob Storage] {#azure-blob-storage}

Collaboration esegue l&#39;autenticazione in [!DNL Azure Blob Storage] utilizzando una stringa di connessione dell&#39;account di archiviazione.

Per istruzioni su come ottenere la stringa di connessione e assegnare le autorizzazioni di archiviazione, vedere [Autentica nella [!DNL Azure Blob Storage] destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob#authenticate).

### [!DNL Google Cloud Storage] {#google-cloud-storage}

Collaboration richiede un ID chiave di accesso [!DNL Google Cloud Storage] e una chiave di accesso segreta generate tramite le impostazioni di interoperabilità [!DNL Google Cloud Storage].

Per i requisiti di generazione delle credenziali e di autorizzazione del bucket, vedi [Autentica nella [!DNL Google Cloud Storage] destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage#authenticate).

### [!DNL Snowflake Batch] {#snowflake-batch}

[!DNL Snowflake Batch] utilizza la condivisione dati [!DNL Snowflake] invece di esportare i file nell&#39;archivio gestito dal cliente. In Collaboration non esiste un passaggio di autenticazione separato. Immetti l’ID account Snowflake, l’area geografica, lo stato del collegamento privato e la conferma della proprietà dell’account durante la creazione della destinazione.

Per i requisiti di preparazione degli account e di inserimento nell&#39;elenco privato, consulta [[!DNL Snowflake Batch] documentazione di destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch).

### [!DNL Data Landing Zone] {#data-landing-zone}

Il provisioning di [!DNL Data Landing Zone] è stato eseguito da Adobe e non richiede un passaggio di autenticazione separato in Collaboration. Durante la creazione della destinazione, specificate il percorso della cartella di destinazione e le impostazioni di output del file.

Per informazioni sull&#39;accesso a un [!DNL Data Landing Zone] con provisioning AWS, vedere [Autenticazione nell&#39;area di destinazione dati con provisioning AWS](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone#authenticate-dlz-aws).

## Passaggi successivi {#next-steps}

Dopo aver ottenuto le informazioni di connessione richieste, [configurare e gestire una destinazione](./manage-destinations.md).
