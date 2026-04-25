---
title: Configurare e gestire le destinazioni
description: Learn how to configure and manage destinations in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b4b26761-46ac-420f-b9f7-6e829d67aec9
TQID: https://experienceleague.adobe.com/3JoqIEJ0ilX3NHYOVersSkaa98kgPzOhqk94UP6Xc50
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 0%

---

# Configurare e gestire le destinazioni

{{limited-availability-release-note}}

Destinations are integrations used to send targeted audiences to external platforms. These integrations enable you to activate audiences across various marketing channels and platforms for use in campaigns and customer engagement.

Collaborators can configure destinations to send audiences to external platforms, such as Adobe Experience Platform, for use in campaigns. Collaborators can then [activate audiences within a project](../collaborate/activate.md), which are sent to their connection&#39;s configured destination. L&#39;attivazione può essere eseguita da uno dei collaboratori a seconda delle impostazioni di attivazione del pubblico [configurate nella connessione](/help/guide/connect/establishing-connections.md#configure-connection-settings).

![The My destinations tab in the Setup workspace showing an active Adobe Experience Platform destinations.](/help/assets/setup/manage-destinations/my-destinations-overview.png)

To learn more about destinations, refer to the [destinations overview](../destinations/overview.md) guide.

## Configure destinations {#configure-destinations}

Desintations are configured in the **[!UICONTROL Setup]** section of Collaboration. To configure a destination, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL My destinations]** tab. Here, you can view all available destinations.

>[!IMPORTANT]
>
>To configure and manage desintations, your user must have a role with the **Manage Audience Data** permission assigned to them. For more information about managing roles, refer to the [manage roles](../permissions/manage-roles.md) guide.

![The My destinations tab in the Setup workspace showing the available destinations.](/help/assets/setup/manage-destinations/my-destinations.png)

The set up process for destinations is dependent on the destination you are configuring. Refer to the [available destinations](../destinations/overview.md#available-destinations) catalog to view the available destinations and their configuration guides.

>[!NOTE]
>
>Currently, only Adobe Experience Platform is available as a self-serve destination within Real-Time CDP Collaboration. If you are interested in configuring a different destination, please contact your Adobe representative.

## Elimina destinazioni {#delete-destinations}

Deleting a destination removes it from your account, removes any previously sent audiences from the destination, and prevents any future audiences from being sent to that destination.

To delete a destination, navigate to the **[!UICONTROL My destinations]** tab in the **[!UICONTROL Setup]** section. Selezionare l&#39;opzione **[!UICONTROL Elimina]** per la destinazione da rimuovere.

![Area di lavoro Destinazioni personali con l&#39;opzione Elimina evidenziata per la destinazione Adobe Experience Platform.](/help/assets/setup/manage-destinations/delete-destination.png)

Viene visualizzata una finestra di dialogo di conferma, in cui è possibile confermare l’eliminazione della destinazione. Selezionare **[!UICONTROL Elimina]** per rimuovere la destinazione.

![Finestra di dialogo Elimina destinazione con l&#39;opzione Elimina evidenziata.](/help/assets/setup/manage-destinations/delete-destination-confirmation.png)

## Passaggi successivi

Dopo aver configurato la destinazione, puoi iniziare a collaborare con le tue connessioni a [attivare tipi di pubblico mirati](../collaborate/activate.md) all&#39;interno dei tuoi progetti.
