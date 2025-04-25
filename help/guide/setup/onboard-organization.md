---
title: Onboarding e gestione dell’organizzazione
description: Scopri come integrare e gestire vari aspetti dell’organizzazione in Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: b9aa8851799ddb492daeb13842a2cad39e84899e
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 1%

---

# Onboarding e gestione dell’organizzazione

{{limited-availability-release-note}}

Scopri come integrare la tua organizzazione in Real-Time CDP Collaboration e gestire vari aspetti dell’azienda. Questa pagina illustra i passaggi necessari per integrare un’organizzazione negli Adobi Real-Time CDP Collaboration, inclusa l’impostazione delle chiavi di corrispondenza, delle identità preferite e di altre opzioni.

![Pagina di installazione](/help/assets/setup/manage-organization/my-organization.png){zoomable="yes"}

## Configurazione iniziale dell’organizzazione

Devi prima impostare l’organizzazione e i dettagli organizzativi. Passa a **[!UICONTROL Configurazione]** nella barra a sinistra, seleziona il simbolo **+** nell&#39;angolo in alto a destra, quindi seleziona **[!UICONTROL Account]**.

>[!TIP]
>
>Dopo aver impostato un account iniziale per l’utilizzo, puoi utilizzare lo stesso flusso di lavoro per impostare account aggiuntivi all’interno della stessa organizzazione.

![Seleziona account per aggiungere una nuova organizzazione a Real-Time CDP Collaboration](/help/assets/setup/manage-organization/add-new-account.png){zoomable="yes"}

Il flusso di lavoro per configurare l’organizzazione include le due pagine seguenti:

