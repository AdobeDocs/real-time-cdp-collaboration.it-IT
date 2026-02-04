---
title: Configurare e gestire l’account
description: Scopri come configurare e gestire vari aspetti dell’account in Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 873af5b0ef5e4e0c937c540de4697ec314624669
workflow-type: tm+mt
source-wordcount: '1373'
ht-degree: 6%

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
>abstract="Le chiavi di corrispondenza sono identificatori utilizzati per riconciliare i profili di pubblico da diverse origini dati. Includi tutte le chiavi di corrispondenza utilizzabili dal tuo brand."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_setup_match_keys"
>title="chiavi di corrispondenza"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="ID persone di prime parti"
>abstract="Gli ID di persone di prime parti, come indirizzi e-mail con hash, numeri di telefono con hash o ID del sistema di gestione delle relazioni con i clienti, sono collegati direttamente a un singolo profilo."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="ID dispositivo di prime parti"
>abstract="Gli ID dispositivo di prime parti, come ECID o indirizzi IP, sono collegati direttamente a dispositivi che possono essere condivisi tra più individui."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="ID partner supportati"
>abstract="Gli ID partner sono identificatori forniti da partner esterni per la riconciliazione del pubblico. Gli ID partner non sono collegati direttamente a un singolo profilo."

![Chiavi di corrispondenza supportate.](/help/assets/setup/manage-account/match-keys.png){zoomable="yes"}

>[!IMPORTANT]
>
>Le chiavi di corrispondenza selezionate durante la configurazione dell&#39;account determineranno le chiavi di corrispondenza disponibili all&#39;interno delle connessioni. Sebbene sia possibile [rimuovere le chiavi di corrispondenza indesiderate](../connect/establishing-connections.md#connection-settings) durante la configurazione della connessione, non è possibile aggiungere le chiavi di corrispondenza dopo che è stata stabilita una connessione. È importante selezionare **tutte** le chiavi di corrispondenza che si intende utilizzare nelle campagne future durante la configurazione dell&#39;account.

