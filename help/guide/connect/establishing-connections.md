---
title: Connessione con inserzionisti o editori
description: Dopo aver individuato i potenziali collaboratori, scopri come stabilire connessioni e iniziare a collaborare ai progetti.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: e0894fb3cb290334e0e95d5c26288705967d9dbe
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 15%

---

# Connessione con inserzionisti o editori

{{limited-availability-release-note}}

Stabilire una connessione tra due parti di una collaborazione (più comunemente un inserzionista e un editore) è il prerequisito in Real-Time CDP Collaboration per le aziende che lavorano insieme sulle campagne. Sia gli editori che gli inserzionisti possono impostare connessioni. La parte che avvia la connessione sarà in seguito *proprietario connessione*.

## Flusso di lavoro di alto livello

Ad alto livello, per stabilire una connessione tra un inserzionista e un editore, il flusso di lavoro si presenta come segue:

1. L&#39;inserzionista [sfoglia gli editori e ne scopre](/help/guide/connect/discover-publishers.md) uno con cui vorrebbe lavorare
2. L&#39;inserzionista invia un invito di connessione.
3. L’editore accetta l’invito.
4. L&#39;inserzionista invia le impostazioni di connessione, incluse le chiavi di corrispondenza e altre. Queste impostazioni di connessione rappresentano i termini della collaborazione all&#39;interno del prodotto.
5. L&#39;editore accetta le impostazioni di connessione. Se lo si desidera, l&#39;editore può rifiutare le impostazioni di connessione iniziali e richiedere che l&#39;inserzionista invii le impostazioni di connessione riviste.

![Diagramma di alto livello del processo di connessione inserzionista-editore.](/help/assets/connect/establish-connection/advertiser-publisher-connection-process.png){zoomable="yes"}

