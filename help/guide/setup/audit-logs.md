---
title: Registri di audit
description: Scopri come utilizzare la funzionalità Registri di controllo in Real-Time CDP Collaboration per monitorare le attività e le modifiche degli utenti.
audience: admin
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
source-git-commit: ff22dde9730fab89481338753b1dc4a0adf1d57e
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 1%

---

# Registri di audit

{{limited-availability-release-note}}

Per aumentare la trasparenza e la visibilità delle attività eseguite nel sistema, puoi controllare le attività degli utenti per vari servizi e funzionalità sotto forma di registri di audit in Adobe Real-Time Customer Data Platform (CDP). Questi registri costituiscono un audit trail che può essere utile per risolvere eventuali problemi in Real-Time CDP Collaboration e aiutare la tua azienda a rispettare in modo efficace le politiche aziendali di gestione dei dati e i requisiti normativi.

In un certo senso, un registro di controllo comunica a *chi* ha eseguito *cosa* azione e *quando*. Ogni azione registrata contiene metadati che indicano il tipo di azione, la data e l’ora, l’ID e-mail dell’utente che l’ha eseguita e altri attributi relativi al tipo di azione.

Utilizza la funzionalità dei registri di controllo in Real-Time CDP Collaboration per monitorare le attività degli utenti e le modifiche all’interno della piattaforma. Questa funzione è integrata con il servizio di audit di Adobe Experience Platform e l’interfaccia utente per questa funzionalità risiede in Experience Platform.

![Schermata di panoramica di alto livello della funzionalità dei registri di controllo](/help/assets/setup/audit-logs/audit-logs-overview.png)

