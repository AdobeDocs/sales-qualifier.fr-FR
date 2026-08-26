---
title: Configurer les points forts marketing
description: Découvrez comment connecter Marketo à Sales Qualifier afin que les représentants puissent afficher et filtrer les prospects par activité de Marketo en direct dans les faits saillants marketing.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 8573d3891d5c8ec8a05637f160f120f933b0ec61
workflow-type: tm+mt
source-wordcount: 686
ht-degree: 3%

---


# Configurer les points forts marketing

Les mises en surbrillance marketing affichent l’activité de [!DNL Marketo] en direct de chaque prospect, comme les ouvertures d’e-mail et les clics, les visites web et les remplissages de formulaires, dans l’onglet **[!UICONTROL Mises en surbrillance marketing]** d’un prospect dans Sales Qualifier. Cet article explique comment connecter votre instance [!DNL Marketo] afin que l’activité se propage.

>[!IMPORTANT]
>
>Pour effectuer cette configuration, vous devez accéder au Adobe Developer Console et à **[!UICONTROL Admin]** dans [!DNL Marketo]. Contactez votre contact Adobe et votre administrateur [!DNL Marketo] pour effectuer les quatre étapes ci-dessous.

La configuration se compose de quatre parties :

* Partie A : création d’informations d’identification d’API dans le Adobe Developer Console.
* Partie B : Rassemblez votre point d’entrée et vos identifiants Sales Qualifier.
* Partie C : configuration d’un webhook dans [!DNL Marketo Engage].
* Partie D : ajout du webhook à un déclencheur de campagne intelligente.

Une fois la configuration terminée, les utilisateurs voient et filtrent cette activité sur **[!UICONTROL Prospects]** > **[!UICONTROL Caractéristiques marketing]**.

## Partie A : création d’informations d’identification d’API {#part-a-create-api-credentials}

Ces informations d’identification [!DNL Marketo] permettent de s’authentifier en toute sécurité auprès de Sales Qualifier.

Pour créer les informations d’identification :

