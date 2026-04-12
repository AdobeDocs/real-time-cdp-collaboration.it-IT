---
title: Gestire l’accesso degli utenti tramite autorizzazioni
description: Consente di gestire le autorizzazioni e l’accesso degli utenti a diversi componenti dell’interfaccia utente di Real-Time CDP Collaboration.
audience: admin
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0155f6a6-5e67-4415-af96-1848345842e4
source-git-commit: 0dead396657c97cec47ddd64c8ec3c349f541a8f
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 2%

---

# Gestire l’accesso degli utenti tramite autorizzazioni {#manage-user-access}

{{limited-availability-release-note}}

Gestisci le autorizzazioni e l&#39;accesso degli utenti ai singoli componenti all&#39;interno di Adobe Real-Time CDP Collaboration tramite l&#39;interfaccia di Experience Cloud [Autorizzazioni](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/browse){target="_blank"}. Le autorizzazioni consentono agli amministratori di sistema e di prodotto di definire [ruoli](./manage-roles.md) per gestire l&#39;accesso degli utenti a funzioni e risorse specifiche.

## Configurare l’accesso alle autorizzazioni {#permissions-access}

Per accedere alle autorizzazioni, devi disporre dell’accesso amministratore e utente al prodotto Adobe Experience Platform. Per configurare i privilegi di amministratore di prodotto è necessario un amministratore di sistema, mentre i privilegi utente possono essere configurati da un amministratore di sistema o di prodotto. Per ulteriori informazioni sui ruoli amministrativi, leggere la [guida al controllo degli accessi](./overview.md#hierarchy).

>[!TIP]
>
>In questa guida, un **amministratore** farà riferimento a **amministratori di sistema e di prodotto**.

### Amministratori di sistema: configurare l’accesso come amministratore del prodotto {#admin-access}

Concedi a un amministratore di prodotto utente l’accesso per fornire funzionalità amministrative all’interno del prodotto Experience Platform tramite i seguenti passaggi:

>[!IMPORTANT]
>
>In qualità di amministratore di sistema, hai accesso predefinito a prodotti Experience Cloud specifici, come Adobe Admin Console. Tuttavia, per utilizzare le Autorizzazioni, è necessario fornire a se stessi l’accesso al prodotto Experience Platform all’amministratore del prodotto e all’utente. Segui la guida dettagliata seguente per accedere a come amministratore di sistema.

Accedi a [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} con le tue credenziali. Viene visualizzata la visualizzazione Home con un elenco dei prodotti disponibili nella sezione **[!UICONTROL Accesso rapido]**. Seleziona **[!UICONTROL Admin Console]**.

![Visualizzazione Home di Experience Cloud con Admin Console evidenziato.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

Viene visualizzato il dashboard della panoramica di [Adobe Admin Console](https://adminconsole.adobe.com/). Selezionare **[!UICONTROL Adobe Experience Platform]** dall&#39;elenco **[!UICONTROL Prodotti]** in **[!UICONTROL Prodotti e servizi]**.

![Dashboard di panoramica di Admin Console con il prodotto Adobe Experience Platform evidenziato.](../../assets/permissions/admin-console.png){zoomable="yes"}

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

![Visualizzazione Home di Experience Cloud con Admin Console evidenziato.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

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

In Real-Time CDP Collaboration, gli amministratori e gli utenti finali lavoreranno con i dati provenienti da Experience Platform, ad esempio i tipi di pubblico e i registri di audit. Questi dati vengono conservati all’interno di istanze di Experience Platform denominate sandbox. Per garantire che gli utenti possano interagire con questi dati, devi assegnare [ruoli predefiniti](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#default-roles){target="_blank"} all&#39;utente.

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

Ora puoi accedere ad Experience Platform e alle Autorizzazioni. Nel passaggio finale, concederai l’accesso a Real-Time CDP Collaboration.

### Amministratori: configurare l’accesso a Real-Time CDP Collaboration {#RTCDP-collaboration-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_permissions"
>title="guida alla gestione dell’accesso utente"
>abstract=""

Per concedere agli utenti l’accesso a Collaboration, utilizza un concetto di controllo degli accessi denominato ruoli. I ruoli definiscono il livello di accesso di un amministratore o un utente alle [risorse](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#permissions) della tua organizzazione.

Quando configuri l’accesso individuale a Collaboration, assegni i ruoli degli utenti contenenti le autorizzazioni dalla risorsa Collaborazioni. Puoi usare la guida [gestione ruoli](./manage-roles.md) per ottenere informazioni su:

- i [due ruoli standard](./manage-roles.md#standard-roles) e i livelli di accesso concessi a Collaboration
- creazione di [ruoli personalizzati](./manage-roles.md#specific-access-roles) tramite la risorsa Collaboration
- l&#39;elenco delle autorizzazioni incluse nella risorsa Collaborazioni

>[!NOTE]
>
>Inoltre, un utente deve essere assegnato a un ruolo contenente l&#39;autorizzazione **[!UICONTROL Prod]** nelle risorse **[!UICONTROL Sandbox]**. Entrambi i ruoli standard contengono questa autorizzazione. Se si sceglie di assegnare a un utente un ruolo personalizzato anziché un ruolo standard, è necessario assicurarsi che uno dei ruoli assegnati contenga questa autorizzazione.

Dopo aver scelto o creato un ruolo che include il livello di accesso necessario per l&#39;utente, è necessario assegnare l&#39;utente a tale ruolo.

#### Assegna un ruolo

È possibile assegnare più ruoli a un singolo utente o più utenti a un singolo ruolo. Il primo caso è stato trattato in precedenza quando [sono stati assegnati i ruoli predefiniti](#product-access) per concedere a un utente l&#39;accesso ad Experience Platform. Nei passaggi successivi, gli utenti verranno assegnati direttamente al ruolo selezionato.

In **[!UICONTROL Autorizzazioni]** seleziona **[!UICONTROL Ruoli]** dal pannello a sinistra, quindi seleziona il tuo ruolo dall&#39;elenco.

![Dashboard delle autorizzazioni con l&#39;area di lavoro Ruoli visualizzata ed evidenziato un ruolo.](../../assets/permissions/select-role.png){zoomable="yes"}

Viene visualizzata la pagina dei dettagli del ruolo. Selezionare la scheda **[!UICONTROL Utenti]**, quindi selezionare **[!UICONTROL Aggiungi utenti]**.

![Area di lavoro dettagli del ruolo con la scheda Utenti visualizzata ed Aggiungi utenti evidenziata.](../../assets/permissions/role-users.png){zoomable="yes"}

Viene visualizzata la finestra di dialogo **[!UICONTROL Aggiungi utenti]**. Seleziona gli utenti dall&#39;elenco, quindi seleziona **[!UICONTROL Salva]**.

![La finestra di dialogo Aggiungi utenti con la selezione di un utente e l&#39;opzione Salva evidenziate.](../../assets/permissions/add-users-to-role.png){zoomable="yes"}

L&#39;utente dovrebbe ora vedere **[!UICONTROL RTCDP Collaboration]** elencato come prodotto in **[!UICONTROL Accesso rapido]** in Experience Cloud.

![Experience Cloud con RTCDP Collaboration è evidenziato in Accesso rapido](../../assets/permissions/rtcdp-experience-cloud.png)

## Passaggi successivi

Ora che gli utenti hanno accesso a Real-Time CDP Collaboration, possono iniziare a utilizzare il prodotto. Per ulteriori informazioni sul prodotto nel suo complesso, consulta la [guida alla panoramica](../home.md).
