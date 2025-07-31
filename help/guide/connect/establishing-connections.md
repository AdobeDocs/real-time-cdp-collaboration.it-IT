---
title: Stabilimento di connessioni
description: Dopo aver individuato i potenziali collaboratori, scopri come stabilire connessioni e iniziare a collaborare ai progetti.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: c159bbcdc5f84abc4c591c5256192d117ec51102
workflow-type: tm+mt
source-wordcount: '3213'
ht-degree: 7%

---

# Stabilimento di connessioni

{{limited-availability-release-note}}

Prima che i collaboratori possano lavorare insieme sulle campagne, devono stabilire una connessione. Questa connessione consente loro di attivare tipi di pubblico, creare progetti ed eseguire rapporti sulle prestazioni della campagna.

Le connessioni vengono stabilite in base al modello di collaborazione scelto. Collaboration supporta due pattern di collaborazione chiave: da inserzionista a editore e da brand a brand. Per ulteriori informazioni su questi pattern, consulta la guida [casi d&#39;uso](/help/guide/overview/use-cases.md).

<!-- REPLACE THE LINK ABOVE WITH THE CORRECT LINK AFTER PAGE IS ESTABLISHED -->

Per informazioni su come stabilire una connessione, leggere la sezione seguente corrispondente al proprio modello di collaborazione:

- [Connessione inserzionista-editore](#advertiser-to-publisher-connection)
- [Connessione brand-to-brand](#brand-to-brand-connection)

## Connessione inserzionista-editore {#advertiser-to-publisher-connection}

![Diagramma di alto livello del processo di connessione inserzionista-editore.](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

Nel modello da inserzionista a editore, un inserzionista individua un editore con cui desidera collaborare tramite l&#39;area di lavoro **[!UICONTROL Discover publishers]** e invia un invito alla connessione. L’editore rivede quindi l’invito e lo accetta, consentendo all’inserzionista di proporre le impostazioni di connessione. Una volta che l&#39;editore accetta le impostazioni di connessione, la connessione viene stabilita ed entrambi i collaboratori possono iniziare a lavorare insieme ai progetti.

### Panoramica di alto livello

Per stabilire una connessione tra un inserzionista e un editore, sono necessari i seguenti passaggi:

1. [Individua editori](#discover-publishers): l&#39;inserzionista identifica i potenziali editori con cui collaborare.
2. [Invia invito](#send-invite): l&#39;inserzionista invia un invito di connessione all&#39;editore selezionato.
3. [Accetta invito](#accept-invite): l&#39;editore rivede e accetta l&#39;invito.
4. [Configura impostazioni di connessione](#configure-connection-settings): l&#39;inserzionista configura le impostazioni di connessione e le invia all&#39;editore per la revisione.
5. [Conferma impostazioni di connessione](#establish-connection): l&#39;editore esamina le impostazioni di connessione e le accetta o le rifiuta. Se accettata, la connessione viene stabilita. Se viene rifiutato, l’editore può fornire un feedback per le revisioni al di fuori del prodotto. L&#39;inserzionista può quindi rivedere le impostazioni e inviarle nuovamente per la revisione.

Una volta accettate le impostazioni di connessione, la connessione viene stabilita e i collaboratori sono pronti a [creare un progetto](/help/guide/collaborate/manage-projects.md#create-project) per iniziare a collaborare alle campagne.

## Connessione brand-to-brand {#brand-to-brand-connection}

![Diagramma di alto livello del processo di connessione brand-to-brand.](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>Il termine **brand** viene utilizzato per indicare un&#39;azienda o un brand al di fuori di Collaboration. Il termine **collaboratore** fa riferimento a qualsiasi account che può creare una connessione in Collaboration, indipendentemente dal fatto che sia un inserzionista o un editore.

Nel modello brand-to-brand, due brand che hanno comunicato al di fuori del prodotto possono connettersi direttamente in Collaboration utilizzando un [invito di connessione privato](#private-connection-invite). Un marchio può essere un inserzionista o un editore. Questo modello è particolarmente utile per i marchi che potrebbero non rientrare nel modello tradizionale inserzionista-editore, ad esempio due inserzionisti o due editori.

Per iniziare, un collaboratore invia un invito di connessione privato a un altro collaboratore. Il destinatario rivede l’invito e lo accetta, consentendo al proprietario di proporre le impostazioni di connessione. Una volta che il destinatario accetta le impostazioni di connessione, la connessione viene stabilita ed entrambi i collaboratori possono iniziare a lavorare insieme ai progetti.

### Panoramica di alto livello

>[!TIP]
>
>Quando si parla del processo di connessione, verrà fatta una distinzione tra **proprietario** e **destinatario**. Il proprietario è il collaboratore che avvia la connessione inviando l&#39;invito, mentre il destinatario è il collaboratore che riceve e rivede l&#39;invito.

Il processo di connessione tra due marchi prevede diversi passaggi. Prima di avviare il processo di connessione, è necessario soddisfare alcuni prerequisiti:

1. Due marchi comunicano al di fuori del prodotto per discutere il potenziale collegamento.
2. I marchi [creano account](/help/guide/setup/onboard-account.md) in Collaboration, se non lo hanno già fatto, assicurandosi di selezionare il tipo di ruolo appropriato (inserzionista o editore).

Una volta soddisfatti i prerequisiti, il processo di connessione può iniziare. Le seguenti fasi delineano il processo:

1. [Invia invito di connessione privata](#send-private-connection-invite): un collaboratore invia un invito di connessione privata a un altro collaboratore.
2. [Accetta invito di connessione privata](#accept-private-connection-invite): il destinatario rivede e accetta l&#39;invito di connessione privata.
3. [Configura impostazioni di connessione](#configure-connection-settings): il proprietario configura le impostazioni di connessione e le invia al destinatario per la revisione e l&#39;accettazione.
4. [Conferma impostazioni di connessione](#establish-connection): il destinatario esamina le impostazioni di connessione e le accetta o le rifiuta.

Una volta accettate le impostazioni di connessione, la connessione viene stabilita e i collaboratori sono pronti a [creare un progetto](/help/guide/collaborate/manage-projects.md#create-project) per iniziare a collaborare alle campagne.

## Connessione {#connect}

L&#39;area di lavoro **[!UICONTROL Connetti]** consente di gestire le connessioni con i collaboratori, inviare inviti di connessione e consentire agli inserzionisti di sfogliare la directory di pubblicazione. L’area di lavoro è divisa in due schede principali:

### Individua editori {#discover-publishers}

>[!IMPORTANT]
>
>Solo gli inserzionisti possono individuare gli editori utilizzando l&#39;area di lavoro **[!UICONTROL Individua editori]**. Per informazioni sulla connessione con i collaboratori indipendentemente dal loro ruolo, consulta la sezione [connessione brand-to-brand](#brand-to-brand-connection).

Per individuare gli editori, passare all&#39;area di lavoro **[!UICONTROL Individua editori]** nella scheda **[!UICONTROL Connetti]**. Qui puoi sfogliare l’elenco degli editori disponibili utilizzando i controlli di impaginazione nella parte inferiore dell’area di lavoro. Per ulteriori informazioni sull&#39;area di lavoro **[!UICONTROL Individua autori]**, vedere la guida [individua autori](/help/guide/connect/discover-publishers.md).

![Nell&#39;area di lavoro Individua editori viene visualizzato un elenco degli editori disponibili.](/help/assets/connect/establish-connection/discover-publishers.png){zoomable="yes"}

### Invia invito {#send-invite}

>[!IMPORTANT]
>
>Questa sezione descrive il processo con cui gli inserzionisti inviano inviti di connessione agli editori tramite l&#39;area di lavoro **[!UICONTROL Discover publishers]**. Per informazioni sulla creazione di connessioni tra brand indipendentemente dai ruoli, leggi la sezione [connessione brand-to-brand](#brand-to-brand-connection) o visita la sezione [invito connessione privata](#private-connection-invite).

Dopo aver identificato un editore con cui vuoi collaborare, seleziona l&#39;opzione **[!UICONTROL Connetti]** nella scheda dell&#39;editore. Questa azione avvia il processo di connessione.

![L&#39;opzione Connetti è evidenziata in un editore specifico nell&#39;area di lavoro Individua editori.](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo in cui viene richiesto di inviare un invito alla connessione all&#39;editore. Seleziona **[!UICONTROL Invia invito]** per continuare.

![Finestra di dialogo Invia invito alla connessione con il pulsante Invia invito evidenziato.](/help/assets/connect/establish-connection/send-connection-invite-dialog.png){zoomable="yes"}

>[!NOTE]
>
>Se si desidera connettersi a un editore con cui si è stabilito un contatto esterno al prodotto, è possibile utilizzare l&#39;opzione di invito di connessione privata. Per ulteriori informazioni, consulta la sezione [invito alla connessione privata](#private-connection-invite).

L&#39;invito in sospeso viene visualizzato nella scheda **[!UICONTROL Le mie connessioni]** della sezione **[!UICONTROL Azione richiesta]**. Lo stato della connessione è **[!UICONTROL Invito inviato]**. È possibile visualizzare in anteprima le impostazioni di connessione selezionando **[!UICONTROL Anteprima connessione]**, ma non è possibile modificarle finché l&#39;autore non accetta l&#39;invito.

![La connessione in sospeso viene visualizzata nell&#39;area di lavoro Connessioni personali nella sezione Azione richiesta.](/help/assets/connect/establish-connection/preview-connection.png){zoomable="yes"}

### Invito connessione privata {#private-connection-invite}

Gli inviti di connessione privata consentono di connettersi ai collaboratori con cui hai comunicato all&#39;esterno del prodotto utilizzando un **[!UICONTROL Codice connessione]**. Per creare una connessione privata, è necessario ottenere il **[!UICONTROL codice di connessione]** dal collaboratore con cui si desidera stabilire la connessione all&#39;esterno del prodotto. È quindi possibile utilizzare questo codice per inviare un invito di connessione privato al collaboratore nell&#39;area di lavoro **[!UICONTROL Connetti]**.

#### Codice di connessione {#connect-code}

Prima di poter inviare un invito di connessione privato, il collaboratore desiderato deve fornire il proprio **[!UICONTROL codice di connessione]** univoco. Per trovare e copiare il **[!UICONTROL codice di connessione]**, passare alla scheda **[!UICONTROL Account personale]** nell&#39;area di lavoro **[!UICONTROL Configurazione]**. Il codice **[!UICONTROL Connect]** viene visualizzato nei dettagli dell&#39;account.

![Scheda Account personale nell&#39;area di lavoro di installazione con il codice Connect evidenziato.](/help/assets/connect/establish-connection/connect-code.png){zoomable="yes"}

Seleziona l&#39;icona Copia (![icona Copia](/help/assets/icons/copy.png)) accanto a **[!UICONTROL Codice di connessione]** per copiarlo negli Appunti. Puoi quindi condividere questo codice con il tuo collaboratore al di fuori del prodotto.

![Il codice di connessione con l&#39;icona di copia evidenziata.](/help/assets/connect/establish-connection/copy-connect-code.png){zoomable="yes"}

##### Aggiornamento del codice di connessione {#refresh-connect-code}

Puoi aggiornare il tuo **[!UICONTROL Codice di connessione]** in qualsiasi momento. L&#39;aggiornamento del codice genera un nuovo codice univoco che puoi condividere con i collaboratori. Questa opzione è utile se desideri annullare la validità del codice precedente per motivi di sicurezza. Tutte le connessioni stabilite utilizzando il vecchio codice rimarranno attive, ma i nuovi collaboratori dovranno utilizzare il nuovo codice per connettersi con te.

>[!IMPORTANT]
>
>L&#39;aggiornamento del **[!UICONTROL codice di connessione]** durante un invito in sospeso potrebbe impedire l&#39;accettazione dell&#39;invito. Se aggiorni il codice, il tuo collaboratore potrebbe dover inviare nuovamente l’invito alla connessione privata utilizzando il nuovo codice.

Per aggiornare il **[!UICONTROL Codice di connessione]**, seleziona l&#39;icona di aggiornamento (![icona di aggiornamento](/help/assets/icons/refresh.png)) accanto a **[!UICONTROL Codice di connessione]**.

![Il codice di connessione con l&#39;icona di aggiornamento evidenziata.](/help/assets/connect/establish-connection/refresh-connect-code.png){zoomable="yes"}

>[!IMPORTANT]
>
>Tutti gli account creati prima dell&#39;introduzione della funzionalità **[!UICONTROL Codice di connessione]** non avranno un codice di connessione generato e il campo di connessione verrà visualizzato come **[!UICONTROL Non disponibile]**. Utilizza l’opzione di aggiornamento per generare un nuovo codice di connessione.

#### Invia invito di connessione privata {#send-private-connection-invite}

Una volta ottenuto il **[!UICONTROL Codice di connessione]** dal collaboratore, puoi inviare un invito di connessione privato. A questo scopo, passa all&#39;area di lavoro **[!UICONTROL Connetti]** e seleziona l&#39;icona più (![icona più](/help/assets/icons/plus.png)) nell&#39;angolo superiore destro.

![Icona più evidenziata nell&#39;area di lavoro di connessione.](/help/assets/connect/establish-connection/private-connection-invite.png){zoomable="yes"}

Viene visualizzata la finestra di dialogo **[!UICONTROL Connetti]** in cui viene richiesto di immettere il **[!UICONTROL Codice di connessione]** del collaboratore con cui si desidera stabilire la connessione. Incolla il codice nel campo di testo e seleziona **[!UICONTROL Continua]** per continuare.

![La finestra di dialogo Connetti con il campo Codice di connessione è stata compilata ed è stata evidenziata l&#39;opzione Continua.](/help/assets/connect/establish-connection/private-connection-invite-connect.png){zoomable="yes"}

Nella finestra di dialogo **[!UICONTROL Connetti]** verrà quindi visualizzato il collaboratore a cui è associato il codice, che consente di confermare la connessione con il collaboratore corretto. Se il collaboratore è corretto, selezionare **[!UICONTROL Connetti]** per inviare l&#39;invito alla connessione privata.

![Viene visualizzata la finestra di dialogo Connetti con i dettagli del collaboratore e viene evidenziata l&#39;opzione Connetti.](/help/assets/connect/establish-connection/private-connection-invite-connect-confirm.png){zoomable="yes"}

### Accetta invito {#accept-invite}

>[!TIP]
>
>Quando si parla del processo di connessione, verrà fatta una distinzione tra **proprietario** e **destinatario**. Il proprietario è il collaboratore che avvia la connessione inviando l&#39;invito, mentre il destinatario è il collaboratore che riceve e rivede l&#39;invito.

Prima che il proprietario possa configurare le impostazioni di connessione, il destinatario deve accettare l&#39;invito alla connessione. A tale scopo, passare all&#39;area di lavoro **[!UICONTROL Connetti]** e trovare la connessione in sospeso nella sezione **[!UICONTROL Azione richiesta]**. Lo stato della connessione è **[!UICONTROL Invito ricevuto]**. Seleziona **[!UICONTROL Accetta]** per accettare l&#39;invito.

![La connessione in sospeso viene visualizzata nella sezione Azione richiesta dell&#39;area di lavoro Connessione con l&#39;opzione Accetta evidenziata.](/help/assets/connect/establish-connection/accept-connection.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo in cui viene richiesto di accettare l&#39;invito. Selezionare **[!UICONTROL Accetta invito]** per continuare.

![Finestra di dialogo Accetta invito alla connessione con l&#39;opzione Accetta invito evidenziata.](/help/assets/connect/establish-connection/accept-connection-invite.png){zoomable="yes"}

Lo stato della connessione cambia in **[!UICONTROL In sospeso]**. Il proprietario può ora configurare le impostazioni di connessione.

### Configurare le impostazioni di connessione {#configure-connection-settings}

Le impostazioni di connessione definiscono i termini tra due collaboratori. Queste impostazioni includono casi d’uso, chiavi di corrispondenza, ripartizione del credito e contratti legali. I collaboratori che si connettono con gli inserzionisti possono anche aggiungere nomi degli inserzionisti alle impostazioni di connessione, che verranno utilizzate durante la creazione dei progetti.

Dopo che il destinatario accetta l’invito, il proprietario può configurare le impostazioni di connessione. A tale scopo, passare a **[!UICONTROL Le mie connessioni]** e trovare la connessione in sospeso nella sezione **[!UICONTROL Azione richiesta]**. Selezionare **[!UICONTROL Configura connessione]** per configurare le impostazioni di connessione.

![L&#39;area di lavoro Connessione con l&#39;opzione Configura connessione è evidenziata nella sezione Azione richiesta.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

Viene visualizzata l&#39;area di lavoro delle impostazioni di connessione, che consente di configurare le varie impostazioni della connessione.

![Area di lavoro impostazioni connessione.](/help/assets/connect/establish-connection/connection-set-up.png){zoomable="yes"}

<!-- FIX THE ABOVE SCREENSHOT TO INCLUDE ADV NAMES, AS WELL AS THE ONES BELOW -->

#### Impostazioni della connessione {#connection-settings}

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
>abstract="Questa sezione determina chi paga per le attività corrispondenti all’interno di Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Condivisione del pubblico"
>abstract="I crediti di attivazione del pubblico vengono utilizzati in base al numero di ID corrispondenti preparati per l’attivazione."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Misurazione"
>abstract="Esegui attività per generare report e informazioni approfondite sulle prestazioni della campagna. I crediti vengono utilizzati in base al numero di righe nei rapporti sulle campagne in tutte le campagne e alla frequenza di reporting (giornaliera, ogni tre giorni o settimanale)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Accordo legale"
>abstract="Verifica l’esistenza di un accordo di condivisione dei dati tra le due parti."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Nome inserzionista"
>abstract="<p>Impostazione facoltativa. Indica nome e ID in base ai quali l’inserzionista è noto all’editore.</p><p>Il nome dell’inserzionista aggiunto qui verrà precompilato nel passaggio Crea progetto.</p><ul><li>Se l’editore ha configurato più nomi, selezionane uno dall’elenco.</li><li>Se è stato configurato un solo nome, questo viene preselezionato automaticamente.</li><li>Se non è configurato alcun nome, il campo verrà precompilato con il nome dell’account dell’inserzionista preso da Collaboration.</li></ul>"
>additional-url="https://experienceleague.adobe.com/it/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="Creare un progetto"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_activation"
>title="Attivazione del pubblico"
>abstract="L’attivazione del pubblico consente di selezionare il collaboratore che può avviarla."

Puoi configurare le seguenti impostazioni di connessione:

+++Attivazione pubblico

>[!IMPORTANT]
>
>Tutte le connessioni create prima dell&#39;introduzione della funzionalità **[!UICONTROL Audience Activation]** avranno automaticamente l&#39;impostazione di Audience Activation impostata sul proprietario della connessione. Se vuoi consentire a entrambi i collaboratori di attivare i tipi di pubblico, devi [eliminare la connessione corrente](#delete-connections) e crearne una nuova con le impostazioni aggiornate.

L’attivazione del pubblico consente di selezionare quale collaboratore può attivare i tipi di pubblico all’interno della connessione. L&#39;attivazione del pubblico sarà un&#39;opzione solo se è selezionato il caso d&#39;uso **[!UICONTROL Attivazione pubblico]**. Se scegli di rimuovere il caso d’uso durante il processo di connessione, l’impostazione di attivazione del pubblico verrà rimossa dalle impostazioni di connessione. Per ulteriori informazioni su Audience Activation, consulta la guida [activate](/help/guide/collaborate/activate.md).

Per impostare l&#39;attivazione del pubblico, selezionare **[!UICONTROL Imposta]** nella sezione **[!UICONTROL Attivazione pubblico]**. Utilizza il menu a discesa per specificare quale collaboratore può attivare i tipi di pubblico. Puoi scegliere un singolo collaboratore o consentire a entrambi i collaboratori di attivare i tipi di pubblico.

![Finestra di dialogo di attivazione del pubblico con opzioni nell&#39;area di lavoro delle impostazioni della connessione.](/help/assets/connect/establish-connection/audience-activation.png){zoomable="yes"}

Al termine, seleziona **[!UICONTROL Salva]** per salvare le modifiche.

![Finestra di dialogo di attivazione del pubblico con l&#39;opzione Salva nell&#39;area di lavoro delle impostazioni della connessione.](/help/assets/connect/establish-connection/audience-activation-confirm.png){zoomable="yes"}

+++

+++Casi d’uso

I casi di utilizzo vengono compilati automaticamente con tutte le opzioni disponibili. I casi d’uso selezionati determinano quali visualizzazioni e opzioni sono disponibili all’interno dei tuoi progetti. Per ulteriori informazioni, consulta la guida ai [casi d&#39;uso del progetto](/help/guide/collaborate/manage-projects.md#project-use-cases).

Per personalizzare i tuoi casi d&#39;uso, seleziona **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Casi d&#39;uso]** e disattiva quelli che non desideri includere in alcun progetto con il tuo collaboratore. Al termine, seleziona **[!UICONTROL Salva]** per salvare le modifiche.

![Impostazioni dei casi d&#39;uso nell&#39;area di lavoro delle impostazioni della connessione.](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++Corrispondenza chiavi

Le chiavi di corrispondenza vengono compilate automaticamente con quelle selezionate durante [la configurazione dell&#39;account](/help/guide/setup/onboard-account.md#set-up-match-keys). È possibile disattivare i tasti di corrispondenza che non si desidera utilizzare, ma non è possibile aggiungere i tasti di corrispondenza che non sono stati selezionati durante la configurazione dell&#39;account.

Per personalizzare le chiavi di corrispondenza, seleziona **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Chiavi di corrispondenza]** e disattiva le chiavi di corrispondenza che non desideri utilizzare in questa connessione. Al termine, seleziona **[!UICONTROL Salva]** per salvare le modifiche.

![Impostazioni chiave di corrispondenza nell&#39;area di lavoro delle impostazioni di connessione.](/help/assets/connect/establish-connection/match-keys.png){zoomable="yes"}

+++

+++Divisione del credito

Utilizzare la sezione della suddivisione del credito per determinare quale delle due parti che collaborano coprirà i costi delle attività. Le opzioni di frazionamento del credito sono determinate dai casi d’uso selezionati per la connessione. Mentre il caso d&#39;uso **[!UICONTROL Misurazione]** richiede una parte per coprire i costi, il caso d&#39;uso **[!UICONTROL Attivazione - Corrispondenza]** offre un&#39;opzione aggiuntiva per consentire a ciascuna parte di coprire i propri costi. Per informazioni sulla suddivisione dei costi, leggere la guida dei [tipi di attività di credito](/help/guide/setup/my-activity.md#types-of-activities).

>[!NOTE]
>
>Pubblico: l’uscita è sempre coperta dal collaboratore che riceve il pubblico, pertanto non è richiesta alcuna selezione.

Per impostare la divisione del credito, selezionare **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Divisione credito]**. Puoi quindi selezionare le opzioni appropriate per ogni caso d’uso. Al termine, seleziona **[!UICONTROL Salva]** per salvare le modifiche.

![Finestra di dialogo Divisione crediti con opzioni nell&#39;area di lavoro delle impostazioni della connessione.](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}

+++

+++Accordi

Devi confermare che esiste un accordo legale tra te e il tuo collaboratore. Questo accordo delinea i termini della condivisione dei dati e della collaborazione. È possibile selezionare la casella di controllo **[!UICONTROL Conferma e conferma]** per confermare l&#39;esistenza dell&#39;accordo.

![La sezione Contratto legale viene evidenziata e confermata nell&#39;area di lavoro connessione.](/help/assets/connect/establish-connection/legal-agreement.png){zoomable="yes"}

+++

+++Nomi inserzionisti

>[!NOTE]
>
>Questa opzione può essere visualizzata durante la configurazione delle impostazioni di connessione o la revisione delle impostazioni di connessione, a seconda di chi avvia la connessione.

Se sei un editore che forma una connessione con un inserzionista, puoi scegliere di aggiungere i nomi degli inserzionisti nelle impostazioni di connessione. Questo consente di aggiungere più nomi con cui l’inserzionista è noto nei tuoi sistemi. Ciò è particolarmente utile se l&#39;inserzionista è presente in più aree geografiche o se è noto con nomi diversi in contesti diversi. Successivamente, quando crei un progetto, puoi selezionare il nome dell’inserzionista appropriato dall’elenco di nomi configurati nelle impostazioni di connessione.

![I nomi degli inserzionisti nell&#39;area di lavoro delle impostazioni della connessione.](/help/assets/connect/establish-connection/advertiser-names.png){zoomable="yes"}

Per aggiungere i nomi degli inserzionisti, seleziona **[!UICONTROL Modifica]** nella sezione **[!UICONTROL Nomi inserzionisti]**. Puoi quindi immettere l&#39;**[!UICONTROL ID inserzionista]** che l&#39;inserzionista è noto come nel tuo sistema e un **[!UICONTROL nome inserzionista]** da associare a tale ID in Collaboration. È possibile aggiungere più nomi di inserzionisti selezionando l&#39;opzione **[!UICONTROL Aggiungi]**.

![Finestra di dialogo Nomi inserzionista con opzioni nell&#39;area di lavoro delle impostazioni della connessione.](/help/assets/connect/establish-connection/advertiser-names-dialog.png){zoomable="yes"}

Al termine, seleziona **[!UICONTROL Salva]** per salvare le modifiche.

Durante la creazione di un progetto, il nome dell’inserzionista verrà precompilato in base alle seguenti impostazioni stabilite durante la connessione    :

1. **Nessun nome inserzionista impostato**: se non viene aggiunto alcun nome di inserzionista, per impostazione predefinita Collaboration utilizza il nome dell&#39;inserzionista come nome dell&#39;inserzionista.
2. **Un nome di inserzionista impostato**: se viene aggiunto un singolo nome di inserzionista, Collaboration utilizza automaticamente tale nome come nome dell&#39;inserzionista per il progetto.
3. **Più nomi inserzionisti impostati**: se vengono aggiunti più nomi inserzionisti, è possibile selezionare uno qualsiasi dei nomi specificati durante la creazione del progetto.

>[!NOTE]
>
> Dopo aver inviato le impostazioni di connessione, non è più possibile aggiungere o modificare i nomi degli inserzionisti.

![L&#39;area di lavoro delle impostazioni di connessione con la sezione Nomi inserzionisti è stata compilata.](/help/assets/connect/establish-connection/add-advertiser-names.png)

+++

Dopo aver effettuato le selezioni, selezionare **[!UICONTROL Invia]** per inviare le impostazioni suggerite al destinatario per la revisione.

### Rivedi impostazioni di connessione {#review-connection-settings}

Successivamente, il destinatario deve rivedere le impostazioni di connessione proposte dal proprietario. Il destinatario può eseguire questa operazione passando alla scheda **[!UICONTROL Le mie connessioni]** nell&#39;area di lavoro **[!UICONTROL Connetti]**. La connessione verrà visualizzata nella sezione **[!UICONTROL Azione richiesta]**. Selezionare **[!UICONTROL Rivedi impostazioni connessione]** per rivedere le impostazioni di connessione proposte.

![L&#39;area di lavoro Le mie connessioni con l&#39;opzione Controlla impostazioni connessione evidenziata.](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}

Esaminare le impostazioni proposte dal collaboratore. È possibile accettare o rifiutare le impostazioni di connessione. Se si rifiutano le impostazioni di connessione, sarà necessario comunicare con il collaboratore le modifiche che si desidera apportare all&#39;esterno del prodotto. Le informazioni di contatto del collaboratore vengono visualizzate nella sezione **[!UICONTROL Contatto]** dell&#39;area di lavoro delle impostazioni di connessione. Il proprietario può quindi rivedere le impostazioni di connessione e inviarle nuovamente per la revisione.

Se si è soddisfatti delle impostazioni di connessione proposte, è necessario confermare che è in vigore un accordo legale tra l&#39;utente e il collaboratore. Selezionare la casella di controllo **[!UICONTROL Conferma e conferma]** per confermare l&#39;esistenza dell&#39;accordo.

![La sezione relativa all&#39;accordo legale è evidenziata nell&#39;area di lavoro delle impostazioni di connessione.](/help/assets/connect/establish-connection/legal-agreement-review.png){zoomable="yes"}

Inoltre, se sei un editore che si connette con un inserzionista, ora puoi aggiungere i nomi degli inserzionisti nelle impostazioni di connessione. Per ulteriori informazioni su questo processo, vedere la sezione [impostazioni di connessione](#connection-settings).

>[!NOTE]
>
> Una volta accettate le impostazioni di connessione, non sarà più possibile aggiungere o modificare i nomi degli inserzionisti.

Selezionare **[!UICONTROL Accetta]** per continuare la connessione. Lo stato della connessione passerà a **[!UICONTROL Attivo]** e ora puoi iniziare a collaborare ai progetti.

## Elimina connessioni {#delete-connections}

È possibile eliminare le connessioni con i collaboratori che non si desidera continuare a utilizzare. Per eliminare le connessioni esistenti, passare a **[!UICONTROL Connetti]**. In qualità di editore, verrà visualizzata la connessione esistente. In qualità di inserzionista, devi quindi passare a **[!UICONTROL Le mie connessioni]**.

Selezionare **[!UICONTROL Visualizza connessione]** nella scheda di connessione che si desidera eliminare.

![L&#39;opzione Visualizza connessione è evidenziata nella visualizzazione Connessioni personali.](/help/assets/connect/establish-connection/delete-view-connection.png){zoomable="yes"}

Selezionare l&#39;icona Elimina ![icona Elimina](/help/assets/common/delete.svg) nell&#39;area di lavoro connessioni per eliminare la connessione.

![Icona Elimina evidenziata nell&#39;area di lavoro connessione.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

Viene visualizzata una finestra di dialogo di conferma in cui viene richiesto di confermare l’eliminazione della connessione. Seleziona **[!UICONTROL Elimina]** per confermare l&#39;eliminazione.

![Finestra di dialogo di conferma per eliminare una connessione.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Una volta eliminata la connessione, tutti i progetti esistenti nella collaborazione verranno eliminati definitivamente e non potranno essere ripristinati. La richiesta di connessione rimarrà in sospeso, ma la connessione e le relative configurazioni non saranno più attive. Se si desidera stabilire di nuovo la connessione con il collaboratore, è necessario ristabilire la connessione.

## Passaggi successivi

Dopo aver stabilito una connessione con il tuo collaboratore, ora tu e il tuo collaboratore potete [creare progetti](/help/guide/collaborate/manage-projects.md#create-project).
