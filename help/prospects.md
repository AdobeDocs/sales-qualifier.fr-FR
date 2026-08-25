---
title: Prospects dans Sales Qualifier
description: Découvrez comment créer, filtrer et examiner votre liste de prospects dans Sales Qualifier pour donner la priorité à la diffusion.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/zf2H5rq1JlIT26LqLPMrm2Mq3tSIrLOiTEw6BXb1w2U'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 08dd05e1d13b501d43d457e6217a43aaabdb1d0d
workflow-type: tm+mt
source-wordcount: 535
ht-degree: 2%

---


# Prospects

Sélectionnez **[!UICONTROL Prospects]** dans le volet de navigation de gauche pour afficher les prospects et les contacts auxquels vous pouvez accéder. Utilisez la liste pour consulter le statut de chaque prospect et sa dernière activité.

![Tableau des prospects affichant le statut du prospect et la dernière activité pour la gestion des prospects](./assets/prospects.png){width="800" zoomable="yes"}

* **[!UICONTROL Leads]** : leads qui vous sont affectés dans le CRM connecté.
* **[!UICONTROL Contacts]**—Contacts qui vous sont assignés dans le CRM connecté.
* **[!UICONTROL Liste des personnes]** : prospects que vous importez ou ajoutez manuellement.

## Création de votre liste de prospects

La liste des prospects regroupe des personnes provenant de plusieurs sources :

* **Prospects CRM** : Sales Qualifier importe automatiquement les leads et les contacts attribués à l’utilisateur connecté. Pour plus d&#39;informations, consultez la section [&#x200B; Intégrations &#x200B;](integrations.md).
* **Prospects importés**—Prospects importés à partir d&#39;un fichier CSV.
* **Prospects ajoutés manuellement**—Prospects ajoutés individuellement dans Sales Qualifier.

Pour ajouter des prospects qui ne proviennent pas de votre CRM :

1. Sur la page **[!UICONTROL Prospects]**, sélectionnez **[!UICONTROL Liste des personnes]**.
1. Sélectionnez **[!UICONTROL + Ajouter des personnes]** puis sélectionnez **[!UICONTROL Importer CSV]** ou **[!UICONTROL Ajouter une personne]**.

   * Pour un import CSV, chargez un fichier CSV au format `firstname,email`.
     Vous devez indiquer votre prénom et votre adresse e-mail. Le nom est facultatif. Le modèle CSV n’inclut pas la colonne d’ID de prospect CRM, mais vous pouvez ajouter la colonne et ses valeurs au fichier avant l’importation. Si l’importation échoue, consultez le message d’erreur pour les champs ou valeurs à corriger, puis chargez à nouveau le fichier.
   * Pour ajouter une personne manuellement, saisissez ses détails dans le formulaire.

1. Sélectionnez **[!UICONTROL Enregistrer]**.

## Filtrer et rechercher des prospects

Sélectionnez **[!UICONTROL Filtrer]** pour affiner la liste. Vous pouvez filtrer par :

* Statut du plan d’engagement
* Création par
* Titre du traitement
* Compte
* Source
* Dernière mise à jour

Les administrateurs peuvent également rendre les champs CRM mappés disponibles en tant que filtres. Dans **[!UICONTROL Paramètres d’administration]**, activez **[!UICONTROL Filtrable]** pour chaque champ que les représentants utilisent pour rechercher des prospects. Voir [&#x200B; Mappage des champs CRM &#x200B;](integrations.md#map-crm-fields-inbound-mapping).

Dans **[!UICONTROL Mes contacts d’opportunité]**, vous pouvez également filtrer les contacts par champs à partir des opportunités associées, telles que l’étape, le type et la date de fermeture. Les champs d’opportunité comportent des libellés tels que **[!UICONTROL Phase (Opportunité)]** qui les distinguent des champs de contact. Votre administrateur contrôle les champs d’opportunité disponibles en tant que filtres.

### Filtrer par engagement Marketo

Recherchez et hiérarchisez les prospects en fonction de leur engagement dans les [!DNL Marketo] en direct, tel que les ouvertures d’e-mail et les clics, les visites web, les remplissages de formulaires et les moments intéressants. L’engagement apparaît en temps quasi réel, comme cela se produit.

Pour filtrer les prospects par engagement Marketo :

1. Sélectionnez **[!UICONTROL Filtrer]**.
1. Ajoutez un filtre d’engagement [!DNL Marketo] et définissez le type d’activité, la campagne ou d’autres attributs pour vous concentrer sur l’engagement qui importe.

Chaque prospect montre sa dernière activité [!DNL Marketo] ainsi que son historique récent.

Le filtrage de l’engagement Marketo est disponible dans toutes les régions de production. Votre administrateur l’active pour votre organisation et votre sandbox, et un spécialiste marketing effectue une configuration unique dans [!DNL Marketo]. Voir [Activation du filtrage de l’engagement Marketo](integrations.md#turn-on-marketo-engagement-filtering).

## Consulter les détails du prospect

Sélectionnez un prospect pour ouvrir son profil. Examinez les signaux qui comptent avant de vous adresser à :

* **Résumé de personne par IA** : instantané écrit par IA du prospect ou du contact et de son engagement récent. Utilisez le résumé pour comprendre la personne en un coup d’œil avant de passer en revue les activités individuelles. Les résumés des personnes par IA sont disponibles sur les instances exécutant Adobe Journey Optimizer B2B edition Prime ou Ultimate.
* **Liste des activités**—Liste chronologique des activités et des comportements récents.
* **Vue Chronologie** : chronologie visuelle de l’engagement sur plusieurs canaux.
* **Contenu affiché** : pages Web et ressources consultées par le prospect. Sélectionnez un élément pour l’ouvrir.

>[!MORELIKETHIS]
>
>* [Comptes](accounts.md)
>* [Workflows sortants](outbound-workflows.md)
>* [Conversation IA](ai-assistant.md)
