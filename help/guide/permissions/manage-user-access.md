---
title: Manage user access through Permissions
description: Manage permissions and users access to different components of the Real-Time CDP Collaboration UI.
audience: admin
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0155f6a6-5e67-4415-af96-1848345842e4
TQID: https://experienceleague.adobe.com/uPFss3qIstJmeVFF1YpQQJ0V848SiDEfy6BYyEcgPZw
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1406
ht-degree: 2%

---

# Manage user access through Permissions {#manage-user-access}

{{limited-availability-release-note}}

Manage permissions and user access to individual components within Adobe Real-Time CDP Collaboration through the Experience Cloud [Permissions](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/browse){target="_blank"} interface. Permissions allows system and product administrators to define [roles](./manage-roles.md) to manage user access to specific features and resources.

## Configure access to Permissions {#permissions-access}

To access Permissions, you must have both product administrator and user access to the Adobe Experience Platform product. A system administrator is required to configure product administrator privileges, while user privileges can be configured by a system or product administrator. For more information on the administrative roles, read the [access control heirarchy](./overview.md#hierarchy) guide.

>[!TIP]
>
>In questa guida, un **amministratore** farà riferimento a **amministratori di sistema e di prodotto**.

### System Administrators: configure product administrator access {#admin-access}

Grant a user product administrator access to give them administrative capabilities within the Experience Platform product through the following steps:

>[!IMPORTANT]
>
>As a system administrator, you have out-of-the box access to specific Experience Cloud products, such as Adobe Admin Console. However, to use Permissions, you are required to give yourself product administrator and user access to the Experience Platform product. Follow the step-by-step guide below to give yourself access as a system administrator.

Log in to [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} with your credentials. The home view displays with a list of your available products within the **[!UICONTROL Quick access]** section. Seleziona **[!UICONTROL Admin Console]**.

![Experience Cloud&#39;s home view with Admin Console highlighted.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

The [Adobe Admin Console](https://adminconsole.adobe.com/) overview dashboard displays. Selezionare **[!UICONTROL Adobe Experience Platform]** dall&#39;elenco **[!UICONTROL Prodotti]** in **[!UICONTROL Prodotti e servizi]**.

![Admin Console&#39;s overview dashboard with the Adobe Experience Platform product highlighted.](../../assets/permissions/admin-console.png){zoomable="yes"}

The Adobe Experience Platform dashboard displays. Select the **[!UICONTROL Admins]** tab and then select **[!UICONTROL Add admin]**.

![Adobe Experience Platform product dashboard with the Admins tab selected and Add admin highlighted.](../../assets/permissions/add-admin.png){zoomable="yes"}

The **[!UICONTROL Add product administrators]** dialog appears. Enter the user email or username into the **[!UICONTROL Email or username]** text field and then select the correct account from the dropdown. Select **[!UICONTROL Save]** to finish adding the user as a product administrator.

![The Add product administrators dialog with a users information filled in and the Save option selected.](../../assets/permissions/add-product-administrators.png){zoomable="yes"}

The user now has product administrator privileges and can perform administrative functions, such as adding users or other admins, to the product within the Admin Console. Next they&#39;ll need user access to the Experience Platform product to access and perform functions within Permissions.

### Administrators: configure user access to Experience Platform {#user-access}

Now that you&#39;ve granted the user product administrator access, you need to provide them user access to the Experience Platform product. As part of the access configurations, you&#39;ll assign the user specific [product profiles](https://helpx.adobe.com/it/enterprise/using/manage-product-profiles.html).

>[!TIP]
>
>If you&#39;re following along from the previous section, you&#39;ll already be within the Adobe Experience Platform product and you may skip the first step.

Navigate to the [Admin Console](https://adminconsole.adobe.com/){target="_blank"} and select **[!UICONTROL Adobe Experience Platform]** from the **[!UICONTROL Products]** list under **[!UICONTROL Products and services]**.

![Experience Cloud&#39;s home view with Admin Console highlighted.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

Select the **[!UICONTROL Users]** tab and then select **[!UICONTROL Add users]**.

![Adobe Experience Platform product dashboard with the Users tab selected and Add users highlighted.](../../assets/permissions/add-users.png){zoomable="yes"}

The **[!UICONTROL Add users to this product]** dialog appears. Enter the user&#39;s name or email into the **[!UICONTROL Name, user group or email address]** text field and then select the correct account from the dropdown. Next, select the **[!UICONTROL Products]** add option.

![The Add users to this product dialog with a users information filled in and the Products add option selected.](../../assets/permissions/add-users-to-product.png){zoomable="yes"}

The **[!UICONTROL Select product profiles]** dialog appears. Select **[!UICONTROL AEP-Default-All-Users]** and **[!UICONTROL Default Production All Access]** and then select **[!UICONTROL Apply]**.

![The Select product profiles dialog with the AEP-Default-All-Users and Default Production All Access options selected and Apply highlighted.](../../assets/permissions/select-product-profiles.png){zoomable="yes"}

Confirm the information is correct and then select **[!UICONTROL Save]**.

![La finestra di dialogo Aggiungi utenti ai prodotti contiene le informazioni sugli utenti e i profili di prodotto visualizzati ed è evidenziata l&#39;opzione Salva.](../../assets/permissions/save-selections.png){zoomable="yes"}

Ora l’utente deve disporre dell’accesso amministratore di prodotto e prodotto ad Experience Platform, per poter accedere alle Autorizzazioni. Successivamente, devi assegnare all’utente due ruoli fondamentali per consentirgli di accedere all’interfaccia utente di Experience Platform.

### Amministratori: configurare l’accesso all’interfaccia utente di Experience Platform {#product-access}

In Real-Time CDP Collaboration, gli amministratori e gli utenti finali lavoreranno con i dati provenienti da Experience Platform, ad esempio i tipi di pubblico e i registri di audit. Questi dati vengono conservati all’interno di istanze di Experience Platform denominate sandbox. Per garantire che gli utenti possano interagire con questi dati, devi assegnare [ruoli predefiniti](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/home#default-roles){target="_blank"} all&#39;utente.

Per iniziare, passa a [Adobe Experience Cloud](https://experience.adobe.com/). Dovresti trovare **[!UICONTROL Experience Platform]** e **[!UICONTROL Autorizzazioni]** all&#39;interno di **[!UICONTROL Accesso rapido]**.

![Vista Home di Experience Cloud con Experience Platform e Autorizzazioni evidenziati.](../../assets/permissions/experience-cloud-products.png){zoomable="yes"}

>[!NOTE]
>
> L’accesso ai prodotti può richiedere alcuni minuti e riceverai un’e-mail di avviso per informarti che hai ricevuto l’accesso. Se dopo aver ricevuto l’e-mail non trovi Experience Platform o le Autorizzazioni in Adobe Experience Cloud, disconnettiti e accedi di nuovo al tuo account.

In questa fase, è ora possibile accedere a **[!UICONTROL Autorizzazioni]**. Se tenti di accedere a **[!UICONTROL Experience Platform]**, riceverai un avviso che informa che non sono abilitate sandbox, come mostrato di seguito. Per risolvere questo problema, devi assegnare i ruoli predefiniti al tuo utente. Per iniziare, seleziona **[!UICONTROL Autorizzazioni]**.

![Visualizzazione Home di Experience Cloud con un avviso visualizzato ed autorizzazioni evidenziate.](../../assets/permissions/experience-cloud-warning.png){zoomable="yes"}

Verrà visualizzato il dashboard **[!UICONTROL Autorizzazioni]**. Seleziona **Utenti** dal pannello a sinistra, quindi seleziona il nome dell&#39;utente.

![Dashboard delle autorizzazioni con l&#39;area di lavoro Utenti visualizzata ed un utente evidenziato.](../../assets/permissions/permissions-user.png){zoomable="yes"}

Selezionare la scheda **[!UICONTROL Ruoli]**, quindi selezionare **[!UICONTROL Aggiungi ruoli]**.

![Area di lavoro utente con la scheda Ruoli visualizzata ed Aggiungi ruoli evidenziati.](../../assets/permissions/user-roles.png){zoomable="yes"}

Viene visualizzata la finestra di dialogo **[!UICONTROL Aggiungi ruoli]**. Seleziona **[!UICONTROL Accesso predefinito a tutti i processi di produzione]** e **[!UICONTROL Amministratori sandbox]**, quindi seleziona **[!UICONTROL Salva]**.

![Finestra di dialogo Aggiungi ruoli con gli amministratori predefiniti di tutti gli accessi alla produzione e delle sandbox selezionati e Salva evidenziato.](../../assets/permissions/add-roles.png){zoomable="yes"}

You now have access to Experience Platform and Permissions. In the final step, you&#39;ll grant access to Real-Time CDP Collaboration.

### Amministratori: configurare l’accesso a Real-Time CDP Collaboration {#RTCDP-collaboration-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_permissions"
>title="guida alla gestione dell’accesso utente"
>abstract=""

To grant users access to Collaboration, you&#39;ll use an access control concept called roles. Roles define the level of access a administrator or user has to [resources](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/home#permissions) in your organization.

When configuring individual access to Collaboration, you&#39;ll assign users&#39; roles containing permissions from the Collaborations resource. You can use the [manage roles](./manage-roles.md) guide to find out information on:

- the [two standard roles](./manage-roles.md#standard-roles) and the levels of access they grant to Collaboration
- creating [custom roles](./manage-roles.md#specific-access-roles) using the Collaboration resource
- the list of permissions included in the Collaborations resource

>[!NOTE]
>
>Additionally, a user must be assigned to a role containing the **[!UICONTROL Prod]** permission in the **[!UICONTROL Sandboxes]** resources. Both standard roles contain this permission. If you choose to assign a user a custom role instead of a standard role, you must ensure one of the roles they are assigned to contain this permission.

Once you&#39;ve chosen or created a role that encompasses the level of access your user needs, you need to assign the user to that role.

#### Assign a role

You may assign multiple roles to a single user or assign multiple users to a single role. The first case was covered earlier when [assigning the default roles](#product-access) to give a user access to Experience Platform. In the next steps, you&#39;ll assign users directly to the role you&#39;ve selected.

In **[!UICONTROL Permissions]** select **[!UICONTROL Roles]** from the left panel and then select your role from the list.

![The Permissions dashboard with the Roles workspace displayed and a role highlighted.](../../assets/permissions/select-role.png){zoomable="yes"}

The role&#39;s detail page displays. Select the **[!UICONTROL Users]** tab and then select **[!UICONTROL Add Users]**.

![The role&#39;s detail workspace with the Users tab displayed and Add Users highlighted.](../../assets/permissions/role-users.png){zoomable="yes"}

The **[!UICONTROL Add Users]** dialog appears. Select the user(s) from the list and then select **[!UICONTROL Save]**.

![The Add Users dialog with a user select and the Save option highlighted.](../../assets/permissions/add-users-to-role.png){zoomable="yes"}

L&#39;utente dovrebbe ora vedere **[!UICONTROL RTCDP Collaboration]** elencato come prodotto in **[!UICONTROL Accesso rapido]** in Experience Cloud.

![Experience Cloud con RTCDP Collaboration è evidenziato in Accesso rapido](../../assets/permissions/rtcdp-experience-cloud.png)

## Passaggi successivi

Ora che gli utenti hanno accesso a Real-Time CDP Collaboration, possono iniziare a utilizzare il prodotto. Per ulteriori informazioni sul prodotto nel suo complesso, consulta la [guida alla panoramica](../home.md).
