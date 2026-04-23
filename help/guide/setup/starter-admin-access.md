---
title: 'Configura l''accesso amministratore per l''onboarding di Collaboration [!DNL Starter] '
description: Scopri come configurare l’accesso come amministratore per Adobe Real-Time CDP Collaboration [!DNL Starter] utilizzando Admin Console in Adobe Experience Cloud.
audience: users invited to Real-Time CDP Collaboration [!DNL Starter]
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 7b5aa5e2-1238-4a0b-be20-becfe6c9e0b7
source-git-commit: db4cc34592e49254163d7db54f93238146ce72a4
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 2%

---

# Configura l&#39;accesso amministratore per l&#39;onboarding di Collaboration [!DNL Starter]

In qualità di primo utente della tua organizzazione ad accedere a Adobe Experience Platform tramite Collaboration [!DNL Starter], sei responsabile della configurazione e della gestione dell&#39;accesso per il tuo team. Per iniziare a lavorare in Real-Time CDP Collaboration, devi concederti le autorizzazioni di amministratore e utente necessarie. Leggi questa guida per scoprire come configurare l’accesso richiesto in Admin Console in modo da poter gestire le autorizzazioni per le collaborazioni nell’interfaccia Autorizzazioni.

## Prerequisiti {#prerequisites}

Prima di continuare, assicurati di disporre di:

* Ha accettato l&#39;invito del partner Collaboration. Per ulteriori informazioni sui requisiti dell&#39;invito, vedere [Collaboration [!DNL Starter] overview](../overview/starter-overview.md#prerequisites).
* Ha rivisto e firmato i termini e le condizioni di Collaboration.
* Hai ricevuto l’e-mail di benvenuto di Adobe e completato la creazione del tuo primo account.

## Configurare l’accesso {#setup-access}

Quando l&#39;account Adobe viene creato tramite il flusso di lavoro [!DNL Starter], viene assegnato automaticamente il ruolo di amministratore di sistema. Questo consente di gestire gli utenti e l’accesso ai prodotti in Admin Console. Tuttavia, non si dispone ancora dell&#39;accesso a **[!UICONTROL Autorizzazioni]**, necessario per gestire l&#39;accesso per Collaboration.

Utilizza Admin Console per concederti sia l&#39;**accesso amministratore prodotto** ad Experience Platform che l&#39;**accesso utente** ai prodotti Experience Platform per accedere alle **[!UICONTROL autorizzazioni]**.

Per ulteriori informazioni su ruoli e prodotti in Experience Cloud, consulta la [panoramica sul controllo degli accessi](../permissions/overview.md).

>[!TIP]
>
>In questa guida, un **amministratore** farà riferimento a **amministratori di sistema e di prodotto**.

### Configurare l’accesso come amministratore del prodotto {#configure-product-admin-access}

Leggere questa sezione per concedere a se stessi i privilegi di amministratore per avviare la configurazione dell&#39;accesso per Collaboration [!DNL Starter].

#### Accedere ad Admin Console {#access-admin-console}

Per iniziare, accedi a [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} con le tue credenziali. Puoi visualizzare un elenco dei prodotti disponibili nella sezione **[!UICONTROL Accesso rapido]**. Seleziona **[!UICONTROL Admin Console]**.

![Home page di Adobe Experience Cloud con Admin Console evidenziato.](../../assets/setup/starter/admin-access/select-admin-console.png){zoomable="yes"}

#### Accedere al dashboard di prodotto di Adobe Experience Platform {#access-adobe-experience-platform}

L&#39;area di lavoro [Admin Console](https://adminconsole.adobe.com/) verrà aperta in una nuova scheda. Selezionare **[!UICONTROL Adobe Experience Platform]** dall&#39;elenco **[!UICONTROL Prodotti]** in **[!UICONTROL Prodotti e servizi]**.

![Area di lavoro Admin Console con il prodotto Adobe Experience Platform evidenziato.](../../assets/setup/starter/admin-access/admin-console-workspace.png){zoomable="yes"}

#### Aggiungi amministratore prodotto {#add-product-admin}

Nel dashboard del prodotto **[!UICONTROL Adobe Experience Platform]**, passa alla scheda **[!UICONTROL Amministratori]**. Quindi seleziona **[!UICONTROL Aggiungi amministratore]**.

