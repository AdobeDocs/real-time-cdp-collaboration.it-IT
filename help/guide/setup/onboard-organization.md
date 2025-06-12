---
title: Onboarding e gestione dell’organizzazione
description: Scopri come integrare e gestire vari aspetti dell’organizzazione in Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 860138b95abc4d6af94bbbf722cf498463570c1b
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 16%

---

# Integrare e gestire l’organizzazione

{{limited-availability-release-note}}

Scopri come integrare la tua organizzazione in Real-Time CDP Collaboration e gestire vari aspetti dell’azienda. Questa pagina illustra i passaggi necessari per integrare un’organizzazione negli Adobi Real-Time CDP Collaboration, inclusa l’impostazione delle chiavi di corrispondenza, delle identità preferite e di altre opzioni.

![L&#39;area di lavoro di configurazione dell&#39;organizzazione presenta le impostazioni correnti.](/help/assets/setup/manage-organization/my-organization.png){zoomable="yes"}

## Configurazione iniziale dell’organizzazione

Devi prima impostare l’organizzazione e i dettagli organizzativi. Se questa è la tua prima organizzazione, sarai indirizzato immediatamente attraverso il processo di onboarding, iniziando con la configurazione dei [dettagli account](#set-up-details).

Per aggiungere altre organizzazioni, passa a **[!UICONTROL Configurazione]** nella barra a sinistra e seleziona l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) nell&#39;angolo superiore destro. Selezionare **[!UICONTROL Account]**.

![Area di lavoro di installazione con l&#39;opzione Account evidenziata.](/help/assets/setup/manage-organization/add-new-account.png){zoomable="yes"}

### Configurare i dettagli {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="E-mail di contatto"
>abstract="Fornisci un’e-mail basata su team o ruolo, ad esempio `collaboration@yourcompany.com`. Non utilizzare indirizzi e-mail personali o individuali."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="Connetti codice"
>abstract="Il codice di connessione è un identificativo univoco per la tua organizzazione. Viene utilizzato per stabilire connessioni con altre organizzazioni in Real-Time CDP Collaboration."

<!-- Move the above to new section for invite on this page when its created -->

Per iniziare a effettuare l’onboarding dell’organizzazione, devi prima impostare i dettagli dell’organizzazione. È necessario aggiungere le seguenti informazioni:

* Aggiungi un **[!UICONTROL nome organizzazione]** per la tua società.
* Aggiungi una **[!UICONTROL Descrizione]** sulla tua azienda.
* Seleziona il tuo **[!UICONTROL Ruolo aziendale]**. È possibile selezionare tra **[!UICONTROL Inserzionista]** e **[!UICONTROL Editore]**. Leggi il documento [sul flusso di lavoro end-to-end](/help/guide/end-to-end-workflow.md) per vedere somiglianze e lievi differenze nel flusso di lavoro tra i due tipi di ruolo organizzativo.
* Seleziona il **[!UICONTROL Settore]** per la tua organizzazione. Alcuni esempi includono **[!UICONTROL Retail]**, **[!UICONTROL Telecomunicazioni]** o **[!UICONTROL Servizi finanziari]**.
* Seleziona l&#39;**[!UICONTROL Area]** per la tua organizzazione. Nella versione corrente del prodotto, **[!UICONTROL Nord America]** è la selezione predefinita predefinita predefinita.
* Aggiungi **[!UICONTROL E-mail di contatto]** per la tua organizzazione. Deve essere un indirizzo e-mail basato su team o ruolo. Gli indirizzi e-mail personali non devono essere forniti.
* Carica un **[!UICONTROL Logo]** per la tua azienda. Attualmente, sono supportate le immagini di tipo SVG.
* Seleziona un&#39;immagine per l&#39;immagine dell&#39;intestazione della società.

>[!NOTE]
>
>Anche se puoi modificare la maggior parte di questi dettagli in qualsiasi momento, **[!UICONTROL Role]** e **[!UICONTROL Region]** non sono modificabili dopo la configurazione iniziale.

![Viene visualizzata la sezione Imposta area di lavoro organizzazione con i dettagli.](/help/assets/setup/manage-organization/add-organization-details.png){zoomable="yes"}

Al termine, utilizza **[!UICONTROL Avanti]** per passare alla pagina successiva e selezionare le chiavi di corrispondenza desiderate che la tua organizzazione utilizzerà.

### Configurare le chiavi di corrispondenza {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Chiavi di corrispondenza"
>abstract="Le chiavi di corrispondenza sono identificatori utilizzati per riconciliare i membri tra tipi di pubblico di diverse origini dati. Includi tutte le chiavi di corrispondenza utilizzabili dalla tua azienda."

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
>Le chiavi di corrispondenza selezionate durante l&#39;impostazione dell&#39;organizzazione determineranno le chiavi di corrispondenza disponibili per le connessioni create con altre organizzazioni. Sebbene sia possibile rimuovere le chiavi di corrispondenza durante la configurazione della connessione, non è possibile aggiungerne di nuove in un secondo momento. È importante selezionare tutte le chiavi di corrispondenza che intendi utilizzare in campagne future durante la configurazione dell’organizzazione.

Le chiavi di corrispondenza, come indirizzi e-mail, ID dispositivo o ID cliente, consentono agli inserzionisti e agli editori di lavorare insieme abilitando una sincronizzazione dei dati accurata e incentrata sulla privacy, consentendo un targeting e una misurazione più precisi del pubblico.

![Diapositiva con gli identificatori disponibili per la prima versione di Real-Time CDP Collaboration.](/help/assets/setup/manage-organization/available-identifiers.png)

Seleziona le chiavi di corrispondenza che desideri utilizzare per riconciliare i membri del pubblico dell’editore e dell’inserzionista. Includi tutte le chiavi di corrispondenza utilizzabili dalla tua azienda. Pianifica per il futuro e seleziona le chiavi di corrispondenza che prevedi di utilizzare nelle campagne future per gli inserzionisti di editori. Se devi selezionare altre chiavi di corrispondenza per la tua organizzazione, puoi farlo in un secondo momento nel flusso di lavoro [modifica organizzazione](#edit-organization).

![Viene visualizzata la sezione Imposta area di lavoro organizzazione con chiavi corrispondenti.](/help/assets/setup/manage-organization/add-organization-match-keys.png){zoomable="yes"}

Seleziona fino a cinque chiavi di corrispondenza che intendi utilizzare. Successivamente, quando si impostano le connessioni, è possibile rimuovere le chiavi di corrispondenza indesiderate, ma non aggiungerne di nuove.

Le chiavi di corrispondenza disponibili in Real-Time CDP Collaboration possono essere di tre tipi:

* ID persone di prime parti
* ID dispositivo di prime parti
* ID partner

Le chiavi di corrispondenza disponibili per la prima versione di Real-Time CDP Collaboration sono:

* E-mail con hash

Al termine, seleziona **[!UICONTROL Completa]** per completare il flusso di lavoro di configurazione dell&#39;organizzazione.

## Modifica organizzazione {#edit-organization}

Dopo aver inizialmente configurato l’organizzazione, puoi modificarne alcuni aspetti e dettagli in qualsiasi momento. Per modificare l&#39;organizzazione, selezionare **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Organizzazione]** dell&#39;area di lavoro **[!UICONTROL Configurazione]**.

![Area di lavoro di installazione con le opzioni Modifica e scheda Organizzazione personale evidenziate.](/help/assets/setup/manage-organization/edit-organization.png){zoomable="yes"}

Ora puoi modificare i dettagli della tua organizzazione, ad eccezione di **[!UICONTROL Ruolo]** e **[!UICONTROL Area]**.

![Finestra di dialogo Modifica dettagli organizzazione.](/help/assets/setup/manage-organization/editable-options.png){zoomable="yes"}

Puoi anche aggiornare i codici di corrispondenza selezionati inizialmente al momento dell’onboarding dell’organizzazione. Seleziona **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Chiavi corrispondenti]** per aggiungere altre chiavi di corrispondenza desiderate.

![L&#39;area di lavoro del programma di installazione con l&#39;opzione Modifica evidenziata nella sezione delle chiavi di corrispondenza dell&#39;organizzazione.](/help/assets/setup/manage-organization/edit-match-keys.png){zoomable="yes"}

## Passaggi successivi

Dopo aver configurato la tua organizzazione, sei pronto per [importare tipi di pubblico](/help/guide/setup/onboard-audiences.md) in Real-Time CDP Collaboration.
