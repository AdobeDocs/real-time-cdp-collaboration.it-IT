---
title: Configura [!DNL Snowflake] per Audience Sourcing
description: Scopri come configurare e collegare  [!DNL Snowflake Secure Data Share]  come origine dati self-service per acquisire i dati sul pubblico in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilità limitata" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 11a73116-4919-48a3-bf44-de2a10c102c1
source-git-commit: 7ce74c7f87432c026e673c2197b0b8c3f91fb6f0
workflow-type: tm+mt
source-wordcount: '1586'
ht-degree: 4%

---

# Configura [!DNL Snowflake] per audience sourcing

Scopri come configurare e collegare [!DNL Snowflake Secure Data Share] nell&#39;interfaccia utente di Adobe Real-Time CDP Collaboration per l&#39;origine dei dati sul pubblico per l&#39;analisi di attivazione e sovrapposizione.

## Panoramica {#overview}

[!DNL Snowflake] è una delle opzioni supportate per l&#39;origine dei dati del pubblico primario in Collaboration. Altri metodi disponibili includono l&#39;approvvigionamento dei tipi di pubblico da [Experience Platform](./onboard-audiences.md), la connessione di un [[!DNL AWS S3] bucket](./configure-aws-s3-audience-sourcing.md) o il caricamento di un [file CSV](./upload-csv-audience-sourcing.md).

Segui i passaggi seguenti per connettere [!DNL Snowflake Secure Data Share] e creare l&#39;origine dei dati sul pubblico in Collaboration. Una volta completata la configurazione, puoi rivedere, attivare e gestire i tipi di pubblico di origine per i progetti di collaborazione.

## Prerequisiti {#prerequisites}

Prima di configurare la connessione [!DNL Snowflake], verificare di soddisfare i seguenti prerequisiti:

* Hai creato [!DNL Snowflake Share] e configurato le autorizzazioni necessarie nel tuo account [!DNL Snowflake] per concedere l&#39;accesso Adobe al tuo [!DNL Snowflake Secure Data Share]. Scopri [come configurare [!DNL Snowflake] le autorizzazioni](#set-up-snowflake-permissions).
* Sono pronti i seguenti [!DNL Snowflake Share] valori:

   * **Nome condivisione**
   * **Identificatore account**
   * **Schema**
   * **Visualizza**