* [Imposta dettagli](#set-up-details)
* [Configura chiavi di corrispondenza](#set-up-match-keys)

>[!IMPORTANT]
>
>Qualsiasi *chiave di corrispondenza* selezionata a livello di organizzazione verrà quindi ridotta al [livello di progetto](/help/guide/collaborate/manage-projects.md) nella collaborazione tra inserzionisti e editori. A livello di progetto, è quindi possibile rimuovere le chiavi di corrispondenza, ma è *impossibile* aggiungere altre chiavi non selezionate a livello di organizzazione in questa schermata.

### Imposta dettagli {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="E-mail di contatto"
>abstract="Fornire un&#39;e-mail basata su team o ruolo, ad esempio `collaboration@yourcompany.com`. Non utilizzare indirizzi e-mail personali o individuali."

![I passaggi relativi ai dettagli e ai casi d&#39;uso per configurare un&#39;organizzazione](/help/assets/setup/manage-organization/add-organization-details.png){zoomable="yes"}

1. Aggiungi un **[!UICONTROL nome organizzazione]** per la tua società.
2. Aggiungi una **[!UICONTROL Descrizione]** sulla tua azienda.
3. Seleziona il tuo **[!UICONTROL Ruolo aziendale]**. È possibile selezionare tra **[!UICONTROL Inserzionista]** e **[!UICONTROL Editore]**. Leggi il documento [sul flusso di lavoro end-to-end](/help/guide/end-to-end-workflow.md) per vedere somiglianze e lievi differenze nel flusso di lavoro tra i due tipi di ruolo organizzativo.
4. Seleziona il **[!UICONTROL Settore]** per la tua organizzazione. Alcuni esempi includono **[!UICONTROL Retail]**, **[!UICONTROL Telecomunicazioni]** o **[!UICONTROL Servizi finanziari]**.
5. Seleziona l&#39;**[!UICONTROL Area]** per la tua organizzazione. Nella versione corrente del prodotto, **[!UICONTROL Nord America]** è la selezione predefinita predefinita predefinita.
6. <span class="preview"> Solo editore</span>: durante la configurazione di un&#39;organizzazione di editori, è necessario leggere e confermare che gli inserzionisti potranno individuarti nel catalogo di editori.
   ![Messaggio di consenso specifico per il server di pubblicazione.](/help/assets/setup/manage-organization/publisher-specific-optin-message.png){zoomable="yes"}
7. Carica un **[!UICONTROL Logo]** per la tua azienda. Attualmente, sono supportate le immagini di tipo SVG.
8. Seleziona un&#39;immagine per l&#39;immagine dell&#39;intestazione della società.

Una volta effettuata la selezione, utilizzare **[!UICONTROL Avanti]** per passare alla pagina successiva e selezionare le chiavi di corrispondenza desiderate che l&#39;organizzazione deve utilizzare.

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
>title="ID di dispositivi di prime parti"
>abstract="Gli ID dispositivo di prime parti come ECID o indirizzi IP sono direttamente collegati ai dispositivi, che possono essere condivisi tra più individui. IPv4 è l’unico ID dispositivo di prime parti attualmente supportato."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="ID partner supportati"
>abstract="Gli ID partner associati ai profili consentono di espandere la portata a un determinato profilo."

Le chiavi di corrispondenza, come indirizzi e-mail, ID dispositivo o ID cliente, consentono agli inserzionisti e agli editori di lavorare insieme abilitando una sincronizzazione dei dati accurata e conforme alla privacy, che consente un targeting e una misurazione più precisi del pubblico.

![Diapositiva con gli identificatori disponibili per la prima versione di Real-Time CDP Collaboration.](/help/assets/setup/manage-organization/available-identifiers.png)

Seleziona le chiavi di corrispondenza che desideri utilizzare per riconciliare i membri del pubblico dell’editore e dell’inserzionista. Includi tutte le chiavi di corrispondenza utilizzabili dalla tua azienda. Pianifica per il futuro e seleziona le chiavi di corrispondenza che prevedi di utilizzare nelle campagne future per gli inserzionisti di editori. Se devi selezionare altre chiavi di corrispondenza per la tua organizzazione, puoi farlo in un secondo momento nel flusso di lavoro [modifica organizzazione](#edit-organization).

![Passaggio di selezione chiavi corrispondenti.](/help/assets/setup/manage-organization/add-organization-match-keys.png){zoomable="yes"}

Seleziona fino a cinque chiavi di corrispondenza che intendi utilizzare. Successivamente, quando si impostano le connessioni, è possibile rimuovere le chiavi di corrispondenza indesiderate, ma non aggiungerne di nuove.

Le chiavi di corrispondenza disponibili in Real-Time CDP Collaboration possono essere di tre tipi:

* ID persone di prime parti
* ID di dispositivi di prime parti
* ID partner

Le chiavi di corrispondenza disponibili per la prima versione di Real-Time CDP Collaboration sono:

* E-mail con hash

<!--

not available in the Limited GA release

* Hashed phone
* IPv4

-->

Al termine, seleziona **[!UICONTROL Completa]** per completare il flusso di lavoro di configurazione dell&#39;organizzazione.

## Modifica organizzazione {#edit-organization}

Dopo aver inizialmente configurato l’organizzazione, puoi modificarne alcuni aspetti e dettagli in qualsiasi momento. Per modificare la tua organizzazione, seleziona **[!UICONTROL Modifica]** nella visualizzazione **[!UICONTROL Organizzazione]**.

![Controllo modifica organizzazione evidenziato.](/help/assets/setup/manage-organization/edit-organization.png){zoomable="yes"}

A questo punto, è possibile aggiornare il nome, la descrizione, il logo e l&#39;immagine del profilo dell&#39;organizzazione.

![Opzioni modificabili per le organizzazioni.](/help/assets/setup/manage-organization/editable-options.png){zoomable="yes"}

Puoi anche aggiornare i codici di corrispondenza selezionati inizialmente al momento dell’onboarding dell’organizzazione, nonché la soglia minima di identità corrispondenti ai codici di corrispondenza affinché siano visibili e utilizzabili in sovrapposizioni di pubblico e altre aree di prodotto. Seleziona **[!UICONTROL Modifica]** nella scheda **[!UICONTROL Chiavi corrispondenti]** per aggiungere altre chiavi di corrispondenza desiderate o aggiornare le soglie di identità.

![Modifica chiavi di corrispondenza](/help/assets/setup/manage-organization/edit-match-keys.png){zoomable="yes"}

## Passaggi successivi

Dopo aver configurato la tua organizzazione, sei pronto per [importare tipi di pubblico](/help/guide/setup/onboard-audiences.md) in Real-Time CDP Collaboration.
