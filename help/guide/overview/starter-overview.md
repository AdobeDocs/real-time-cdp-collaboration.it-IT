---
title: Panoramica di RTCDP Collaboration Starter
description: Scopri in che modo Adobe Real-Time CDP Collaboration Starter consente di espandere e migliorare la collaborazione basata sulla privacy con un partner con licenza senza richiedere una licenza Real-Time CDP completa.
audience: publisher, advertiser, invited users to Real-Time CDP Collaboration Starter
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/it/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 7ae0bd3d-eee9-48c0-9f18-a56033fee52d
source-git-commit: 3d29985d88e6370b4a0e8cd3d56358e85bb91e06
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 2%

---

# Panoramica dell&#39;Adobe Real-Time CDP Collaboration [!DNL Starter]

Utilizzare l&#39;Adobe Real-Time CDP Collaboration [!DNL Starter] per collaborare con un partner autorizzato a progetti di dati incentrati sulla privacy. Non è necessaria una licenza Collaboration per partecipare.

Il tuo partner autorizzato ti invita in Collaboration e utilizza i suoi crediti per finanziare i flussi di lavoro congiunti, sia tra inserzionisti e editori che tra marchi. Per ulteriori informazioni su questi modelli e sul loro funzionamento, leggere le [guide collaborazione](./collaboration-patterns.md) e le [guide flusso di lavoro end-to-end](./end-to-end-workflow.md).

In qualità di utente [!DNL Starter] invitato, puoi:

* Eseguire l&#39;onboarding e gestire i dati di collaborazione in un account [!DNL Starter].
* Source e gestisci i tipi di pubblico da utilizzare nei progetti congiunti.
* Ottieni informazioni approfondite sulle sovrapposizioni di pubblico con il tuo partner per supportare il targeting efficace e la misurazione delle campagne.
* Attiva i tipi di pubblico e condividili nuovamente con il tuo partner per l’attivazione e il coinvolgimento congiunti delle campagne.

## Prerequisiti {#prerequisites}

Per iniziare a utilizzare Collaboration [!DNL Starter], assicurarsi che l&#39;organizzazione e il partner con licenza si trovino nella stessa area geografica. Devi essere invitato da un partner titolare di una licenza Real-Time CDP Prime, Ultimate o Collaboration.

Per avviare l&#39;invito, fornire le seguenti informazioni al partner con licenza:

* Nome del contatto
* E-mail di contatto
* Azienda
* Ruolo (inserzionista/editore): inserzionista
* Settore

Dopo aver ricevuto e accettato l&#39;invito, l&#39;organizzazione deve rivedere e firmare un ordine di vendita gratuito con Adobe per accedere a Collaboration [!DNL Starter]. Per ulteriori dettagli sul processo di invito, vedere la guida [invito di un collaboratore a Collaboration [!DNL Starter]](../connect/establishing-connections.md#invite-collaborator-to-starter).

## Guardrail {#guardrails}

Leggi la tabella seguente per comprendere i guardrail delle chiavi applicabili al tuo account [!DNL Starter]. Questi includono limiti sull’origine del pubblico, volume dei dati, frequenza di aggiornamento, sovrapposizioni di pubblico e funzionalità di attivazione.

| Guardrail | Descrizione |
|----------| ------------|
| Origine pubblico | È possibile inserire i dati del pubblico in Collaboration utilizzando **[!DNL Amazon S3]** come origine. Per istruzioni dettagliate, consulta [come configurare [!DNL Amazon S3] per audience sourcing](../setup/configure-aws-s3-audience-sourcing.md). |
| Pubblico | Il tuo account [!DNL Starter] ha diritto a un massimo di:<ul><li>10 tipi di pubblico originati da un bucket [!DNL AWS S3]</li><li>50 milioni di identità totali (calcolate in base al numero di righe nei dati del pubblico)</li><li>1 aggiornamento per pubblico ogni 6 giorni</li></ul> |
| Sovrapposizioni di pubblico e approfondimenti | Non esiste un limite di utilizzo per la frequenza con cui è possibile eseguire sovrapposizioni di pubblico e informazioni approfondite tra i tipi di pubblico. Learn how to [discover overlaps and compare audiences](../collaborate/discover.md). |
| Activation | In qualità di utente [!DNL Starter], puoi attivare e condividere i tipi di pubblico solo con il partner che ti ha invitato. La configurazione delle destinazioni su piattaforme esterne non è disponibile. Ulteriori informazioni sull&#39;[attivazione dei tipi di pubblico](../collaborate/activate.md). |

