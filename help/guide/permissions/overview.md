---
title: Panoramica sul controllo degli accessi
description: Scopri come accedere ad Adobe Real-Time Customer Data Platform (CDP) Collaboration.
audience: admin
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: af48f5ea-8258-42a6-a39e-f4a4ca5b4a69
source-git-commit: 608706d00124372ac59209478ab551a3a6ce0226
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 2%

---

# Panoramica sul controllo degli accessi

{{limited-availability-release-note}}

>[!IMPORTANT]
>
> Se sei un utente finale che desidera accedere ad Adobe Real-Time CDP Collaboration, rivolgiti al tuo amministratore di sistema o di prodotto per verificare se è disponibile l’accesso. Se non sai chi sia l’amministratore di sistema, contatta il tuo rappresentante Adobe.

Il controllo degli accessi per Adobe Real-Time CDP Collaboration viene fornito tramite Admin Console e le autorizzazioni in [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}. In questa guida imparerai a fornire l’accesso a te stesso o ad altri membri del tuo team, a seconda del caso d’uso.

## Gerarchia di controllo di accesso {#hierarchy}

Per configurare il controllo degli accessi a Collaboration, **è necessario** disporre dei privilegi di amministratore di sistema o di prodotto. Un amministratore di sistema non ha restrizioni e viene fornito durante il processo di onboarding. Nel frattempo, un amministratore di prodotto può fornire funzioni amministrative per tutti i prodotti a cui è stato assegnato. Un amministratore di sistema deve concedere a un amministratore di prodotto l’accesso amministrativo e ai prodotti.

Queste guide descrivono come configurare l’accesso per gli amministratori di sistema, gli amministratori di prodotto e gli utenti finali. Fai riferimento alla tabella seguente per comprendere la differenza chiave tra i ruoli.

| Ruolo | Descrizione |
| --- | --- | 
| Amministratore di sistema | L’utente con privilegi avanzati per l’organizzazione. Possono eseguire tutte le attività amministrative nell’Admin Console e disporre delle autorizzazioni necessarie per delegare funzioni amministrative ad altri utenti. |
| Amministratore del prodotto | Amministra i prodotti loro assegnati e tutte le funzioni amministrative associate, ad esempio l’aggiunta di utenti alle organizzazioni, l’aggiunta o la rimozione di utenti dai profili di prodotto e l’aggiunta o la rimozione di altri amministratori di prodotto da un prodotto. |
| Utente finale | Gli utenti dell’organizzazione che utilizzano i prodotti. |

{style="table-layout:auto"}