Le chiavi di corrispondenza aiutano i collaboratori a collaborare, consentendo una sincronizzazione dei dati accurata e incentrata sulla privacy, consentendo un targeting e una misurazione più precisi del pubblico. Le chiavi di corrispondenza selezionate durante la configurazione dell’account determineranno quali chiavi di corrispondenza saranno disponibili nelle connessioni future. Vengono inoltre utilizzati per [mappare i campi](./onboard-audiences.md#map-fields) dalla connessione dati ai campi di destinazione in Collaboration durante l&#39;individuazione dei tipi di pubblico.

Seleziona le chiavi di corrispondenza da utilizzare per la riconciliazione dei profili di pubblico. Pianifica per il futuro e includi tutte le chiavi di corrispondenza con cui lavorare e che puoi anticipare utilizzando nelle campagne future. Se in un secondo momento dovrai selezionare altre chiavi di corrispondenza per il tuo account, potrai farlo nel flusso di lavoro [modifica account](#edit-account). Tuttavia, le eventuali chiavi di corrispondenza aggiunte dopo la configurazione iniziale non saranno disponibili per l’utilizzo nelle connessioni esistenti.

#### Chiavi di corrispondenza supportate {#supported-match-keys}

Collaboration supporta tre tipi di chiavi di corrispondenza: ID persone di prime parti, ID dispositivo di prime parti e ID partner. Tutte le chiavi di corrispondenza devono soddisfare i seguenti requisiti:

* Le chiavi di corrispondenza devono essere **tagliate**, **in minuscolo**
* Le chiavi di corrispondenza con hash devono essere **SHA256-hash**.
* Se fornisci valori con hash che utilizzano caratteri maiuscoli, Collaboration li converte automaticamente in minuscoli.
* Se l&#39;origine contiene **identificatori di testo normale**, utilizza l&#39;opzione **[!UICONTROL Applica trasformazione]** durante la [configurazione della connessione dati](./manage-data-connection.md#match-keys) per applicare l&#39;hashing. Questa opzione è disponibile solo quando si selezionano i tipi di pubblico da Experience Platform e non è supportata per le origini basate su cloud.

##### ID persone di prime parti

Gli ID persona di prime parti sono direttamente collegati a un singolo profilo. Gli ID attualmente supportati sono:

* **[!UICONTROL E-mail con hash]**
* **[!UICONTROL Telefono con hash]**
* **[!UICONTROL ID CRM]**
* **[!UICONTROL ID fedeltà]**
<!-- * **[!UICONTROL Custom ID]**: Custom identifiers -->

##### ID dispositivo di prime parti

Gli ID dispositivo di prime parti sono identificatori collegati a un dispositivo specifico. Gli ID attualmente supportati sono:

* **[!UICONTROL Hash IPv4]**: indirizzi IPv4 con hash
* **[!UICONTROL IDFA]**: l&#39;identificatore per gli inserzionisti (IDFA) utilizzato nei dispositivi Apple iOS
* **[!UICONTROL GAID]**: ID inserzionista Google utilizzato nei dispositivi Android

##### ID partner

Gli ID partner sono identificatori forniti da partner esterni per la riconciliazione del pubblico. Gli ID attualmente supportati sono:

* **[!UICONTROL ID AdFixus]**

>[!NOTE]
>
>L&#39;integrazione di Adobe con [!DNL AdFixus] associa gli [!UICONTROL ID AdFixus] univoci per ciascun account a un formato con codifica Adobe comune. Queste mappature vengono utilizzate per identificare sovrapposizioni tra collaboratori. Quando si attivano tipi di pubblico con **[!UICONTROL ID AdFixus]**, vengono utilizzati gli ID originali. Il formato codificato da Adobe non lascia mai Collaboration.

Quando selezioni **[!UICONTROL ID AdFixus]**, dovrai fornire l&#39;ID corrispondente dal tuo partner esterno nella sezione **[!UICONTROL Credenziali account]**. Questa opzione sarà disponibile solo *dopo* l&#39;attivazione di **[!UICONTROL ID AdFixus]**. Immetti l&#39;ID AdFixus nel campo **[!UICONTROL ID account]**, assicurandoti di verificare la precisione del valore.

![La finestra di dialogo Corrispondenza chiavi con ID AdFixus è attivata ed è evidenziata la sezione Credenziali account.](/help/assets/setup/manage-account/adfixus-settings.png){zoomable="yes"}

Dopo aver selezionato tutte le chiavi di corrispondenza desiderate, seleziona **[!UICONTROL Completa]** per completare il flusso di lavoro di configurazione dell&#39;account.

![Viene visualizzata la sezione Imposta area di lavoro account con chiavi di corrispondenza.](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Modifica account {#edit-account}

Dopo aver configurato l’account, puoi modificare i dettagli e le chiavi di corrispondenza in qualsiasi momento.

### Modifica dettagli {#edit-details}

Puoi modificare la maggior parte dei dettagli del tuo account in qualsiasi momento, ad eccezione del **[!UICONTROL Ruolo]**. L’area geografica viene impostata automaticamente in base al tuo account Adobe Experience Cloud e non può essere modificata.

Per modificare l&#39;account, selezionare **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Account personale]** dell&#39;area di lavoro **[!UICONTROL Configurazione]**.

![Area di lavoro di installazione con la scheda Account personale e l&#39;opzione Modifica evidenziate.](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

Ora puoi modificare i dettagli del tuo account. Aggiorna i campi che desideri modificare, quindi seleziona **[!UICONTROL Salva]** per confermare le modifiche.

![Finestra di dialogo Modifica dettagli account.](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

### Modifica chiavi di corrispondenza {#edit-match-keys}

>[!IMPORTANT]
>
>La modifica delle chiavi di corrispondenza non influirà sulle connessioni esistenti. Una volta stabilita una connessione, i tasti di corrispondenza selezionati durante la configurazione della connessione vengono corretti. È importante selezionare **tutte** le chiavi di corrispondenza che si intende utilizzare nelle campagne future durante la configurazione dell&#39;account.

Puoi anche aggiornare le chiavi di corrispondenza selezionate inizialmente durante la creazione dell’account. Queste chiavi di corrispondenza determineranno le chiavi di corrispondenza disponibili per le connessioni future.

Seleziona **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Corrispondenza chiavi]**.

![L&#39;area di lavoro del programma di installazione con l&#39;opzione Modifica evidenziata nella sezione delle chiavi di corrispondenza dell&#39;account.](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

Viene visualizzata la finestra di dialogo **[!UICONTROL Corrispondenza chiavi]**. Attiva e disattiva le chiavi di corrispondenza o aggiorna l&#39;**[!UICONTROL ID account]** per l&#39;[!UICONTROL ID AdFixus], quindi seleziona **[!UICONTROL Salva]** per confermare le modifiche.

>[!IMPORTANT]
>
>La modifica del [!UICONTROL ID AdFixus] non attiverà un aggiornamento di [schizzo dati](../glossary.md#sketches) per le connessioni dati esistenti utilizzando la chiave di corrispondenza. Una volta tracciati i dati, eventuali modifiche al tuo [!UICONTROL ID AdFixus] non verranno applicate fino al prossimo aggiornamento del pubblico in base alle impostazioni della [pianificazione della connessione dati](./manage-data-connection.md#scheduling). Se sono necessarie modifiche prima del prossimo aggiornamento, è possibile eliminare e ricreare la connessione dati.

![Finestra di dialogo Corrispondenza chiavi con l&#39;opzione Salva evidenziata.](/help/assets/setup/manage-account/match-key-dialog.png){zoomable="yes"}

## Passaggi successivi

Dopo aver configurato gli account, sei pronto per [generare tipi di pubblico](/help/guide/setup/onboard-audiences.md) in Real-Time CDP Collaboration.
