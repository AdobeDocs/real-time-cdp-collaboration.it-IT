---
title: Desintations overview
description: Learn about destinations in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
TQID: https://experienceleague.adobe.com/1VvnSt3Z65dfQBfXnjJJi3H0Oj9BxFStexq3icVKxkY
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 360
ht-degree: 3%

---

# Panoramica sulle destinazioni

{{limited-availability-release-note}}

Destinations are integrations used to send targeted audiences to external platforms. These integrations enable you to activate audiences across various marketing channels and platforms for use in campaigns and customer engagement.

Collaborators can configure destinations to send audiences to external platforms, such as Adobe Experience Platform, for use in campaigns. Collaborators can then [activate audiences within a project](../collaborate/activate.md), which are sent to their connection&#39;s configured destination. L&#39;attivazione può essere eseguita da uno dei collaboratori a seconda delle impostazioni di attivazione del pubblico [configurate nella connessione](/help/guide/connect/establishing-connections.md#configure-connection-settings).

>[!IMPORTANT]
>
>Currently, when collaborators activate audiences within a project, they are automatically sent to their connection&#39;s configured destination. You **must** configure a destination before your collaborator can activate audiences within a project.

## Configure destinations {#configure-destinations}

To configure a destination, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL My destinations]** tab. Here, you can view all available destinations.

>[!NOTE]
>
> Currently, only Adobe Experience Platform is available as a self-serve destination within Collaboration. If you are interested in configuring a destination such as Amazon S3 or Snowflake, please contact your Adobe representative.

![The My destinations tab in the Setup workspace showing the available destinations.](/help/assets/destinations/overview/my-destinations-overview.png)

To begin configuring a destination, select the **[!UICONTROL Set up]** option within the destination of your choice. For information on configuring specific destinations, refer to the guides in the [available destinations](#available-destinations) table.

![The My destinations workspace with the Set up option highlighted for the Adobe Experience Platform desintation.](/help/assets/destinations/overview/my-destinations-set-up.png)

### Available destinations {#available-destinations}

The following destinations are available for configuration in Collaboration. To view the configuration guide for that destination, select the destination name in the table below. If you are interested in configuring a destination that is not currently available, please contact your Adobe representative.

| Destinazione | Disponibilità |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Disponibile |
| [!DNL Amazon S3] | In arrivo. |
| [!DNL Snowflake] | In arrivo. |
| [!DNL Google Cloud Storage] | In arrivo. |
| [!DNL Azure Blob Storage] | In arrivo. |

>[!NOTE]
>
>**[!DNL Google Cloud Storage]** in questa tabella fa riferimento a **destinazioni** (in cui Collaboration invia tipi di pubblico durante l&#39;attivazione). Per **i tipi di pubblico di origine da** un bucket GCS nell&#39;area di lavoro **[!UICONTROL Configurazione]**, vedere [Configurazione di GCS per l&#39;origine del pubblico](../setup/configure-gcs-audience-sourcing.md).

## Passaggi successivi

Dopo aver configurato la destinazione, puoi iniziare a [attivare tipi di pubblico mirati](../collaborate/activate.md) all&#39;interno dei tuoi progetti.