Per ulteriori informazioni sui ruoli amministrativi, visita il [Centro assistenza Adobe](https://helpx.adobe.com/it/enterprise/using/admin-roles.html).

>[!TIP]
>
>L&#39;utilizzo di **amministratori** in queste guide farà riferimento a **amministratori di sistema e di prodotto**.

## Prodotti aggiuntivi {#products}

Prima di poter concedere l&#39;accesso a Collaboration, devi accedere a più prodotti, a seconda del [caso d&#39;uso](#use-cases). Le guide per il controllo degli accessi possono essere utilizzate con più interfacce utente man mano che si procede, ognuna delle quali può servire a uno scopo specifico all&#39;interno del processo di configurazione degli accessi. Consulta la tabella seguente per informazioni più approfondite sulle finalità di utilizzo dei singoli prodotti.

| Prodotto | Usa |
| --- | --- |
| [Admin Console](https://adminconsole.adobe.com/) | Gli amministratori utilizzano questa funzione per assegnare agli utenti l’accesso ai prodotti e/o agli amministratori. |
| [Autorizzazioni](https://experience.adobe.com/) | Gli amministratori utilizzano questa funzione per assegnare ruoli di amministratori o utenti finali. |
| [Experience Platform](https://platform.adobe.com/) | Gli amministratori e gli utenti finali devono avere accesso al prodotto Experience Platform per assegnarli ai ruoli. |

## Dove iniziare {#use-cases}

Ora che conosci meglio i ruoli utente e amministrativo, nonché i diversi prodotti Experience Cloud, puoi iniziare a dare accesso a Collaboration. Ci sono due fattori principali che influenzano i passaggi da intraprendere:

- se si sta assegnando l&#39;accesso amministratore o utente finale
- se gli utenti hanno già accesso al prodotto Experience Platform

Consulta il grafico seguente per determinare chi è necessario per configurare i privilegi e dove iniziare in base al caso di utilizzo del controllo degli accessi. **Segui l&#39;esercitazione fino alla fine della guida dal punto di partenza.**

>[!TIP]
>
> Per utente con privilegi avanzati si intende il livello massimo di accesso che l&#39;amministratore di sistema può ottenere. Un utente con privilegi avanzati può eseguire tutte le attività amministrative e le funzionalità utente. Un amministratore di sistema non dispone di funzionalità di prodotto pronte all’uso e deve fornire a se stesso l’accesso appropriato, come illustrato nel grafico seguente.

| Caso d’uso | Ruolo richiesto | Dove iniziare |
| --- | --- | --- | 
| Utente privilegiato senza accesso al prodotto Experience Platform esistente. | Un amministratore di sistema. | [Configurare l&#39;accesso amministratore del prodotto](./manage-user-access.md#admin-access) |
| Utente con privilegi avanzati per un amministratore di sistema Experience Platform esistente **con** accesso all&#39;interfaccia utente di Experience Platform. | Un amministratore di sistema. | [Configura accesso a Collaboration](./manage-user-access.md#RTCDP-collab-access) |
| Utente con privilegi avanzati per un amministratore di sistema Experience Platform esistente **senza** accesso all&#39;interfaccia utente di Experience Platform. | Un amministratore di sistema. | [Configurare l&#39;accesso amministratore del prodotto](./manage-user-access.md#admin-access) |
| Privilegi di amministratore di prodotto e accesso a Collaboration per un nuovo amministratore di prodotto. | Un amministratore di sistema. | [Configurare l&#39;accesso amministratore del prodotto](./manage-user-access.md#admin-access) |
| Accesso a Collaboration per un amministratore di prodotto Experience Platform esistente **con** accesso all&#39;interfaccia utente di Experience Platform. | Un amministratore di sistema o di prodotto. | [Configura accesso a Collaboration](./manage-user-access.md#RTCDP-collab-access) |
| Accesso a Collaboration per un amministratore di prodotto Experience Platform esistente **senza** accesso all&#39;interfaccia utente di Experience Platform. | Un amministratore di sistema o di prodotto. | [Configura accesso utente](./manage-user-access.md#user-access) |
| Accesso a Collaboration per un nuovo utente finale. | Un amministratore di sistema o di prodotto. | [Configura accesso utente](./manage-user-access.md#user-access) |
| Accesso Collaboration per un utente esistente con accesso Experience Platform. | Un amministratore di sistema o di prodotto. | [Configura accesso a Collaboration](./manage-user-access.md#RTCDP-collab-access) |

{style="table-layout:auto"}

## Autorizzazioni aggiuntive

Dopo aver ottenuto l’accesso a Collaboration, potrebbe essere necessario disporre di alcune autorizzazioni Experience Platform aggiuntive per funzionalità specifiche.

### Origine pubblico {#audience-sourcing}

Prima di poter iniziare a inviare tipi di pubblico ai collaboratori, è necessario assegnarli a Collaboration. Attualmente, l’unica connessione dati self-service supportata per l’importazione dei tipi di pubblico è Experience Platform. Per iniziare, agli utenti che gestiscono l&#39;onboarding del pubblico dovrà essere assegnato un ruolo contenente le seguenti **[!UICONTROL autorizzazioni per le risorse di gestione dei profili]**:

| Autorizzazione | Descrizione |
| ---- | ---- |
| [!UICONTROL Visualizza segmenti] | Consente all’utente di visualizzare l’elenco dei tipi di pubblico disponibili in una sandbox. |
| [!UICONTROL Visualizza profili] | Consente all&#39;utente di visualizzare i campi disponibili per la mappatura ai campi di collaborazione. |

Di seguito è riportato un ruolo di esempio con le autorizzazioni di cui sopra aggiunte. Per ulteriori informazioni sulla creazione o l&#39;assegnazione di ruoli, fare riferimento alla guida [gestione ruoli](./manage-roles.md).

![L&#39;area di lavoro delle risorse in Autorizzazioni con le autorizzazioni Visualizza segmenti e Visualizza profili aggiunte alla risorsa Gestione profili.](../../assets/permissions/sample-audience-role.png)

>[!NOTE]
>
>Gli utenti possono lavorare con i tipi di pubblico in Collaboration dopo che sono stati acquistati senza alcuna delle autorizzazioni di cui sopra.

## Passaggi successivi

Una volta stabilito da dove iniziare, segui il collegamento del caso d’uso per iniziare a configurare l’accesso. Se desideri ulteriori informazioni sulla configurazione dell&#39;accesso a Collaboration come amministratore oltre a questi casi d&#39;uso, consulta la [guida alla gestione dell&#39;accesso utente](manage-user-access.md). Per informazioni sui ruoli e sulla loro parte nella configurazione dell&#39;accesso ai vari componenti di Collaboration, consulta la guida [gestisci ruoli](manage-roles.md).
