---
title: Registri di audit
description: Scopri come utilizzare la funzionalità Registri di controllo in Real-Time CDP Collaboration per monitorare le attività e le modifiche degli utenti.
audience: admin
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 1%

---

# Registri di audit

{{limited-availability-release-note}}

Per aumentare la trasparenza e la visibilità delle attività eseguite nel sistema, puoi controllare le attività degli utenti per vari servizi e funzionalità sotto forma di registri di audit in Adobe Experience Platform. Questi registri costituiscono un audit trail che può essere utile per risolvere i problemi in Adobe Real-Time CDP Collaboration e aiutare la tua azienda a rispettare in modo efficace le politiche aziendali di gestione dei dati e i requisiti normativi.

In un certo senso, un registro di controllo comunica a *chi* ha eseguito *cosa* azione e *quando*. Ogni azione registrata contiene metadati che indicano il tipo di azione, la data e l’ora, l’ID e-mail dell’utente che l’ha eseguita e altri attributi relativi al tipo di azione.

Utilizza la funzionalità dei registri di controllo in Collaboration per monitorare le attività degli utenti e le modifiche all’interno della piattaforma. Questa funzione è integrata con il servizio di audit di Experience Platform e l’interfaccia utente per questa funzionalità risiede in Experience Platform.

![Schermata di panoramica di alto livello della funzionalità dei registri di controllo.](/help/assets/setup/audit-logs/audit-logs-overview.png)

