---
title: Gestire i ruoli tramite le autorizzazioni
description: Comprendi tutte le risorse ruolo disponibili che forniscono accesso a diversi componenti nell’interfaccia utente di Real-Time CDP Collaboration.
audience: admin
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 59cf5bf2-421b-4ebc-beab-30eafb098649
TQID: https://experienceleague.adobe.com/dB7nEQtEGG8PvCSE7eDDelH-ml2EhKOQ8ovvGXG1Ejg
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 623
ht-degree: 1%

---

# Gestire i ruoli {#manage-roles}

{{limited-availability-release-note}}

Per gestire l&#39;accesso degli utenti a diversi componenti dell&#39;interfaccia utente di Adobe Real-Time CDP Collaboration, un [amministratore](./manage-user-access.md#system-admin-gain-access) può definire e assegnare ruoli. I ruoli definiscono l&#39;accesso di un amministratore o un utente alle [risorse](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/home#permissions){target="_blank"} della tua organizzazione. Questa guida fornisce informazioni sui ruoli standard forniti in Real-Time CDP Collaboration e sulle singole autorizzazioni che è possibile assegnare ai ruoli personalizzati.

Per iniziare a gestire i ruoli, un amministratore dovrà accedere al prodotto Experience Platform. Per informazioni su come ottenere l&#39;accesso amministrativo o su come ottenere l&#39;accesso ad Experience Platform, leggere la [guida alla gestione dell&#39;accesso utente](./manage-user-access.md#manage-user-access-through-permissions).

## Ruoli standard {#standard-roles}

Sono disponibili due ruoli standard forniti che soddisfano due casi di utilizzo comuni per il controllo degli accessi. Si tratta di ruoli di &quot;sola lettura&quot;, il che significa che non possono essere personalizzati.

| Nome ruolo | Descrizione del ruolo | Autorizzazioni |
| --- | --- | --- |
| Manager Collaboration | Si tratta di un’autorizzazione di accesso completo, contenente tutte e 15 le autorizzazioni. Questo consente all’utente di leggere, creare e modificare tutti i dati. Consente inoltre di accedere alla sandbox **[!UICONTROL Prod]** in Experience Platform e di importare i tipi di pubblico in Real-Time CDP Collaboration. | Tutto dalla tabella seguente. |
| Visualizzatori Collaboration | Questa è un’autorizzazione di accesso in sola lettura. Un utente può leggere e individuare dati, attività, connessioni e altro ancora. Consente inoltre di accedere alla sandbox **[!UICONTROL Prod]** in Experience Platform e di importare i tipi di pubblico in Real-Time CDP Collaboration. | Tutte le autorizzazioni di lettura dalla tabella seguente. |

{style="table-layout:auto"}

## Creare ruoli di accesso specifici {#specific-access-roles}

È probabile che tu voglia creare ruoli aggiuntivi per fornire diversi livelli di accesso a utenti diversi. Durante la creazione di ruoli, puoi gestire diversi livelli di accesso selezionando autorizzazioni specifiche all&#39;interno della risorsa **[!UICONTROL Collaborazioni]**. Per informazioni su come creare e gestire i ruoli, consulta la guida [ruoli](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/roles#create-new-role){target="_blank"}.

>[!NOTE]
> Per accedere a Collaboration, un utente deve avere accesso alla sandbox **[!UICONTROL Prod]** in Adobe Experience Platform. Per concedere a un utente l&#39;accesso a questa sandbox, è necessario assegnarlo a un ruolo contenente l&#39;autorizzazione **[!UICONTROL Prod]** nella risorsa **[!UICONTROL Sandbox]**.

Di seguito è riportato un elenco delle autorizzazioni disponibili all&#39;interno della risorsa Collaborazioni:

| Autorizzazione di alto livello | Descrizione |
| --- | --- |
| Gestire le istanze Collaboration | Visualizzare, creare, aggiornare ed eliminare le istanze di collaborazione di un&#39;organizzazione. Scopri le istanze di collaborazione di altre organizzazioni. |
| Leggi istanze Collaboration | Leggi le istanze di collaborazione di un’organizzazione e scopri le istanze di collaborazione di altre organizzazioni. |
| Gestisci inviti di connessione | Visualizzare, creare ed eliminare gli inviti di connessione avviati dall&#39;organizzazione. Accetta e rifiuta l’invito alla connessione avviato da altre organizzazioni. |
| Leggi inviti di connessione | Visualizza inviti di connessione. |
| Gestire le connessioni Collaboration | Un collaboratore può visualizzare, creare e aggiornare le impostazioni, nonché inviare ed eliminare connessioni. |
| Leggi connessioni Collaboration | Visualizza connessioni. |
| Gestire i dati sul pubblico | Eseguire l’onboarding e individuare i tipi di pubblico. Aggiorna i tipi di pubblico pubblici, privati e personalizzati e gestisci le impostazioni dei metadati di Inventario pubblico. |
| Leggi dati pubblico | Leggi e individua i tipi di pubblico. |
| Gestire i dati di misurazione | Integrare, aggiornare ed eliminare i dati di misurazione. |
| Leggi dati di misurazione | Leggi i dati di misurazione. |
| Gestisci progetti | Visualizza, crea, aggiorna ed elimina progetti per qualsiasi attività di individuazione, attivazione e misurazione. |
| Leggi progetti | Visualizza i progetti per qualsiasi attività di individuazione, attivazione e misurazione. |
| Attività di lettura utente | Attività di lettura degli utenti. |
| Esporta attività utente | Esporta attività utente. |
| Leggi Monitoraggio crediti Collaboration | Monitoraggio del credito a livello di organizzazione e istanza. |

{style="table-layout:auto"}

## Passaggi successivi

Dopo aver creato i ruoli che definiscono l&#39;accesso a Collaboration, devi [assegnare i ruoli](./manage-user-access.md#assign-a-role) ad amministratori e utenti. Per una panoramica completa sulla gestione dei ruoli, fare riferimento alla [guida alla gestione delle autorizzazioni per un ruolo](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/permissions).