Una volta completati gli elementi di cui sopra, i collaboratori possono procedere a [creare un progetto](/help/guide/collaborate/manage-projects.md#create-project) per [eseguire rapporti di sovrapposizione](/help/guide/collaborate/discover.md) e avviare campagne pubblicitarie.

>[!IMPORTANT]
>
>Una volta stabilita la connessione tra due collaboratori, le impostazioni di connessione non possono più essere riviste.

## Invia invito {#send-invite}

Per impostare una connessione, selezionare **[!UICONTROL Connetti]** durante la navigazione nell&#39;inventario degli editori nella schermata di individuazione degli editori.

![Connetti selettore](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

A questo punto, l’invito non è disponibile e puoi visualizzare in anteprima le impostazioni di connessione, ma non puoi modificarle. Puoi visualizzare l&#39;invito in sospeso nella scheda **[!UICONTROL Le mie connessioni]**. Lo stato della connessione è **[!UICONTROL Invito inviato]**.

![Invito in sospeso inviato all&#39;editore visualizzato nella visualizzazione Connessioni personali.](/help/assets/connect/establish-connection/pending-invite-sent.png){zoomable="yes"}

Una volta che il collaboratore accetta l&#39;invito, è possibile configurare le impostazioni di connessione e inviarle al collaboratore per la revisione e l&#39;accettazione.

## Impostazioni della connessione {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="Casi d’uso"
>abstract="I casi d’uso sono precompilati con tutte le opzioni. Puoi modificare i casi d’uso prima di inviare le impostazioni di connessione."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="Chiavi di corrispondenza"
>abstract="Le chiavi di corrispondenza sono precompilate con quelle selezionate a livello di organizzazione. Puoi disattivare le chiavi di corrispondenza che non desideri utilizzare in questa connessione."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit"
>title="Suddivisione del credito"
>abstract="Questa sezione determina chi paga per le attività corrispondenti all’interno della collaborazione di Real-Time CDP. Attualmente, è possibile configurare solo il caso d’uso di condivisione del pubblico."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Condivisione del pubblico"
>abstract="La condivisione del pubblico è l’attività che una parte intraprende quando richiede che i dati corrispondenti vengano attivati dal proprio partner di collaborazione."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Misurazione"
>abstract="Questo caso d’uso consente di eseguire attività nella collaborazione di Real-Time CDP per generare rapporti sulle prestazioni delle campagne e informazioni approfondite."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Accordo legale"
>abstract="Verifica l’esistenza di un accordo di condivisione dei dati tra le due parti."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Nomi inserzionisti"
>abstract="Indica gli alias in base ai quali l&#39;inserzionista è noto all&#39;editore. "

Dopo l’invio dell’invito, puoi visualizzare in anteprima le impostazioni di connessione. L’invito deve essere accettato prima di poter completare la configurazione della connessione.

![Visualizzazione delle impostazioni di connessione nello stato di anteprima.](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

Una volta che la connessione è stata accettata dal collaboratore, è ora possibile avviare la configurazione delle impostazioni di connessione per la connessione. Le impostazioni di connessione definiscono i termini della collaborazione, ad esempio i casi d&#39;uso che verranno eseguiti insieme, le chiavi di corrispondenza che verranno utilizzate nei progetti e altro ancora.

Per impostare e condividere le impostazioni di connessione con il tuo collaboratore, passa a **[!UICONTROL Le mie connessioni]**. Per qualsiasi connessione con stato **[!UICONTROL In sospeso]**, è possibile selezionare **[!UICONTROL Configura connessione]** per configurare le impostazioni di connessione.

![La visualizzazione Connessioni personali con una connessione in sospeso e l&#39;opzione Configura connessione evidenziata.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

Puoi modificare e definire i campi seguenti:

![Configura visualizzazione connessione](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++Casi d’uso

I casi di utilizzo sono precompilati con tutti i casi di utilizzo disponibili. È possibile scegliere i casi d&#39;uso che la connessione utilizzerà selezionando **[!UICONTROL Modifica]** e disattivando quelli non desiderati. I casi d&#39;uso selezionati determineranno quali visualizzazioni e opzioni sono [disponibili nei tuoi progetti](../collaborate/manage-projects.md#project-use-cases).

![Casi d’uso](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++Corrispondenza chiavi

Le chiavi di corrispondenza sono precompilate con quelle selezionate [a livello di organizzazione](/help/guide/setup/onboard-organization.md#set-up-match-keys). È possibile disattivare le chiavi di corrispondenza che non si desidera utilizzare in questa connessione, ma non è possibile aggiungere chiavi di corrispondenza non selezionate durante la configurazione dell&#39;organizzazione.

![Corrispondenza chiavi](/help/assets/connect/establish-connection/match-keys.png)

+++

+++Divisione del credito

Utilizzare la sezione della suddivisione del credito per determinare quale delle due parti che collaborano coprirà i costi delle attività.

![Divisione crediti](/help/assets/connect/establish-connection/edit-billing-ownership.png)

+++

+++Accordi

Prima di poter procedere con questa connessione, è necessario riconoscere l&#39;esistenza di un accordo di condivisione dei dati tra le due parti.

![Accordi legali.](/help/assets/connect/establish-connection/legal-agreement.png)

+++

Dopo aver effettuato la selezione, selezionare **[!UICONTROL Invia]** per inviare le impostazioni suggerite al collaboratore per la revisione.

Se ricevi le impostazioni di connessione proposte dal tuo collaboratore, puoi **[!UICONTROL Accettare]** o **[!UICONTROL Rifiutare]** tali impostazioni. Prima di accettare le impostazioni di connessione, è necessario confermare l&#39;esistenza di un accordo legale tra l&#39;utente e il collaboratore. Se rifiuti le impostazioni di connessione, rivolgiti al tuo collaboratore all’esterno del prodotto e discuti come dovrebbero rivedere le impostazioni di connessione affinché tu possa accettarle.

## Elimina connessioni {#delete-connections}

È possibile eliminare le connessioni con i collaboratori che non si desidera continuare a utilizzare. Per eliminare le connessioni esistenti:

1. Passa a **[!UICONTROL Connetti]** > **[!UICONTROL Le mie connessioni]**.
2. Selezionare **[!UICONTROL Visualizza connessione]** sulla scheda di connessione per accedere alla connessione che si desidera eliminare.
3. Seleziona l&#39;icona Elimina ![icona Elimina](/help/assets/common/delete.svg) per visualizzare la finestra di conferma dell&#39;eliminazione della connessione.
   ![Icona Elimina connessione evidenziata.](/help/assets/connect/establish-connection/delete-icon-highlighted.png){zoomable="yes"}
4. Confermare l&#39;eliminazione selezionando **[!UICONTROL Elimina]**.
   ![Finestra di dialogo per confermare l&#39;eliminazione di una connessione. ](/help/assets/connect/establish-connection/delete-connection-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Una volta eliminata la connessione, non potrai più essere connesso con il collaboratore e tutti i progetti esistenti che fanno parte della collaborazione verranno eliminati definitivamente e non potranno essere ripristinati.

## Passaggi successivi

Dopo aver stabilito una connessione con il tuo collaboratore, ora tu e il tuo collaboratore potete [creare progetti](/help/guide/collaborate/manage-projects.md#create-project).