* I dati sul pubblico in [!DNL Snowflake Secure Data Share] devono soddisfare i requisiti di formato descritti nella [Guida alle specifiche di Audience Sourcing (v1.3)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1_3.pdf).
* Tutte le chiavi di corrispondenza nel file del pubblico [!DNL Snowflake] devono essere abilitate anche per il tuo account Collaboration. Scopri come [abilitare le chiavi di corrispondenza](./onboard-account.md#set-up-match-keys) o [aggiungere nuove chiavi di corrispondenza](./onboard-account.md#edit-match-keys) al tuo account.

## Configura autorizzazioni [!DNL Snowflake] {#setup-snowflake-permissions}

[!DNL Snowflake Secure Data Share] consente di condividere dati in tempo reale e di sola lettura in modo sicuro tra gli account [!DNL Snowflake], senza dover copiare o spostare i dati. Per concedere l&#39;accesso Adobe a [!DNL Secure Data Share], assicurati di configurare le autorizzazioni appropriate nell&#39;account [!DNL Snowflake].

Prima di procedere, verificare quanto segue:

* Si dispone dell&#39;accesso a un account [!DNL Snowflake].
* Il tuo account [!DNL Snowflake] è abbonato a inserzioni private. Per configurare le autorizzazioni necessarie è necessario disporre dei privilegi di amministratore per Snowflake.
* Conosci il provider cloud e l&#39;area geografica dell&#39;account [!DNL Snowflake].

Per ulteriori informazioni sulle autorizzazioni necessarie, leggere la [[!DNL Snowflake] documentazione](https://docs.snowflake.com/en/collaboration/consumer-listings-access#access-a-private-listing).

### Raccogli informazioni account [!DNL Snowflake] di Adobe {#collect-account-information}

Per iniziare, individuare e annotare l&#39;identificatore dell&#39;account Adobe [!DNL Snowflake] corrispondente alla propria area geografica. Questo identificatore sarà necessario per concedere l’accesso ad Adobe nei passaggi successivi.

| Area geografica | Identificatore completo dell&#39;account di produzione [!DNL Snowflake] |
| ------------- | --------------- |
| America del Nord | ADOBE.AGORA_SF_02 |
| EMEA | ADOBE.RTCDP_COLLABORATION_DEU1_EXTERNAL |
| Australia | ADOBE.RTCDP_COLLABORATION_AUS3_EXTERNAL |

{style="table-layout:auto"}

### Crea e concedi l&#39;accesso a [!DNL Snowflake Share] {#create-grant-access-to-share}

Quindi, segui questi passaggi per creare un [!DNL Secure Data Share] nel tuo account [!DNL Snowflake] e concedere ad Adobe l&#39;accesso in sola lettura ai tuoi dati sul pubblico.

1. Crea una vista protetta con accesso limitato solo alle colonne necessarie dalla tabella di origine.

   ```sql
   CREATE OR REPLACE SECURE VIEW my_database.my_schema.secure_view_for_adobe AS
   SELECT 
       column1,
       column2,
       column3
   FROM my_database.my_schema.source_table;
   ```

2. Crea un nuovo [!DNL Snowflake Secure Data Share].

   ```sql
   CREATE OR REPLACE SHARE adobe_data_share;
   ```

3. Concedere il privilegio USAGE sul database a [!DNL Snowflake Secure Data Share] in modo che possa accedere agli oggetti nel database.

   ```sql
   GRANT USAGE ON DATABASE my_database TO SHARE adobe_data_share;
   ```

4. Concedere l&#39;utilizzo dello schema a [!DNL Snowflake Secure Data Share] in modo che possa accedere agli oggetti all&#39;interno dello schema.

   ```sql
   GRANT USAGE ON SCHEMA my_database.my_schema TO SHARE adobe_data_share;
   ```

5. Concedi i privilegi SELECT sulla visualizzazione protetta a [!DNL Snowflake Secure Data Share] in modo che Adobe possa leggere i tuoi dati sul pubblico.

   ```sql
   GRANT SELECT ON VIEW my_database.my_schema.secure_view_for_adobe TO SHARE adobe_data_share;
   ```

6. Aggiungi l&#39;account [!DNL Snowflake] di Adobe a [!DNL Snowflake Secure Data Share] utilizzando l&#39;identificatore corretto per la tua area geografica. Consulta [la tabella di mappatura regione/account precedente](#collect-account-information).

   ```sql
   ALTER SHARE adobe_data_share ADD ACCOUNTS = <Account Identifier based on region from the mapping table>;
   ```

### Raccogli dettagli di [!DNL Snowflake Share] {#collect-share-details}

Raccogliere infine i dettagli per [!DNL Snowflake Share] come illustrato nella tabella seguente. Queste informazioni sono necessarie per configurare la connessione tra [!DNL Snowflake Share] e Collaboration.

| Campo | Esempio |
| -------------------------- | --------------- |
| Identificatore account | CUSTOMER_ORG.CUSTOMER_SNOWFLAKE_ACCOUNT |
| Nome [!DNL Share] | adobe_data_share |
| Nome schema | schema_cliente |
| Nome visualizzazione | secure_view_for_adobe |

{style="table-layout:auto"}

## Configura la connessione [!DNL Snowflake] {#configure-snowflake-connection}

Dopo aver completato la [configurazione delle autorizzazioni di Snowflake](#set-up-snowflake-permissions) e aver verificato che tutti i [prerequisiti](#prerequisites) siano soddisfatti, ora puoi connettere [!DNL Snowflake Secure Data Share] a Collaboration per iniziare a creare l&#39;origine dei tipi di pubblico.

Dalla scheda **[!UICONTROL Tipi di pubblico]** nell&#39;area di lavoro **[!UICONTROL Configurazione]**, selezionare l&#39;icona Aggiungi (![Icona Aggiungi.](/help/assets/icons/plus.png)) e quindi seleziona **[!UICONTROL Pubblico]**.

Se questo è il tuo primo pubblico, puoi anche selezionare l&#39;opzione **[!UICONTROL Aggiungi pubblico]**.

![Scheda Pubblico personale nell&#39;area di lavoro di configurazione con l&#39;icona Aggiungi e l&#39;opzione Aggiungi pubblico visualizzate.](../../assets/setup/snowflake-audience-sourcing/add-audience.png)

Viene visualizzato il flusso di lavoro Aggiungi pubblico. Seleziona **[!UICONTROL Aggiungi una nuova connessione dati]**, quindi seleziona **[!UICONTROL Avanti]**.

![L&#39;area di lavoro Aggiungi tipi di pubblico con l&#39;opzione Aggiungi una nuova connessione dati evidenziata.](../../assets/setup/snowflake-audience-sourcing/add-data-connection.png){zoomable="yes"}

### Seleziona [!DNL Snowflake] come connessione dati {#select-snowflake}

Selezionare **[!UICONTROL Snowflake]** come connessione dati, quindi **[!UICONTROL Next]**.

![Schermata di selezione della connessione dati con [!DNL Snowflake] disponibile come opzione selezionabile.](../../assets/setup/snowflake-audience-sourcing/select-snowflake-data-connection.png)

### Rivedere il file del pubblico {#review-audience-file}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sourcing_specifications_snowflake"
>title="Preparazione dei dati per l’onboarding"
>abstract="Leggi la guida sulle specifiche di acquisizione del pubblico per scoprire come formattare e strutturare i dati sul pubblico da Snowflake per Collaboration."
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-audience-sourcing" text="Consulta la guida"

Viene visualizzata una finestra di dialogo in cui vengono illustrati i requisiti di [!DNL Snowflake Share] e del file del pubblico [!DNL Snowflake] prima che sia possibile iniziare a creare l&#39;origine. Assicurati che [!DNL Snowflake Share] sia stato creato con il nome di condivisione, l&#39;identificatore dell&#39;account, lo schema e la visualizzazione corretti. Per verificare che i dati del pubblico siano formattati e strutturati correttamente per l&#39;utilizzo in Collaboration, consulta la **[[!UICONTROL guida alle specifiche di Audience Sourcing]](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1_3.pdf)**.

Al termine, seleziona **[!UICONTROL Avvia onboarding]**.

![Prepara [!DNL Snowflake Share] per la finestra di dialogo di onboarding con un collegamento alle specifiche di Audience Sourcing.](../../assets/setup/snowflake-audience-sourcing/prepare-snowflake-share-onboarding-dialog.png)

### Autentica connessione [!DNL Snowflake Share] {#authenticate-snowflake-share-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sharing_snowflake"
>title="Aggiungi pubblico da Snowflake"
>abstract="Per collegare la condivisione Snowflake, autorizza l’utente del servizio Adobe a recuperare i dati sul pubblico per l’elaborazione. Segui i passaggi descritti in Experience League per concedere ad Adobe l’accesso al tuo Snowflake Share."

In questo passaggio, devi fornire le credenziali [!DNL Snowflake Share] necessarie per connettere [!DNL Snowflake Share] a Collaboration:

| Campo | Descrizione | Esempio |
|--------------------|-------------|------------------------------|
| Nome condivisione | Nome di [!DNL Snowflake Share]. | `ADOBE_DATA_SHARE` |
| Identificatore account | L’identificatore univoco del tuo account Snowflake. | `CUSTOMER_ORG.CUSTOMER_SNOWFLAKE_ACCOUNT` |
| Schema | Lo schema all&#39;interno di [!DNL Snowflake Share] che contiene i dati del pubblico. | `CUSTOMER_SCHEMA` |
| Visualizzazione | Il set di dati effettivo che Collaboration estrae dai dati del pubblico. | `SECURE_VIEW_FOR_ADOBE` |

{style="table-layout:auto"}

Dopo aver immesso tutte le credenziali richieste, seleziona **[!UICONTROL Avanti]**.

![Il modulo di connessione [!DNL Snowflake Share] con i campi Nome condivisione, Identificatore account, Schema e Visualizza è stato compilato ed è stato evidenziato il pulsante Avanti.](../../assets/setup/snowflake-audience-sourcing/snowflake-authentication-credentials-form.png)

Nella parte inferiore della pagina successiva viene visualizzata una finestra di dialogo di conferma che conferma la connessione di [!DNL Snowflake Share] a Collaboration.

![Una finestra di dialogo di conferma conferma conferma che la connessione [!DNL Snowflake Share] è stata stabilita correttamente.](../../assets/setup/snowflake-audience-sourcing/snowflake-share-connection-established.png)

### Fornisci nome e descrizione {#provide-name-description}

Nella visualizzazione **[!UICONTROL Fornisci dettagli]**, immetti un nome descrittivo e una descrizione facoltativa per la connessione dati [!DNL Snowflake]. Al termine, selezionare **[!UICONTROL Avanti]**.

![Nella schermata dei dettagli vengono visualizzati il nome e la descrizione della connessione dati, con il pulsante Avanti evidenziato.](../../assets/setup/snowflake-audience-sourcing/provide-name-description.png)

### Mappare i campi {#map-fields}

La schermata **[!UICONTROL Mapping]** è di sola lettura in questo momento. Non è possibile aggiungere, eliminare o applicare trasformazioni. Collaboration mappa automaticamente i campi di identità di origine dai dati di [!DNL Snowflake Share] ai campi di destinazione in base alla **[specifica di origine del pubblico (v1.3)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1_3.pdf)**.

Conferma visivamente i campi mappati e seleziona **[!UICONTROL Avanti]** per continuare. Puoi anche visualizzare in anteprima i dati di esempio di [!DNL Snowflake Share] con l&#39;opzione **[!UICONTROL Anteprima dati di origine]**.

![Nella schermata Mappa campi vengono visualizzati i campi di origine e di destinazione mappati automaticamente, con le opzioni Anteprima dati di origine e Successivo evidenziate.](../../assets/setup/snowflake-audience-sourcing/map-fields-screen.png)

Quando si sceglie di visualizzare l&#39;anteprima, viene visualizzata la finestra di dialogo Anteprima dati **[!UICONTROL [!DNL Snowflake Share]]** con dati di esempio in formato tabulare. Rivedi, quindi seleziona **[!UICONTROL Chiudi]**.

La finestra di dialogo di anteprima dei dati di ![[!DNL Snowflake Share] mostra i dati di esempio di [!DNL Snowflake Share] ed è evidenziata l&#39;opzione Chiudi.](../../assets/setup/snowflake-audience-sourcing/preview-source-data.png)

<!-- NOTE: Manual mapping will be available in the future. -->
<!-- In the **[!UICONTROL Map fields]** screen, you can use the **[!UICONTROL Source field]** and **[!UICONTROL Target field]** dropdowns to update the auto-mapped fields, or include additional fields with the **[!UICONTROL Add field]** option. Once finished, select **[!UICONTROL Next]**. -->

<!-- ![The Map fields screen showing the mapped fields with the Next option highlighted.](../../assets/setup/snowflake-audience-sourcing/map-fields.png) -->

### Pianificazione della frequenza di aggiornamento e dell’intervallo di date {#refresh-frequency-date-range}

Nella visualizzazione **[!UICONTROL Pianificazione]**, utilizzare il menu a discesa per selezionare la frequenza di aggiornamento da uno a sei giorni. Quindi utilizza l’icona del calendario per specificare le date di inizio e fine per il pubblico di sourcing.

>[!IMPORTANT]
>
>Per gestire in modo efficace i crediti Collaboration, impostare la frequenza di aggiornamento in modo che corrisponda o non superi la frequenza di aggiornamento dei dati [!DNL Snowflake] sottostanti. L&#39;intervallo minimo di aggiornamento supportato è una volta ogni sei giorni.

![Nella schermata Pianifica vengono evidenziate le configurazioni della frequenza di aggiornamento e dell&#39;intervallo di date e l&#39;opzione Avanti.](../../assets/setup/snowflake-audience-sourcing/refresh-frequency-date-range.png)

### Verifica e completa la connessione {#review-and-complete}

Infine, controlla le impostazioni di configurazione nella schermata di riepilogo. Questa visualizzazione contiene un riepilogo delle sezioni riportate di seguito.

* **[!UICONTROL Connessione dati]**: visualizza il nome di condivisione, l&#39;identificatore dell&#39;account, lo schema e la visualizzazione di [!DNL Snowflake Share].
* **[!UICONTROL Dettagli]**: visualizza il nome e la descrizione facoltativa della connessione dati per consentirne l&#39;identificazione in un secondo momento.
* **[!UICONTROL Mappatura]**: visualizza la mappatura dei campi sorgente dal file del pubblico ai campi di destinazione utilizzati in Collaboration.
* **[!UICONTROL Pianificazione]**: visualizza la frequenza con cui la connessione aggiorna i dati del pubblico e l&#39;intervallo di date attivo per la determinazione origine.

Se devi modificare una sezione, seleziona l&#39;icona della matita (![icona Modifica](/help/assets/icons/edit.png)). Seleziona **[!UICONTROL Completa]** per confermare tutte le sezioni.

![Nella schermata di revisione viene visualizzato un riepilogo delle impostazioni di connessione dati, dettagli, mapping e pianificazione, con l&#39;opzione Completa evidenziata.](../../assets/setup/snowflake-audience-sourcing/review-settings.png)

Una finestra di dialogo di conferma conferma conferma che la connessione dati è stata creata correttamente e che l’origine del pubblico è in corso.

## Rivedere i tipi di pubblico originati {#review-sourced-audiences}

Al termine dell&#39;installazione, Collaboration inizia a raccogliere i tipi di pubblico da [!DNL Snowflake Share]. Se l&#39;origine del pubblico è in corso, nella parte superiore della visualizzazione viene visualizzato un banner.

![La scheda Tipi di pubblico mostra il banner Determinazione origine pubblico in corso.](../../assets/setup/snowflake-audience-sourcing/audience-sourcing-in-progress.png)

>[!TIP]
>
>Il tempo di Audience sourcing varia in base alle dimensioni dei dati di [!DNL Snowflake] e alla frequenza di aggiornamento configurata. Set di dati più grandi o pianificazioni di aggiornamento meno frequenti potrebbero richiedere più tempo per essere visualizzati nell&#39;area di lavoro **[!UICONTROL I miei tipi di pubblico]**.

Al termine dell&#39;operazione di sourcing, i tipi di pubblico sono disponibili nella scheda **[!UICONTROL Tipi di pubblico]** con le stesse caratteristiche e informazioni dei tipi di pubblico di Experience Platform.

![La scheda Tipi di pubblico personali mostra un elenco dei tipi di pubblico di origine nella visualizzazione a tabella.](../../assets/setup/snowflake-audience-sourcing/snowflake-audience-list.png)

In visualizzazione griglia o tabella, selezionare un elemento riga o **[!UICONTROL Visualizza pubblico]** per visualizzare una panoramica di un pubblico specifico. Vengono visualizzati lo stato, l&#39;origine e il nome della connessione dati del pubblico, insieme ai pannelli dettagliati per **[!UICONTROL Identità]**, **[!UICONTROL Categorie]**, **[!UICONTROL Accesso alla connessione]** e **[!UICONTROL Visibilità metadati]**. Per informazioni dettagliate, consulta [come visualizzare un singolo pubblico](./onboard-audiences.md#view-individual-audiences).

Utilizza questa visualizzazione per confermare la configurazione del pubblico e le impostazioni di visibilità prima di utilizzarlo nei progetti di collaborazione.

## Visualizza connessione dati [!DNL Snowflake] {#view-snowflake-connection}

La connessione [!DNL Snowflake] appena aggiunta è immediatamente disponibile nella scheda **[!UICONTROL Le mie connessioni dati]**. L&#39;origine del pubblico viene visualizzata come [!UICONTROL [!DNL Snowflake]].

La connessione dati [!DNL Snowflake] include le stesse funzionalità e gli stessi dettagli delle altre connessioni dati del pubblico. Ulteriori informazioni su [come visualizzare e gestire le connessioni dati](../setup/manage-data-connection.md).

![La scheda Connessioni dati mostra la connessione dati [!DNL Snowflake] con le informazioni sullo stato dell&#39;origine.](../../assets/setup/snowflake-audience-sourcing/data-connection-tab-snowflake.png)

## Passaggi successivi {#next-steps}

Configurazione e connessione di [!DNL Snowflake] come origine dati in Collaboration completata. Al termine dell&#39;approvvigionamento, puoi [creare progetti di collaborazione](../collaborate/manage-projects.md), [attivare tipi di pubblico](../collaborate/activate.md), [esaminare sovrapposizioni e approfondimenti](../collaborate/measure.md) e [gestire le impostazioni del pubblico e la visibilità](./onboard-audiences.md).

Per informazioni su altri metodi di determinazione origine del pubblico, consulta la seguente documentazione:

* [Configura [!DNL Amazon S3] per audience sourcing](./configure-aws-s3-audience-sourcing.md)
* [Tipi di pubblico di Source da Experience Platform](./onboard-audiences.md)
* [Carica file CSV per Audience sourcing](./upload-csv-audience-sourcing.md)