Per informazioni più complete sui registri di controllo, consulta la [documentazione dei registri di controllo di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"}.

## Accedere ai registri di audit

Puoi accedere ai registri di audit in due modi, come descritto nelle sezioni seguenti. Entrambe le opzioni visualizzano un elenco di registri di audit che acquisiscono varie attività eseguite nell’interfaccia utente di Real-Time CDP Collaboration

### Accedere ai registri di audit dall’interfaccia utente di Real-Time CDP Collaboration

1. Passa alla scheda **[!UICONTROL Attività]** nell&#39;interfaccia utente di Real-Time CDP Collaboration.
2. Seleziona il collegamento Experience Platform nel testo dell’interfaccia utente nella parte superiore della pagina.

![Accedere ai registri di controllo dall&#39;interfaccia utente di Real-Time CDP Collaboration](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Accedere ai registri di audit direttamente nell’interfaccia utente di Experience Platform

1. Passa all&#39;interfaccia utente di Adobe Experience Platform e seleziona la sezione **[!UICONTROL Audits]** dal menu a sinistra. Se non riesci a visualizzare i registri di audit, rivolgiti agli amministratori di sistema della tua organizzazione per ottenere le autorizzazioni necessarie.

![Accedere ai registri di controllo dall&#39;interfaccia utente di Experience Platform](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## Visualizzare e utilizzare i registri di audit

Per visualizzare i registri di audit:

1. Passa alla sezione **[!UICONTROL Audit]** nell&#39;interfaccia utente di Adobe Experience Platform.
2. Utilizza i filtri per restringere i registri in base ai criteri.
3. Seleziona una voce di registro per visualizzare informazioni dettagliate, tra cui la marca temporale, l’ID richiesta, i dettagli della risorsa e lo stato dell’azione.

![Registro di controllo dettagliato](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### Attività acquisite

I registri di audit acquisiscono informazioni dettagliate sulle attività degli utenti, tra cui:

* **ID utente**: l&#39;identificatore dell&#39;utente che ha eseguito l&#39;azione.
* **Azione**: tipo di azione eseguita (ad esempio creazione, aggiornamento, eliminazione).
* **Risorsa**: risorsa modificata o creata.
* **Timestamp**: l&#39;ora in cui è stata eseguita l&#39;azione.

Questi registri creano un percorso completo di tutte le attività all’interno dell’istanza Real-Time CDP Collaboration, utile per la governance dei dati e la conformità alle normative. Ulteriori informazioni sulla gestione di [registri di controllo nell&#39;interfaccia utente](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui).

### Filtrare i registri di audit

L’interfaccia utente dei registri di controllo fornisce diversi filtri per facilitare la ricerca di registri specifici:

* **Categoria**: fa riferimento al tipo di risorsa, ad esempio istanza di collaborazione, connessione, progetto.
* **Azione**: tipo di azione eseguita (ad esempio: crea, elimina, aggiorna).
* **ID richiesta**: identificatore univoco della richiesta.
* **E-mail utente**: indirizzo e-mail dell&#39;utente che ha eseguito l&#39;azione.
* **Stato**: lo stato dell&#39;azione (ad esempio: consentito, negato).
* **Intervallo date**: l&#39;intervallo di date per il quale si desidera visualizzare i registri.

Ulteriori informazioni su [filtraggio dei registri di controllo](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs).

### Esempio di utilizzo

I registri di audit vengono generati e visualizzati nell’interfaccia utente di Experience Platform audits quando esegui azioni all’interno dell’interfaccia utente di Real-Time CDP Collaboration, ad esempio la gestione dei tipi di pubblico, l’estensione degli inviti di connessione, la creazione di progetti e così via. Ad esempio, le operazioni per creare o aggiornare parti di un progetto vengono acquisite come mostrato di seguito:

![Esempio di registri di audit generati durante la creazione e l&#39;aggiornamento di parti di un progetto.](/help/assets/setup/audit-logs/create-project-audits.png)

## Vantaggi

Comprendi alcuni dei vantaggi dell’utilizzo dei registri di audit:

* **Governance dei dati**: utilizza i registri di audit per garantire che tutte le attività all&#39;interno della piattaforma siano tracciate e controllabili.
* **Conformità alle normative**: la funzione fornisce una traccia delle attività degli utenti per soddisfare i requisiti normativi.
* **Risoluzione dei problemi**: i registri di controllo consentono di identificare e risolvere i problemi fornendo registri dettagliati delle azioni dell&#39;utente.

## Riferimenti per categorie e azioni

La tabella seguente fornisce un riferimento di tutte le categorie e le azioni per Real-Time CDP Collaboration.

![Categorie disponibili evidenziate nei registri di controllo di Real-Time CDP Collaboration.](/help/assets/setup/audit-logs/available-categories.png)

| Categoria | Azioni | Descrizione |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Istanza Collaboration]** | crea, aggiorna, elimina | Gestisci gli account dell&#39;organizzazione, inclusa la creazione, l&#39;aggiornamento e l&#39;eliminazione di organizzazioni. Ulteriori informazioni sulla [configurazione delle organizzazioni](/help/guide/setup/onboard-organization.md). |
| **[!UICONTROL Invito connessione Collaboration]** | creare, aggiornare, eliminare, approvare, rifiutare | Consente di gestire gli inviti di connessione, ad esempio la creazione, l&#39;aggiornamento, l&#39;eliminazione, l&#39;approvazione e il rifiuto degli inviti. Ulteriori informazioni sugli [inviti alla connessione](/help/guide/connect/establishing-connections.md). |
| **[!UICONTROL Connessione Collaboration]** | crea, aggiorna, elimina, approva, rifiuta, richiedi approvazione | Consente di gestire le connessioni di collaborazione, tra cui la creazione, l&#39;aggiornamento, l&#39;eliminazione, l&#39;approvazione, il rifiuto e la richiesta di approvazione per le connessioni. |
| **[!UICONTROL Connessione dati Collaboration]** | crea, aggiorna, elimina | Gestisci le connessioni dati per la collaborazione al fine di importare e gestire i tipi di pubblico, tra cui la creazione, l’aggiornamento e l’eliminazione di connessioni dati. Ulteriori informazioni sulla [gestione delle connessioni dati](/help/guide/setup/manage-data-connection.md). |
| **[!UICONTROL Entità dati Collaboration]** | crea, aggiorna, elimina | Gestisci le entità dati per la collaborazione, inclusa la creazione, l’aggiornamento e l’eliminazione di entità dati. In questo contesto, le entità dati si riferiscono ai tipi di pubblico. Ulteriori informazioni sull&#39;[importazione e gestione dei tipi di pubblico](/help/guide/setup/onboard-audiences.md). |
| **[!UICONTROL Progetto Collaboration]** | crea, aggiorna, elimina | Gestisci i progetti in collaborazione, tra cui creazione, aggiornamento ed eliminazione di progetti. Ulteriori informazioni sulla gestione di [progetti](/help/guide/collaborate/manage-projects.md). |
| **[!UICONTROL Modulo Collaboration]** | crea, aggiorna, elimina | Gestisci diversi moduli all’interno dei progetti di collaborazione, inclusa la creazione, l’aggiornamento e l’eliminazione di vari moduli nell’interfaccia utente. Ad esempio, la possibilità di [condividere tipi di pubblico](/help/guide/collaborate/share.md). |

{style="table-layout:auto"}

Sfruttando la funzionalità dei registri di audit, puoi mantenere un registro chiaro e dettagliato di tutte le attività all’interno dell’istanza Real-Time CDP Collaboration, garantendo trasparenza e responsabilità.
