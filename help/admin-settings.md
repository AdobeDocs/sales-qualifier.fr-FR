---
title: Paramètres d’administration
description: Découvrez comment gérer les champs CRM, la synchronisation des activités, le processus de désinscription aux e-mails et d’autres paramètres d’administration de Sales Qualifier.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/vbtO6I67ZEaZz3oio9InNErvq5D0wjbRxyDZpTq8Lzo'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4bid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
internal-label: Administration
source-git-commit: 483e57ab9d8f3f5e4201e0b691e37727a25d3f22
workflow-type: tm+mt
source-wordcount: 856
ht-degree: 0%

---


# Paramètres d’administration

Utilisez **[!UICONTROL Paramètres d’administration]** pour configurer les intégrations CRM, gérer le Centre de connaissances et configurer le processus de désinscription aux e-mails.

Sales Qualifier se connecte à Salesforce ou Microsoft Dynamics 365. La connexion donne au Account Qualification Agent (AQA) une vue cohérente des prospects, comptes, contacts, activités et propriétaires. Sales Qualifier peut également écrire des activités de sensibilisation et un statut d’opt-out dans le CRM et synchroniser les activités de sensibilisation avec Marketo.

Pour configurer les connexions CRM, le mappage des champs et la synchronisation des activités, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Paramètres d’administration]** > **[!UICONTROL Connexions CRM]**. Les utilisateurs standard peuvent utiliser les données et les filtres CRM configurés, mais ne peuvent pas modifier ces paramètres. Pour connecter un CRM pour la première fois, voir [Prise en main](getting-started.md#connect-your-crm).

>[!IMPORTANT]
>
>Pour accéder à **[!UICONTROL Paramètres d’administration]**, vous devez être membre des groupes d’utilisateurs `Sales Qualifier` et `Sales Qualifier Admins`.

## CRM MCP et le plug-in intégré

Sales Qualifier fonctionne avec votre CRM des manières suivantes :

* **Requêtes CRM MCP** : les requêtes Account Qualification Agent interrogent les données CRM actives afin que les réponses et les informations reflètent l’état actuel de vos enregistrements.
* **Plug-in intégré** : le plug-in CRM affiche des informations [!DNL Marketo Sales Insights] (MSI) et des données agentiques dans votre CRM. Utilisez le plug-in pour ajouter un prospect à Sales Qualifier.
* **Synchronisation des activités** : lorsqu’un administrateur active **[!UICONTROL Synchronisation des activités]**, les activités d’extension se synchronisent avec le CRM et Marketo.

## Étendue de l’accès CRM

Sales Qualifier lit les utilisateurs, les contacts, les mappages des propriétaires, les prospects, les comptes, les opportunités et les activités à partir du CRM. Il écrit uniquement les activités de sensibilisation consignées et le statut d’opt-out dans le CRM, et synchronise les activités de sensibilisation avec Marketo. Votre administrateur CRM prépare l’accès à l’API dans Salesforce ou Dynamics. Un administrateur Sales Qualifier se connecte ensuite au CRM, mappe les champs entrants et choisit de synchroniser ou non les activités.

>[!NOTE]
>
>Les étapes d’identification de la section [Prise en main](getting-started.md#connect-your-crm) décrivent l’accès en lecture aux objets CRM. Si vous activez la synchronisation des activités ou l’écriture différée d’opt-out, contactez votre administrateur CRM pour obtenir l’accès en écriture correspondant à celui requis par votre configuration CRM.

## Mappage des champs CRM (mapping entrant)

Une fois le CRM connecté, sélectionnez **[!UICONTROL Gérer]** pour la connexion et ouvrez **[!UICONTROL Mapping entrant]**. Le mappage entrant contrôle les champs CRM que Sales Qualifier extrait dans l’application.

1. Sélectionnez **[!UICONTROL Ajouter une section]**.
1. Saisissez un nom et une description de section.
1. Sélectionnez un type d’entité. **[!UICONTROL Prospects]** est sélectionné par défaut. **[!UICONTROL Contacts]**, **[!UICONTROL Comptes]** et **[!UICONTROL Opportunités]** sont également disponibles.
1. Sélectionnez les champs du CRM à importer.

   Chaque ligne de champ affiche ses **[!UICONTROL Nom d’affichage]**, **[!UICONTROL Nom du champ]** et **[!UICONTROL Type de données]**.

1. Activez **[!UICONTROL Filtrable]** pour chaque champ de prospect, contact ou opportunité que vous souhaitez rendre disponible en tant que filtre sur la liste **[!UICONTROL Prospects]**.
1. Prévisualisez la section et sélectionnez **[!UICONTROL Ajouter]**.

Les champs mappés apparaissent dans les zones correspondantes de Sales Qualifier :

* Les champs du prospect apparaissent dans l’onglet **[!UICONTROL Personne]**.
* Les champs Compte s’affichent dans l’onglet **[!UICONTROL Compte]**.
* Les champs d’opportunité apparaissent dans la section **[!UICONTROL Opportunité de compte]**. Les champs d’opportunité filtrables apparaissent également comme leurs propres colonnes dans **[!UICONTROL Mes contacts d’opportunité]**, avec des libellés tels que **[!UICONTROL Étape (opportunité)]** pour les distinguer des champs de contact.

## Configuration de la synchronisation des activités (mapping sortant)

1. Dans **[!UICONTROL Connexions CRM]**, sélectionnez **[!UICONTROL Gérer]** pour le CRM connecté.
1. Ouvrez **[!UICONTROL Mapping sortant]**.
1. Activez **[!UICONTROL Synchronisation des activités]** pour synchroniser les activités de sensibilisation de Sales Qualifier avec le CRM et Marketo. Les activités E-mail envoyé, ouvert, sur lesquelles l’utilisateur a cliqué et a répondu incluent le nom du workflow sortant.

Lorsque la synchronisation des activités est désactivée, Sales Qualifier continue à utiliser les données CRM entrantes, mais ne synchronise pas les activités de sensibilisation au CRM ou à Marketo.

## Créer un guide pratique pour le centre de connaissances {#knowledge-center}

Le **[!UICONTROL Centre de connaissances]** donne à Account Qualification Agent (AQA) accès à vos documents de vente. Sales Qualifier utilise ces ressources pour générer des recherches, des informations sur les qualifications et des informations qui reflètent les ventes de votre entreprise. Seuls les administrateurs peuvent créer et gérer le playbook.

![ Centre de connaissances ](assets/knowledge-center.png){width="800" zoomable="yes"}

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Administration]**, sélectionnez **[!UICONTROL Paramètres d’administration]** et sélectionnez **[!UICONTROL Centre de connaissances]**
1. u
1. Définissez les paramètres **[!UICONTROL Nom de la société]** et **[!UICONTROL URL de la société]** que Sales Qualifier utilise pour effectuer des recherches dans votre société et rédiger des e-mails.
1. Chargez des pièces de théâtre commerciales, des profils client idéaux, des guides de positionnement et d’autres documents promotionnels au format PDF, PPTX ou DOCX.
1. Sélectionnez **[!UICONTROL Créer un playbook]**.

Chaque document chargé affiche son statut de traitement, tel que **[!UICONTROL Prêt]**, et la date de sa dernière mise à jour.

>[!NOTE]
>
>Le traitement d’un playbook peut prendre jusqu’à 24 heures.

Lorsque le manuel est prêt, les représentants peuvent l’utiliser à deux endroits :

* **Invites de courrier électronique sortant** : dans une invite de point de contact, nommez le document et décrivez le contexte à utiliser. Par exemple, saisissez `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`. Voir [ Générer et réviser des points de contact](outbound-workflows.md#step-3-generate-and-review-touchpoints).
* **Chat IA** : Reportez-vous au Centre de connaissances dans votre question. Par exemple, saisissez `From the Knowledge Center, help me position our security solution for ABC Corp before tomorrow's call`. Voir [Conversation IA](ai-assistant.md).

Dans les deux cas, le contenu généré reflète le message de votre playbook plutôt que la recherche générique.

## Configuration du processus d’opt-out global des e-mails

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Administration]** et sélectionnez **[!UICONTROL Paramètres d’administration]**.
1. Sélectionnez **[!UICONTROL Paramètres de messagerie]** sous **[!UICONTROL Conformité]**.
1. Activez **[!UICONTROL Inclure un lien d’opt-out dans chaque e-mail]** pour ajouter un pied de page de désabonnement aux e-mails sortants.
1. Dans **[!UICONTROL Modèle de message d’opt-out]**, saisissez le texte du pied de page. Incluez le jeton `{opt_out_link}` où le lien de désabonnement doit apparaître.

Les paramètres sont enregistrés automatiquement.

Lorsqu’un prospect sélectionne le lien, Sales Qualifier cesse d’envoyer des e-mails à ce prospect et synchronise le statut de désinscription sur le CRM connecté.

## Référence : exemples de paramètres d’API

Votre équipe CRM peut utiliser ces exemples pour confirmer que l’accès en lecture renvoie les champs de prospect attendus.

### Exemple OData Dynamics

```text
$select=fullname,_ownerid_value,leadid,emailaddress1,jobtitle,statuscode,createdon,modifiedon,statecode
$filter=_ownerid_value eq '<crmUserId>' [AND additional filters]
$expand=Lead_ActivityPointers(...),parentaccountid(...)
$orderby=modifiedon desc
```

### Exemple SOQL Salesforce

```sql
SELECT Id, Salutation, FirstName, LastName, Name, Title, Company, Email,
  LeadSource, Status, OwnerId, LastModifiedDate, LastActivityDate, CreatedDate,
  (SELECT Id, Subject, ActivityDate, Status FROM Tasks ORDER BY ActivityDate DESC LIMIT 1),
  (SELECT Id, Subject, ActivityDateTime FROM Events ORDER BY ActivityDateTime DESC LIMIT 1)
FROM Lead
WHERE OwnerId = '<crmUserId>' AND IsDeleted = false
ORDER BY LastModifiedDate DESC
```

>[!MORELIKETHIS]
>
>* [Commencer](getting-started.md)
>* [Prospects](prospects.md)