Per informazioni più complete sui registri di audit, consulta la [documentazione dei registri di audit di Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"}.

## Accedere ai registri di audit

Puoi accedere ai registri di audit in due modi, come descritto nelle sezioni seguenti. Entrambe le opzioni visualizzano un elenco di registri di audit che acquisiscono varie attività eseguite all’interno di Collaboration.

### Accedere ai registri di audit dall’interfaccia utente di Collaboration

1. Passa alla scheda **[!UICONTROL Attività]** nell&#39;area di lavoro **[!UICONTROL Configurazione]** in Collaboration.
2. Seleziona il collegamento Experience Platform nel testo nella parte superiore della pagina.

![Accedere ai registri di controllo dalla scheda Attività personali in Collaboration.](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Accedere ai registri di audit direttamente nell’interfaccia utente di Experience Platform

1. Passa a [Experience Platform](https://platform.adobe.com/) e seleziona la sezione **[!UICONTROL Audits]** dal menu a sinistra. Se non riesci a visualizzare i registri di audit, rivolgiti agli amministratori di sistema della tua organizzazione per ottenere le autorizzazioni necessarie.

![Accedere ai registri di controllo da Experience Platform.](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## Visualizzare e utilizzare i registri di audit

Per visualizzare i registri di audit:

1. Passa alla sezione **[!UICONTROL Audit]** in Experience Platform.
2. Utilizza i [filtri](#filter-audit-logs) per limitare i registri in base ai criteri.
3. Seleziona una voce di registro per visualizzare informazioni dettagliate, tra cui la marca temporale, l’ID richiesta, i dettagli della risorsa e lo stato dell’azione.

![Registro di controllo dettagliato](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### Attività acquisite

I registri di audit acquisiscono informazioni dettagliate sulle attività degli utenti, tra cui:

* **Timestamp**: la data e l&#39;ora esatte dell&#39;azione eseguite in un mese/giorno/anno, ora:minute, formato AM/PM.
* **Nome risorsa**: nome della risorsa su cui è stata eseguita l&#39;azione.
* **Categoria**: tipo di risorsa su cui è stata eseguita l&#39;azione.
* **Azione**: azione specifica eseguita, ad esempio creazione o eliminazione.
* **Utente**: indirizzo e-mail dell&#39;utente che ha eseguito l&#39;azione.

Questi registri creano un percorso completo di tutte le attività all’interno dell’istanza Collaboration, utile per la governance dei dati e la conformità alle normative. Ulteriori informazioni sulla gestione di [registri di controllo nell&#39;interfaccia utente](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui).

### Filtrare i registri di audit {#filter-audit-logs}

L’interfaccia utente dei registri di controllo fornisce diversi filtri per facilitare la ricerca di registri specifici:

* **Categoria**: tipo di risorsa su cui è stata eseguita l&#39;azione, ad esempio Istanza di Collaboration o Invito alla connessione Collaboration.
* **Azione**: tipo di azione eseguita. Le azioni disponibili dipendono dalla categoria selezionata. Ad esempio, le azioni per Istanza di Collaboration includono creazione, aggiornamento ed eliminazione.
* **ID richiesta**: identificatore univoco della richiesta.
* **Utente**: indirizzo e-mail dell&#39;utente che ha eseguito l&#39;azione.
* **Stato**: lo stato dell&#39;azione, ad esempio consenti o nega.
* **Intervallo date**: l&#39;intervallo di date per il quale si desidera visualizzare i registri.

Ulteriori informazioni su [filtraggio dei registri di controllo](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs).

## Vantaggi

I registri di audit offrono diversi vantaggi alle organizzazioni che utilizzano Collaboration:

* **Governance dei dati**: utilizza i registri di audit per garantire che tutte le attività all&#39;interno della piattaforma siano tracciate e controllabili.
* **Conformità alle normative**: la funzione fornisce una traccia delle attività degli utenti per soddisfare i requisiti normativi.
* **Risoluzione dei problemi**: i registri di controllo consentono di identificare e risolvere i problemi fornendo registri dettagliati delle azioni dell&#39;utente.

## Riferimenti per categorie e azioni

La tabella seguente fornisce un riferimento di tutte le categorie e le azioni per Real-Time CDP Collaboration.

![Categorie disponibili evidenziate nei registri di controllo di Real-Time CDP Collaboration.](/help/assets/setup/audit-logs/available-categories.png)

| Categoria | Azioni | Descrizione |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Istanza Collaboration]** | crea, aggiorna, elimina | Gestisci gli account, tra cui creazione, aggiornamento ed eliminazione. Per ulteriori informazioni, consulta la [guida alla configurazione degli account](/help/guide/setup/onboard-account.md). |
| **[!UICONTROL Invito connessione Collaboration]** | creare, aggiornare, eliminare, approvare, rifiutare | Consente di gestire gli inviti di connessione, ad esempio la creazione, l&#39;aggiornamento, l&#39;eliminazione, l&#39;approvazione e il rifiuto degli inviti. Per ulteriori informazioni, leggere la guida [stabilire connessioni](/help/guide/connect/establishing-connections.md). |
| **[!UICONTROL Connessione Collaboration]** | crea, aggiorna, elimina, approva, rifiuta, richiedi approvazione | Gestisci le connessioni, ad esempio creando, aggiornando, eliminando, approvando, rifiutando e richiedendo l&#39;approvazione per le connessioni. |
| **[!UICONTROL Connessione dati Collaboration]** | crea, aggiorna, elimina | Gestisci le connessioni dati da dove origini e gestisci i tipi di pubblico, incluse la creazione, l’aggiornamento e l’eliminazione delle connessioni dati. Per ulteriori informazioni, leggere la [guida alla gestione delle connessioni dati](/help/guide/setup/manage-data-connection.md). |
| **[!UICONTROL Entità dati Collaboration]** | crea, aggiorna, elimina | Gestisci le entità dati per Collaboration, inclusa la creazione, l’aggiornamento e l’eliminazione. In questo contesto, le entità dati si riferiscono ai tipi di pubblico. Per ulteriori informazioni, consulta la guida [sourcing e gestione dei tipi di pubblico](/help/guide/setup/onboard-audiences.md). |
| **[!UICONTROL Progetto Collaboration]** | crea, aggiorna, elimina | Gestisci i progetti all&#39;interno di Collaboration, inclusa la creazione, l&#39;aggiornamento e l&#39;eliminazione. Per ulteriori informazioni, leggere la guida [gestione progetti](/help/guide/collaborate/manage-projects.md). |
| **[!UICONTROL Modulo Collaboration]** | crea, aggiorna, elimina | Gestisci diversi moduli all’interno dei progetti, tra cui la creazione, l’aggiornamento e l’eliminazione di vari moduli nell’interfaccia utente. Ad esempio, la possibilità di [attivare tipi di pubblico](/help/guide/collaborate/activate.md). |

{style="table-layout:auto"}

Sfruttando la funzionalità dei registri di audit, puoi mantenere una registrazione chiara e dettagliata di tutte le attività all’interno di Collaboration, garantendo trasparenza e responsabilità.
