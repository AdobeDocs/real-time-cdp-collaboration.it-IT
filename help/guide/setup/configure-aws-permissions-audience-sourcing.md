---
title: Configurare le autorizzazioni di AWS per Audience Sourcing
description: Scopri come configurare le autorizzazioni di AWS Identity and Access Management (IAM) per concedere ad Adobe un accesso sicuro e in sola lettura al tuo  [!DNL Amazon S3]  bucket per l’audience sourcing in Real-Time CDP Collaboration.
source-git-commit: 73f11b7341cf94540dc01f8803291f6dc3cd5038
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 1%

---

# Configurare le autorizzazioni di AWS per Audience sourcing

Usa questa guida per configurare i criteri e i ruoli di AWS Identity and Access Management (IAM) che consentono ad Adobe di accedere in modo sicuro e in sola lettura al bucket Amazon S3. Questo accesso consente a Real-Time CDP Collaboration di originare i tipi di pubblico dal bucket S3.

## Prerequisiti {#prerequisites}

Prima di continuare, verifica di soddisfare i seguenti requisiti e di avere accesso alle informazioni richieste.

### Autorizzazioni AWS richieste

Per completare la configurazione, il tuo account deve disporre dell’accesso di amministratore AWS. L’accesso come amministratore consente di creare e gestire i criteri e i ruoli IAM necessari per autorizzare l’accesso di Adobe al bucket S3. Se non disponi dei privilegi di amministratore, contatta l’amministratore di AWS prima di procedere.

### Informazioni richieste

Man mano che procedi nei passaggi seguenti, tieni presente quanto segue. Questi dettagli sono utilizzati nella [[!DNL Amazon S3] guida dell&#39;interfaccia utente di audience sourcing](./configure-aws-s3-audience-sourcing.md).

* Il nome del bucket S3 in cui sono memorizzati i file del pubblico.
* Il percorso della cartella (prefisso) in cui si trovano i file del pubblico.
* Nome risorsa Amazon (ARN) per il nuovo ruolo IAM creato, ad esempio: `arn:aws:s3:::my-company-data/audience-files/`

>[!TIP]
>
>Un ARN (Amazon Resource Name) identifica in modo univoco le risorse AWS, come i bucket S3 e i ruoli IAM. Utilizza il formato seguente per specificare il bucket e il percorso della cartella opzionale:
>
>```
>arn:aws:s3:::<bucket-name>/<optional-folder-path>
>```

## Creare un criterio IAM {#create-policy}

Per iniziare la configurazione, crea innanzitutto un criterio IAM che conceda **accesso in sola lettura** al bucket S3. Questa policy consente ad Adobe di leggere i file necessari per il audience sourcing ma non concede le autorizzazioni di scrittura o eliminazione.

Apri [AWS Management Console](https://aws.amazon.com/console/) e passa a **[!DNL IAM]** > **[!DNL Policies]** > **[!DNL Create policy]**.

Nell&#39;area di lavoro dei criteri di creazione di AWS, seleziona la scheda **JSON** e incolla il criterio di esempio seguente.

>[!NOTE]
>
>Sostituisci `<Your AWS ARN for bucket folder path>` e `<Your AWS ARN for bucket>` con ARN S3 specifici. Quando si specifica il percorso della cartella del bucket, includere `/*` alla fine dell&#39;ARN (ad esempio, `arn:aws:s3:::my-company-data/audience-files/*`). In questo modo Adobe può accedere a tutti i file e le sottocartelle all’interno del percorso di cartella specificato.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket",
        "s3:GetBucketLocation"
      ],
      "Resource": "<Your AWS ARN for bucket folder path>"
    },
    {
      "Sid": "Statement2",
      "Effect": "Allow",
      "Action": [
        "s3:ListBucket"
      ],
      "Resource": "<Your AWS ARN for bucket>"
    }
  ]
}
```

Rivedere le impostazioni dei criteri e selezionare **[!DNL Create policy]**. Registrare il nome del criterio da utilizzare in un passaggio successivo.

>[!TIP]
>
>Per individuare il nome del bucket e il percorso della cartella, apri **Amazon S3 Management Console**. Nella pagina **Bucket**, seleziona il nome del bucket per aprirlo. Nella visualizzazione **Oggetti** sono elencati i file e le cartelle e il percorso nella parte superiore della pagina mostra il percorso della cartella corrente.

## Creare un ruolo IAM {#create-role}

Creare un ruolo IAM e impostare il ruolo IAM di Real-Time CDP Collaboration AWS come **entità attendibile**. Questo consente ai servizi di Adobe di assumere il ruolo e leggere in modo sicuro i dati del pubblico S3.

Nella scheda **[!DNL IAM]** della console di gestione Amazon S3, passa a **[!DNL Roles]** > **[!DNL Create role]**.

In [!DNL Step 1] del flusso di lavoro [!DNL Create role], nella sezione **[!DNL Trusted entity type]**, selezionare **[!DNL Custom trust policy]**. Quindi, nell&#39;editor **[!DNL Custom trust policy]**, incolla il seguente esempio e sostituisci `<Adobe IAM Role ARN>` con il valore per la tua area geografica.

* ARN per il ruolo Adobe IAM appropriato per la tua area geografica:

| Area geografica | ARN per ruolo Adobe IAM |
|---------|-------------------|
| America del Nord | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-va6-role` |
| Australia | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-aus3-role` |
| EMEA | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-deu1-role` |

Esempio di criterio di attendibilità:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Principal": {
        "AWS": "<Adobe IAM Role ARN>"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

Rivedi il criterio e seleziona **Avanti** per continuare.

Nella sezione [!DNL Step 2] **[!DNL Add permissions]** del flusso di lavoro [!DNL Create role], cercare e allegare i criteri IAM creati [prima](#create-policy). Selezionare il criterio seguito da **[!DNL Next]** per continuare a [!DNL Step 3].

Nella sezione [!DNL Step 3] **[!DNL Name review, and create - Role details]**, fornire un nome di ruolo (ad esempio, `s3-iam-role`) e una descrizione facoltativa.

In questa pagina vengono visualizzati i criteri delle entità attendibili, il riepilogo dei criteri di autorizzazione e gli eventuali tag aggiunti per l&#39;organizzazione interna e il tracciamento.

Infine, selezionare **Crea ruolo** per confermare la configurazione.

>[!IMPORTANT]
>
>Dopo aver creato il ruolo, è necessario registrare il nome risorsa di Amazon (ARN). Dovrai fornire il ruolo IAM ARN durante il passaggio **Autentica la tua connessione S3** nel flusso di lavoro [Configura AWS S3 per Audience sourcing](./configure-aws-s3-audience-sourcing.md).

## Passaggi successivi {#next-steps}

Questa configurazione consente ad Adobe di accedere in sola lettura al bucket S3 e stabilisce una connessione affidabile con il ruolo IAM di Adobe.

Quindi, procedi a [Configurare AWS S3 per l&#39;origine del pubblico](./configure-aws-s3-audience-sourcing.md) per connettere il bucket S3 a Collaboration.

Per ulteriori informazioni sull&#39;origine dei tipi di pubblico, fare riferimento a [Source e gestire i tipi di pubblico](./onboard-audiences.md).