{style="table-layout:auto"}

## Guida introduttiva {#getting-started}

Dopo aver [accettato l&#39;invito e accettato le condizioni](../connect/establishing-connections.md#accept-invitation-sign-terms), accedi a [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} con le tue credenziali. Prima di poter utilizzare Collaboration, è necessario concedere al tuo account l’accesso e i ruoli appropriati.

Utilizzare questo flusso di lavoro per configurare l&#39;account [!DNL Starter] e iniziare a collaborare con il partner.

### Configurare l’accesso come amministratore {#setup-admin-access}

Innanzitutto, utilizza l&#39;area di lavoro **Accesso amministratore** per concederti l&#39;accesso necessario. In questo modo puoi disporre sia di diritti amministrativi che di accesso utente ai prodotti Experience Platform. Per i passaggi dettagliati sulla configurazione dell&#39;accesso iniziale, vedere le [istruzioni di accesso per amministratori](../setup/starter-admin-access.md).

Al termine, dovresti visualizzare **[!UICONTROL Autorizzazioni]**, **[!UICONTROL Experience Platform]** e **[!UICONTROL Real-Time CDP Collaboration]** nella sezione **[!UICONTROL Accesso rapido]** della tua home page di [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}.

![L&#39;area di lavoro di Adobe Experience Cloud mostra le autorizzazioni, Experience Platform e Real-Time CDP Collaboration dopo la configurazione dell&#39;accesso dell&#39;amministratore del prodotto.](/help/assets/overview/starter/setup-admin-access.png){zoomable="yes"}

Per ulteriori dettagli sui ruoli di accesso e sui diversi prodotti Adobe Experience Cloud, leggere la [panoramica sul controllo di accesso](../permissions/overview.md).

### Configurare le autorizzazioni {#configure-permissions}

Ora che disponi dei privilegi di amministratore, puoi assegnare ruoli e autorizzazioni a te stesso e ad altri utenti dell’organizzazione. Questo passaggio è necessario prima di poter accedere a Real-Time CDP Collaboration o consentire ad altri di utilizzarlo. Per istruzioni dettagliate, vedere [come configurare le autorizzazioni](../setup/starter-permission-controls.md). Per ulteriori informazioni sui diversi ruoli e autorizzazioni disponibili in Collaboration, consulta la documentazione di [gestione ruoli](../permissions/manage-roles.md).

Una volta assegnati ruoli e autorizzazioni, verifica di poter accedere a Collaboration. Passa a [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} e seleziona **[!UICONTROL Real-Time CDP Collaboration]** nella sezione **[!UICONTROL Accesso rapido]**. Verrà aperta l&#39;area di lavoro **[!UICONTROL Adobe Real-Time CDP Collaboration]**, in cui è possibile iniziare a utilizzare le funzionalità di Collaboration.

### Configurare le connessioni {#set-up-connections}

Quindi, segui i passaggi descritti nelle seguenti guide per impostare la connessione e iniziare a collaborare con il tuo partner:

* [Configurare l’account Collaboration](../setup/onboard-account.md)
* [Stabilisci una connessione con il tuo collaboratore che invita](../connect/overview.md)
* [Crea un nuovo progetto e inizia a collaborare con il tuo partner](../collaborate/overview.md)

### Comprendere l’utilizzo del credito {#understand-credit-usage}

Tutte le attività di Collaboration [!DNL Starter] utilizzano crediti. Tuttavia, in qualità di utente invitato, non è necessario acquistare o gestire questi crediti. Il collaboratore che ti ha invitato copre tutto l&#39;utilizzo del credito associato alle tue attività. Per ulteriori informazioni, consulta la [documentazione sull&#39;utilizzo e il consumo del credito [!DNL Starter]](../setup/starter-credit-usage.md).

## Passaggi successivi {#next-steps}

Hai completato la configurazione iniziale e hai configurato l’organizzazione per una collaborazione sicura. Quindi, esplora le seguenti risorse per scoprire di più sull’audience sourcing e diversi casi d’uso del progetto in Collaboration:

* [Source e gestire i tipi di pubblico](../setup/onboard-audiences.md)
* [Casi di utilizzo del progetto](../collaborate/overview.md#project-use-cases):
   * [Scopri le sovrapposizioni e confronta i tipi di pubblico](../collaborate/discover.md)
   * [Attiva tipi di pubblico](../collaborate/activate.md)
   * [Misura le prestazioni della campagna](../collaborate/measure.md)