1. Accédez à [Adobe Developer Console](https://developer.adobe.com/console/) et connectez-vous avec votre Adobe ID.
1. Sélectionnez **[!UICONTROL Créer un projet]** ou ouvrez un projet existant.
1. Sélectionnez **[!UICONTROL Modifier le projet]**, renommez le projet en un élément identifiable, tel que `Sales Qualifier Marketing Highlights`, puis sélectionnez **[!UICONTROL Enregistrer]**.
1. Sélectionnez **[!UICONTROL Ajouter une API]**, sélectionnez **[!UICONTROL API Experience Platform]** puis **[!UICONTROL Suivant]**.
1. Choisissez **[!UICONTROL OAuth serveur à serveur]** comme type d’authentification, puis sélectionnez **[!UICONTROL Suivant]**.

   **[!UICONTROL OAuth de serveur à serveur]** [!DNL Marketo] permet d’appeler l’API Sales Qualifier directement depuis son serveur, sans nécessiter qu’une personne se connecte.

1. Saisissez un nom d’identification de 45 caractères ou moins, tel que `Sales Qualifier Marketing Highlights Creds`.
1. Sélectionnez le profil de produit à associer, puis sélectionnez **[!UICONTROL Enregistrer l’API configurée]**.
1. Sous **[!UICONTROL Informations d’identification connectées]**, ouvrez les informations d’identification **[!UICONTROL OAuth de serveur à serveur]**. Sélectionnez **[!UICONTROL Récupérer le secret client]**, puis copiez les **[!UICONTROL ID client]** et **[!UICONTROL Secret client]**. Vous utilisez ces valeurs dans [Partie C](#part-c-configure-the-marketo-webhook).

>[!WARNING]
>
>Gardez le secret client privé. Traitez-le comme un mot de passe et ne l’envoyez pas par e-mail. Utilisez le canal sécurisé approuvé de votre organisation pour le partager avec la personne qui configure le webhook.

## Partie B : rassembler votre point d’entrée et vos identifiants {#part-b-gather-your-endpoint-and-identifiers}

Vous avez besoin de trois valeurs pour [Partie C](#part-c-configure-the-marketo-webhook) :

* **URL du point d’entrée** : adresse du webhook Sales Qualifier pour votre région.
* **ID d’organisation IMS** : identifiant de votre organisation dans le système Adobe Identity Management (IMS), sous la forme `{ORG_ID}@AdobeOrg`.
* **Nom du sandbox** : nom de votre sandbox AEP tel qu’il apparaît dans l’URL de Sales Qualifier (valeur de `sname`), et non pas nom d’affichage affiché dans l’interface utilisateur. Utilisez la valeur d’URL en minuscules, par exemple `prod`, et non `Prod`.

| Zone géographique | URL du point d’entrée Webhook |
| --- | --- |
| Amérique du Nord | `https://5r6xakp9k3.execute-api.us-east-1.amazonaws.com/prod/external/marketo/signals` |
| EMEA | `https://pc72i8q1k3.execute-api.eu-west-1.amazonaws.com/prod/external/marketo/signals` |
| APAC / Australie | `https://5cxxxyqlai.execute-api.ap-southeast-2.amazonaws.com/prod/external/marketo/signals` |

{style="table-layout:auto"}

Si vous n’êtes pas sûr de votre région, de votre ID d’organisation IMS ou du nom du sandbox, votre contact Adobe peut les confirmer.

## Partie C : configuration du webhook Marketo {#part-c-configure-the-marketo-webhook}

Pour créer le webhook :

1. Dans [!DNL Marketo], sélectionnez **[!UICONTROL Admin]** > **[!UICONTROL Webhooks]**.
1. Sélectionnez **[!UICONTROL Nouveau Webhook]**.
1. Définissez **[!UICONTROL URL]** sur l’URL du point d’entrée pour votre région à partir de [Partie B](#part-b-gather-your-endpoint-and-identifiers).
1. Définissez **[!UICONTROL Type de demande]** sur `POST`.
1. Définissez **[!UICONTROL Encodage du jeton de requête]** sur `JSON`. Ce paramètre est obligatoire.
1. Collez le modèle de payload ci-dessous dans **[!UICONTROL Modèle]**. Utilisez le **[!UICONTROL Insérer un jeton]** de [!DNL Marketo] pour correspondre aux noms de champ de votre instance.

   >[!NOTE]
   >
   >Avec l’encodage JSON, n’entourez pas les jetons de chaîne de guillemets. [!DNL Marketo] les ajoute automatiquement.

   ```json
   {
     "leadId": {{lead.Id:default=0}},
     "email": {{lead.Email Address:default=}},
     "fullName": {{lead.Full Name:default=}},
     "company": {{company.Company Name:default=}},
     "title": {{lead.Job Title:default=}},
     "department": {{lead.Department:default=}},
     "country": {{lead.Country:default=}},
     "score": {{lead.Lead Score:default=0}},
     "rating": {{lead.Lead Rating:default=}},
     "leadStatus": {{lead.Lead Status:default=}},
     "leadSource": {{lead.Lead Source:default=}},
     "isCustomer": {{lead.Is Customer:default=false}},
     "industry": {{company.Industry:default=}},
     "annualRevenue": {{company.Annual Revenue:default=0}},
     "numEmployees": {{company.Num Employees:default=0}},
     "campaignId": {{campaign.id:default=0}},
     "campaignName": {{campaign.name:default=}},
     "programName": {{program.name:default=}},
     "occurredAt": {{system.dateTime:default=}},
     "munchkinId": {{system.munchkinId:default=}},
     "triggerName": {{trigger.Trigger Name:default=}},
     "crmId": {{lead.SFDC ID:default=}},
     "crmType": {{lead.SFDC Type:default=}},
     "crmOwnerEmail": {{lead.Lead Owner Email Address:default=}},
     "crmOwnerFirstName": {{lead.Lead Owner First Name:default=}},
     "crmOwnerLastName": {{lead.Lead Owner Last Name:default=}},
     "attributes": {
       "asset": {{trigger.Name:default=}},
       "link": {{trigger.Link:default=}},
       "subject": {{trigger.Subject:default=}},
       "webPage": {{trigger.Web Page:default=}},
       "category": {{trigger.Category:default=}},
       "details": {{trigger.Details:default=}},
       "sentBy": {{trigger.Sent By:default=}},
       "receivedBy": {{trigger.Received By:default=}},
       "referrer": {{trigger.Referrer:default=}},
       "searchEngine": {{trigger.Search Engine:default=}},
       "searchQuery": {{trigger.Search Query:default=}},
       "imDescription": {{lead.Last Interesting Moment Desc:default=}},
       "imType": {{lead.Last Interesting Moment Type:default=}},
       "imDate": {{lead.Last Interesting Moment Date:default=}},
       "imSource": {{lead.Last Interesting Moment Source:default=}},
       "chatAgentName": {{trigger.Agent Name:default=}},
       "chatAgentEmail": {{trigger.Agent Email:default=}},
       "chatConversationStatus": {{trigger.Conversation Status:default=}},
       "chatConversationSummary": {{trigger.Conversation Summary:default=}},
       "chatGoalName": {{trigger.Goal name:default=}},
       "chatMeetingStatus": {{trigger.meeting status:default=}},
       "chatScheduledFor": {{trigger.Scheduled For:default=}},
       "chatDocumentName": {{trigger.Document Name:default=}},
       "chatDocumentUrl": {{trigger.Document URL:default=}},
       "chatPageUrl": {{trigger.Page URL:default=}}
     }
   }
   ```

1. Sélectionnez **[!UICONTROL Actions Webhook]** > **[!UICONTROL Définir l’en-tête personnalisé]**, puis ajoutez les en-têtes suivants, à l’aide des valeurs de [Partie A](#part-a-create-api-credentials) et [Partie B](#part-b-gather-your-endpoint-and-identifiers) :

   | Header | Valeur |
   | --- | --- |
   | `Content-Type` | `application/json` |
   | `x-client-id` | Votre identifiant client |
   | `x-client-secret` | Votre Secret Client |
   | `x-gw-ims-org-id` | Votre identifiant imsOrg |
   | `x-sandbox-name` | Nom de votre sandbox |

   {style="table-layout:auto"}

1. Sélectionnez **[!UICONTROL Enregistrer]**.

## Partie D : ajout du webhook à un déclencheur de campagne intelligente {#part-d-add-the-webhook-to-a-trigger-smart-campaign}

Ajoutez une étape de flux **[!UICONTROL Call Webhook]** à une campagne intelligente de déclenchement, existante ou nouvelle. La liste dynamique se déclenche sur cette campagne et détermine les activités à envoyer à Sales Qualifier.

Pour ajouter le webhook :

1. Ouvrez un déclencheur de campagne intelligente existant ou créez-en un (**[!UICONTROL Activités marketing]** > **[!UICONTROL Nouveau]** > **[!UICONTROL Campagne intelligente]**).
1. Dans l’onglet **[!UICONTROL Liste dynamique]**, ajoutez le ou les déclencheurs des activités à envoyer, par exemple **[!UICONTROL Clics sur le lien dans l’e-mail]**, **[!UICONTROL Remplit le formulaire]** ou **[!UICONTROL Page web des visites]**.
1. Dans l’onglet **[!UICONTROL Flux]**, ajoutez une étape **[!UICONTROL Appeler le Webhook]** et sélectionnez le webhook que vous avez créé dans [Partie C](#part-c-configure-the-marketo-webhook).
1. Activez la campagne intelligente.

L’activité de cette campagne intelligente se propage désormais dans Sales Qualifier. Les représentants voient et filtrent cette activité sur **[!UICONTROL Prospects]** > **[!UICONTROL Caractéristiques marketing]**.

>[!MORELIKETHIS]
>
>* [Gérer les intégrations](integrations.md)
>* [Prospects](prospects.md)
>* [Commencer](getting-started.md)
