---
title: Configurare e gestire l’account
description: Scopri come configurare e gestire vari aspetti dell’account in Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 18%

---

# Configurare e gestire l’account

{{limited-availability-release-note}}

Scopri come impostare l’account in Real-Time CDP Collaboration per prepararti alle connessioni con altri collaboratori. Questa guida descrive la configurazione iniziale dell’account, inclusa l’aggiunta di dettagli sull’account, la selezione delle chiavi di corrispondenza e la gestione delle impostazioni dell’account.

![L&#39;area di lavoro di installazione visualizza un account configurato.](/help/assets/setup/manage-account/my-account.png){zoomable="yes"}

## Configurare l’account {#set-up-account}

La prima volta che accedi a Collaboration ti viene richiesto di configurare l’account. Si tratta di un processo una tantum che consente di configurare i dettagli dell’account e le chiavi di corrispondenza. Se questo è il primo account della tua organizzazione, sarai indirizzato immediatamente attraverso il processo di onboarding, a partire dalla configurazione di [dettagli account](#set-up-details).

Per aggiungere altre organizzazioni, passa a **[!UICONTROL Configurazione]** nella barra a sinistra e seleziona l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) nell&#39;angolo superiore destro. Selezionare **[!UICONTROL Account]**.

![Area di lavoro di installazione con la scheda Account personale e l&#39;opzione Account evidenziate.](/help/assets/setup/manage-account/add-new-account.png){zoomable="yes"}

### Configurare i dettagli {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="E-mail di contatto"
>abstract="Fornisci un’e-mail basata su team o ruolo, ad esempio **collaboration@yourcompany.com**. Non utilizzare indirizzi e-mail personali o individuali."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="Codice di connessione"
>abstract="Il codice di connessione è un identificatore univoco per il tuo account. Viene utilizzato per stabilire connessioni con altri collaboratori in Real-Time CDP Collaboration."

Per iniziare a configurare l&#39;account, devi prima impostare i dettagli dell&#39;account. È necessario aggiungere le seguenti informazioni:

* Aggiungi un **[!UICONTROL nome account]** che rappresenti chiaramente il tuo marchio.
* Aggiungi una **[!UICONTROL Descrizione]** del tuo marchio. Questo è facoltativo, ma aiuta gli altri collaboratori a comprendere meglio il tuo marchio.
* Seleziona il tuo **[!UICONTROL Ruolo]**. È possibile selezionare tra **[!UICONTROL Inserzionista]** e **[!UICONTROL Editore]**. Leggi la guida [roles](/help/guide/overview/roles.md) per vedere somiglianze e leggere differenze nel flusso di lavoro tra i due tipi di ruolo account.
<!-- The above will need to be updated when I update things for B2B -->
* Seleziona **[!UICONTROL Settore]** per il tuo account. Alcuni esempi includono **[!UICONTROL Retail]**, **[!UICONTROL Telecomunicazioni]** o **[!UICONTROL Servizi finanziari]**.
* L&#39;**[!UICONTROL Area]** viene impostata automaticamente in base al tuo account Adobe Experience Cloud. Questo non può essere modificato in alcun momento.
* Aggiungi un **[!UICONTROL indirizzo e-mail di contatto]** per il tuo account. Deve essere un indirizzo e-mail basato su team o ruolo. Gli indirizzi e-mail personali non devono essere forniti.
* Carica un **[!UICONTROL Logo]** per il tuo account. Attualmente, sono supportate le immagini di tipo SVG. Questo è facoltativo, ma il caricamento di un logo aiuta a rappresentare visivamente il tuo marchio nell’interfaccia di Collaboration
* Seleziona un&#39;immagine per l&#39;immagine di intestazione dell&#39;account.

>[!NOTE]
>
>Anche se puoi modificare la maggior parte di questi dettagli in qualsiasi momento, il **[!UICONTROL Ruolo]** non è modificabile dopo la configurazione iniziale. Al termine, utilizza **[!UICONTROL Avanti]** per passare alla pagina successiva e selezionare le chiavi di corrispondenza desiderate che la tua organizzazione utilizzerà.

![L&#39;area di lavoro Configura account con la sezione Dettagli visualizzata e l&#39;opzione Successivo evidenziata.](/help/assets/setup/manage-account/add-account-details.png){zoomable="yes"}

### Configurare le chiavi di corrispondenza {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Chiavi di corrispondenza"
>abstract="Le chiavi di corrispondenza sono identificatori utilizzati per riconciliare i membri tra tipi di pubblico di diverse origini dati. Includi tutte le chiavi di corrispondenza utilizzabili dal tuo brand."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="ID persone di prime parti"
>abstract="Gli ID di persone di prime parti, come indirizzi e-mail con hash o numeri di telefono, sono direttamente collegati a un singolo profilo. Gli ID attualmente supportati sono e-mail con hash e numeri di telefono."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="ID dispositivo di prime parti"
>abstract="Gli ID dispositivo di prime parti, come ECID o indirizzi IP, sono direttamente collegati ai dispositivi, che possono essere condivisi tra più persone. IPv4 è l’unico ID dispositivo di prime parti attualmente supportato."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="ID partner supportati"
>abstract="Gli ID partner associati ai profili consentono di espandere la portata a un determinato profilo."

>[!IMPORTANT]
>
>Le chiavi di corrispondenza selezionate durante la configurazione dell&#39;account determineranno le chiavi di corrispondenza disponibili per le connessioni create con altri collaboratori. Anche se è possibile rimuovere le chiavi di corrispondenza durante la configurazione della connessione, non è possibile aggiungere nuove chiavi di corrispondenza. È importante selezionare **tutte** le chiavi di corrispondenza che intendi utilizzare nelle campagne future durante la configurazione dell&#39;account.

Le chiavi di corrispondenza, come indirizzi e-mail, ID dispositivo o ID cliente, aiutano i collaboratori a lavorare insieme consentendo una sincronizzazione dei dati accurata e incentrata sulla privacy, consentendo un targeting e una misurazione più precisi del pubblico.

![Diapositiva con gli identificatori disponibili per la prima versione di Collaboration.](/help/assets/setup/manage-account/available-identifiers.png)

<!-- Eventually replace this image above to match branding better. -->

Seleziona le chiavi di corrispondenza da utilizzare per la riconciliazione dei profili di pubblico. Includi tutte le chiavi di corrispondenza utilizzabili. Pianifica per il futuro e seleziona le chiavi di corrispondenza che prevedi di utilizzare nelle campagne future. Se in un secondo momento dovrai selezionare altre chiavi di corrispondenza per il tuo account, potrai farlo nel flusso di lavoro [modifica account](#edit-account).

Seleziona fino a cinque chiavi di corrispondenza che intendi utilizzare. Successivamente, quando si impostano le connessioni, è possibile rimuovere le chiavi di corrispondenza indesiderate, ma non aggiungerne di nuove.

Esistono tre tipi di chiavi di corrispondenza disponibili:

* ID persone di prime parti
* ID dispositivo di prime parti
* ID partner

>[!IMPORTANT]
>
>Attualmente, l’unica chiave di corrispondenza supportata è l’e-mail con hash.

Al termine, seleziona **[!UICONTROL Completa]** per completare il flusso di lavoro di configurazione dell&#39;organizzazione.

![Viene visualizzata la sezione Imposta area di lavoro organizzazione con chiavi corrispondenti.](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Modifica account {#edit-account}

Dopo aver configurato l’account, puoi modificarne alcuni aspetti e dettagli in qualsiasi momento. Per modificare l&#39;account, selezionare **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Account personale]** dell&#39;area di lavoro **[!UICONTROL Configurazione]**.

![Area di lavoro di installazione con la scheda Account personale e l&#39;opzione Modifica evidenziate.](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

Ora puoi modificare i dettagli del tuo account, ad eccezione del **[!UICONTROL Ruolo]**. Tieni presente che l’area geografica viene impostata automaticamente in base al tuo account Adobe Experience Cloud e non può essere modificata in alcun momento.

![Finestra di dialogo Modifica dettagli account.](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

Puoi anche aggiornare i codici di corrispondenza selezionati inizialmente al momento dell’onboarding dell’organizzazione. Seleziona **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Chiavi corrispondenti]** per aggiungere altre chiavi di corrispondenza desiderate.

![L&#39;area di lavoro del programma di installazione con l&#39;opzione Modifica evidenziata nella sezione delle chiavi di corrispondenza dell&#39;account.](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

## Passaggi successivi

Dopo aver configurato gli account, sei pronto per [generare tipi di pubblico](/help/guide/setup/onboard-audiences.md) in Real-Time CDP Collaboration.