![Dashboard di prodotto di Adobe Experience Platform con la scheda Amministratori e l&#39;opzione Aggiungi amministratore evidenziate.](../../assets/setup/starter/admin-access/add-admin.png){zoomable="yes"}

Immetti il tuo indirizzo e-mail o nome utente nella finestra di dialogo **[!UICONTROL Aggiungi amministratori di prodotto]**, quindi seleziona l&#39;account corretto dal menu a discesa. Al termine, seleziona **[!UICONTROL Salva]**.

![Nella finestra di dialogo Aggiungi amministratori di prodotto vengono visualizzate le informazioni dell&#39;account e l&#39;opzione Salva evidenziata.](../../assets/setup/starter/admin-access/add-product-admin.png){zoomable="yes"}

Ora sei un amministratore di prodotto e puoi aggiungere utenti o altri amministratori al prodotto all’interno di Admin Console. Quindi, concedi all’utente l’accesso al prodotto Experience Platform per accedere ed eseguire funzioni in Autorizzazioni.

### Configurare l’accesso utente {#configure-user-access}

Per gestire le autorizzazioni di Collaboration, devi disporre dell&#39;**accesso utente** al prodotto oltre all&#39;accesso come amministratore. L’accesso utente può essere configurato da un amministratore di sistema o di prodotto.

>[!TIP]
>
>Se segui quanto riportato nella sezione precedente, dovresti essere già nel dashboard del prodotto **[!UICONTROL Adobe Experience Platform]** all&#39;interno di Admin Console. Da qui, passare a [aggiungi te stesso/a come utente](#add-user).

La procedura seguente illustra come iniziare a configurare l’accesso utente:

1. [Accedi ad Admin Console dalla home page di Adobe Experience Cloud](#access-admin-console).
2. [Passare alla dashboard del prodotto Adobe Experience Platform](#access-adobe-experience-platform).

#### Aggiungi utente al prodotto {#add-user}

Ora sei nel dashboard prodotto **[!UICONTROL Adobe Experience Platform]**. Passa alla scheda **[!UICONTROL Utenti]**, quindi seleziona **[!UICONTROL Aggiungi utenti]**.

![Adobe Experience Platform product dashboard with the Users tab and the Add users option highlighted.](../../assets/setup/starter/admin-access/add-user.png){zoomable="yes"}

The **[!UICONTROL Add users to this product]** dialog appears, prompting you to enter your name, user group or email address. Fill in the values, then select your account from the dropdown list.

![Add users to this product dialog displays your account&#39;s information and the Products option highlighted.](../../assets/setup/starter/admin-access/add-users-to-product.png){zoomable="yes"}

Next, select the add icon ![Add icon](../../assets/icons/plus.png) under **[!UICONTROL Products]**.

A dialog appears with a list of available [product profiles](https://helpx.adobe.com/it/enterprise/using/manage-product-profiles.html). Select **[!UICONTROL AEP-Default-All-Users]** and **[!UICONTROL Default Production All Access]**. Then select **[!UICONTROL Apply]**.

![Select product profiles dialog displays the product profiles selected and the Apply option highlighted.](../../assets/setup/starter/admin-access/select-product-profiles.png){zoomable="yes"}

Finally, select **[!UICONTROL Save]** to finish adding new user to the product.

![Add users to this product dialog with the Save option highlighted.](../../assets/setup/starter/admin-access/save-user.png){zoomable="yes"}

After you have user access, navigate back to [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}. Confirm that **[!UICONTROL Permissions]** and **[!UICONTROL Real-Time CDP Collaboration]** are available under **[!UICONTROL Quick access]**.

![Adobe Experience Cloud home screen showing both Permissions and Real-Time CDP Collaboration listed under Quick access and highlighted.](../../assets/setup/starter/admin-access/permissions-collaboration-available.png){zoomable="yes"}

>[!TIP]
>
>If **[!UICONTROL Permissions]** and **[!UICONTROL Real-Time CDP Collaboration]** don&#39;t appear in **[!UICONTROL Quick access]**, try signing out and back in.

## Passaggi successivi {#next-steps}

You now have both **administrator access** and **user access** to enter Permissions where you can define roles, assign specific permissions, and manage user access for Collaboration features and resources. For step-by-step instructions, refer to the [Permission controls guide](./starter-permission-controls.md).
