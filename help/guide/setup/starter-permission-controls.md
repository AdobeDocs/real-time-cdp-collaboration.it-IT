---
title: 'Configura i controlli delle autorizzazioni per l''onboarding di Collaboration [!DNL Starter] '
description: Scopri come configurare le autorizzazioni per Adobe Real-Time CDP Collaboration [!DNL Starter] utilizzando le autorizzazioni in Adobe Experience Cloud.
audience: users invited to Real-Time CDP Collaboration [!DNL Starter]
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 4e50b6cc-58f7-4a0c-8b6d-f5aa4f092e9f
source-git-commit: 147fd5847bc5074e4b4f8a05a9a1c3afc089be56
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 2%

---

# Configura i controlli delle autorizzazioni per l&#39;onboarding di Collaboration [!DNL Starter]

Dopo aver impostato l’accesso amministratore e utente ai prodotti Adobe Experience Platform, devi assegnare a te stesso i ruoli con le autorizzazioni appropriate per Real-Time CDP Collaboration. Leggi questa guida per scoprire come aggiungere i ruoli giusti al tuo account tramite l’interfaccia Autorizzazioni di Experience Cloud, per poter accedere e gestire l’accesso degli utenti alle funzioni di Collaboration.

Per informazioni dettagliate sui ruoli standard e sulle autorizzazioni disponibili inclusi nella risorsa Collaboration, consulta [guida alla gestione dei ruoli](../permissions/manage-roles.md).

## Prerequisiti {#prerequisites}

Assicurati di disporre sia di **privilegi di amministratore** che di **accesso utente** al prodotto Adobe Experience Platform. Se non hai già impostato questi livelli di accesso, consulta la [guida all&#39;accesso per gli amministratori](./starter-admin-access.md) per istruzioni dettagliate.

## Impostare le autorizzazioni {#setup-permissions}

Segui i passaggi seguenti per configurare le autorizzazioni necessarie per Collaboration. Accedi innanzitutto a [Adobe Experience Cloud](https://experience.adobe.com/) con le credenziali.

### Autorizzazioni di accesso {#access-permissions}

Dopo aver effettuato l&#39;accesso, passa alla sezione **[!UICONTROL Accesso rapido]** e seleziona **[!UICONTROL Autorizzazioni]**. Verrà aperto il dashboard Autorizzazioni, in cui è possibile assegnare i ruoli necessari.

![Home page di Experience Cloud con autorizzazioni evidenziate nella sezione Accesso rapido.](../../assets/setup/starter/access-permissions.png){zoomable="yes"}

### Seleziona un utente {#select-user}

Nel dashboard **[!UICONTROL Autorizzazioni]**, seleziona **[!UICONTROL Utenti]** dal pannello a sinistra. Quindi seleziona il tuo account dalla tabella Utenti.

>[!NOTE]
>
> Se sei il primo utente della tua organizzazione ad accedere ad Experience Platform, potresti essere l&#39;unico utente elencato nella tabella **Utenti**. Per invitare altri membri del team, seguire i passaggi descritti nella [guida alla configurazione dell&#39;accesso utente](../permissions/manage-user-access.md#administrators-configure-user-access-to-experience-platform).

![Nel dashboard Autorizzazioni viene visualizzata la tabella Utenti con un account utente evidenziato.](../../assets/setup/starter/select-user.png){zoomable="yes"}

### Assegna ruoli {#assign-roles}

Nell&#39;area di lavoro **[!UICONTROL Utente]** corrispondente, passa alla scheda **[!UICONTROL Ruoli]**. Then select **[!UICONTROL Add Roles]**.

![Nell&#39;area di lavoro Utente corrispondente viene visualizzata la scheda Ruoli con l&#39;opzione Aggiungi ruoli evidenziata.](../../assets/setup/starter/add-roles.png){zoomable="yes"}

The **[!UICONTROL Add Roles]** dialog appears with a table of available roles. Ogni riga della tabella rappresenta un ruolo con le seguenti informazioni:

| **Colonna** | **Descrizione** |
|---------------|--------------------------------------------------------|
| **Nome** | The name of the role. |
| **Descrizione** | Breve riepilogo che illustra la funzione del ruolo. I ruoli di sola lettura non possono essere personalizzati. |
| **Sandbox** | Specifies which sandboxes (for example, `Prod`) the role provides access to. |
| **Modified** | Data dell&#39;ultimo aggiornamento del ruolo. |

{style="table-layout:auto"}

Per una panoramica approfondita di un ruolo specifico e delle relative autorizzazioni, vedere la [Guida alla gestione delle autorizzazioni per un ruolo](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/permissions).

Review the information and select the roles you want to assign to your account. Al termine, selezionare **[!UICONTROL Salva]**.

![Add Roles dialog displays the roles selected and the Save option highlighted.](../../assets/setup/starter/add-roles-dialog.png){zoomable="yes"}

A confirmation dialog confirms that new roles were successfully added.

Per verificare che le autorizzazioni siano configurate correttamente, tornare alla home page di [Experience Cloud](https://experience.adobe.com/). Select **[!UICONTROL Real-Time CDP Collaboration]** within **[!UICONTROL Quick access]**. Dovresti poter accedere all&#39;area di lavoro di Collaboration e iniziare a utilizzare le funzionalità disponibili per il tuo account [!DNL Starter].

## Passaggi successivi {#next-steps}

Una volta configurate le autorizzazioni, puoi accedere a Collaboration. Successivamente, è possibile:

* [Creare ruoli personalizzati con autorizzazioni specifiche per gestire diversi livelli di accesso](../permissions/manage-roles.md#create-specific-access-roles).
* [Assegnare più utenti a un ruolo nelle autorizzazioni](../permissions/manage-user-access.md#assign-a-role).
* [Configura l&#39;account Collaboration e stabilisci connessioni con il tuo collaboratore](../overview/starter-overview.md#set-up-connections).
* [Ulteriori informazioni sull&#39;utilizzo e il consumo del credito in Collaboration [!DNL Starter]](./starter-credit-usage.md).

Per una panoramica completa di Real-Time CDP Collaboration e delle sue funzionalità chiave, leggere la [guida alla panoramica](../home.md).
