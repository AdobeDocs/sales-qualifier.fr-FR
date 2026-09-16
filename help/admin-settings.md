---
title: Paramètres d’administration
description: Découvrez comment gérer les champs CRM, la synchronisation des activités, le processus d’opt-out des e-mails et d’autres paramètres d’administration du qualificateur Marketo d’Adobe.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/vbtO6I67ZEaZz3oio9InNErvq5D0wjbRxyDZpTq8Lzo'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration

internal-label: Administration
source-git-commit: d967b633fcb63c64169d3e3fbf305fd2ff82236d
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%
---

# Paramètres d’administration

Utilisez **[!UICONTROL Paramètres d’administration]** pour configurer les intégrations CRM, gérer le Centre de connaissances et configurer le processus de désinscription aux e-mails.

Adobe Marketo Qualifier se connecte à Salesforce ou Microsoft Dynamics 365. La connexion donne au Account Qualification Agent (AQA) une vue cohérente des prospects, comptes, contacts, activités et propriétaires. Marketo Qualifier peut également écrire des activités de sensibilisation et un statut d’opt-out dans le CRM et synchroniser les activités de sensibilisation avec Marketo.

Pour configurer les connexions CRM, le mappage des champs et la synchronisation des activités, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Paramètres d’administration]** > **[!UICONTROL Connexions CRM]**. Les utilisateurs standard peuvent utiliser les données et les filtres CRM configurés, mais ne peuvent pas modifier ces paramètres. Pour connecter un CRM pour la première fois, voir [Prise en main](getting-started.md#connect-your-crm).

>[!IMPORTANT]
>
>Pour accéder à **[!UICONTROL Paramètres d’administration]**, vous devez être membre des groupes d’utilisateurs `Marketo Qualifier` et `Marketo Qualifier Admins`.

## CRM MCP et le plug-in intégré

Marketo Qualifier fonctionne avec votre CRM des manières suivantes :

* **Requêtes CRM MCP** : les requêtes Account Qualification Agent interrogent les données CRM actives afin que les réponses et les informations reflètent l’état actuel de vos enregistrements.
* **Plug-in intégré** : le plug-in CRM affiche des informations [!DNL Marketo Sales Insights] (MSI) et des données agentiques dans votre CRM. Utilisez le plug-in pour ajouter un prospect au qualificateur Marketo.
* **Synchronisation des activités** : lorsqu’un administrateur active **[!UICONTROL Synchronisation des activités]**, les activités d’extension se synchronisent avec le CRM et Marketo.

## Étendue de l’accès CRM

Le qualificateur Marketo lit les utilisateurs, les contacts, les mappages des propriétaires, les prospects, les comptes, les opportunités et les activités à partir du CRM. Il écrit uniquement les activités de sensibilisation consignées et le statut d’opt-out dans le CRM, et synchronise les activités de sensibilisation avec Marketo. Votre administrateur CRM prépare l’accès à l’API dans Salesforce ou Dynamics. Un administrateur Marketo Qualifier connecte ensuite le CRM, mappe les champs entrants et choisit de synchroniser ou non les activités.

>[!NOTE]
>
>Les étapes d’identification de la section [Prise en main](getting-started.md#connect-your-crm) décrivent l’accès en lecture aux objets CRM. Si vous activez la synchronisation des activités ou l’écriture différée d’opt-out, contactez votre administrateur CRM pour obtenir l’accès en écriture correspondant à celui requis par votre configuration CRM.

## Mappage des champs CRM (mapping entrant)

Une fois le CRM connecté, sélectionnez **[!UICONTROL Gérer]** pour la connexion et ouvrez **[!UICONTROL Mapping entrant]**. Le mappage entrant contrôle les champs CRM que le qualificateur Marketo extrait dans l’application.

1. Sélectionnez **[!UICONTROL Ajouter une section]**.
1. Saisissez un nom et une description de section.
1. Sélectionnez un type d’entité. **[!UICONTROL Prospects]** est sélectionné par défaut. **[!UICONTROL Contacts]**, **[!UICONTROL Comptes]** et **[!UICONTROL Opportunités]** sont également disponibles.
1. Sélectionnez les champs du CRM à importer.

   Chaque ligne de champ affiche ses **[!UICONTROL Nom d’affichage]**, **[!UICONTROL Nom du champ]** et **[!UICONTROL Type de données]**.

1. Activez **[!UICONTROL Filtrable]** pour chaque champ de prospect, contact ou opportunité que vous souhaitez rendre disponible en tant que filtre sur la liste **[!UICONTROL Prospects]**.
1. Prévisualisez la section et sélectionnez **[!UICONTROL Ajouter]**.

Les champs mappés apparaissent dans les zones correspondantes du qualificateur Marketo :

* Les champs du prospect apparaissent dans l’onglet **[!UICONTROL Personne]**.
* Les champs Compte s’affichent dans l’onglet **[!UICONTROL Compte]**.
* Les champs d’opportunité apparaissent dans la section **[!UICONTROL Opportunité de compte]**. Les champs d’opportunité filtrables apparaissent également comme leurs propres colonnes dans **[!UICONTROL Mes contacts d’opportunité]**, avec des libellés tels que **[!UICONTROL Étape (opportunité)]** pour les distinguer des champs de contact.

## Configuration de la synchronisation des activités (mapping sortant)

1. Dans **[!UICONTROL Connexions CRM]**, sélectionnez **[!UICONTROL Gérer]** pour le CRM connecté.
1. Ouvrez **[!UICONTROL Mapping sortant]**.
1. Activez **[!UICONTROL Synchronisation des activités]** pour synchroniser les activités de sensibilisation du qualificateur Marketo avec le CRM et Marketo.

Lorsque la synchronisation des activités est désactivée, le qualificateur de Marketo continue à utiliser les données CRM entrantes, mais ne synchronise pas les activités de sensibilisation vers votre CRM ou votre Marketo.

## Configuration des règles de synchronisation CRM

Le qualificateur Marketo peut écrire automatiquement des mises à jour de statut de lead dans Salesforce et Microsoft Dynamics lorsqu’un prospect se déplace dans un workflow sortant, de sorte que les représentants ne mettent plus à jour le CRM manuellement.

### À quoi servent les règles de synchronisation CRM

Une mise à jour peut cibler l’enregistrement **[!UICONTROL Lead]**, **[!UICONTROL Contact]**, **[!UICONTROL Compte]** ou **[!UICONTROL Opportunité]**, et pas seulement le lead.

Les mises à jour se déclenchent à ces moments de workflow sortant :

* Ajouté à un workflow, répondu ou réunion réservée
* Supprimé par un représentant ou workflow terminé sans réponse
* Opt-out ou e-mail bounce

Les valeurs de champ peuvent être personnalisées avec des jetons dynamiques afin que la mise à jour du CRM reflète le parcours réel du prospect plutôt qu’une valeur statique. Des jetons sont disponibles pour obtenir des détails tels que le nom du représentant, le nom du workflow sortant, ainsi que la date et l’heure de la réunion.

Seules les valeurs compatibles avec le CRM sont écrites, un champ en échec ne bloque pas les autres, et les problèmes temporaires réessayent automatiquement. Chaque mise à jour est suivie afin que vous puissiez voir ce qui a été synchronisé et ce qui requiert une attention particulière.

### Configurer des règles de synchronisation CRM

Pour configurer des règles de synchronisation CRM :

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Administration]** et sélectionnez **[!UICONTROL Paramètres d’administration]** > **[!UICONTROL Connexions CRM]**.
1. Sélectionnez **[!UICONTROL Gérer]** pour le CRM connecté, puis sélectionnez **[!UICONTROL Règles de synchronisation]**.
1. Sélectionnez l’entité et les champs CRM cibles, mappez-les aux moments du workflow ci-dessus, puis activez le bouton (bascule).

Une fois les règles de synchronisation CRM configurées, les équipes commerciales bénéficient d’un statut précis, personnalisé et à jour des prospects, contacts, comptes et opportunités à chaque étape, avec moins de décalage des données et de travail manuel.

## Créer un guide pratique pour le centre de connaissances {#knowledge-center}

Le **[!UICONTROL Centre de connaissances]** donne à Account Qualification Agent (AQA) accès à vos documents de vente. Marketo Qualifier utilise ces ressources pour générer des recherches, des informations sur les qualifications et des informations qui reflètent les ventes de votre entreprise. Seuls les administrateurs peuvent créer et gérer le playbook.

![&#x200B; Centre de connaissances &#x200B;](assets/knowledge-center.png){width="800" zoomable="yes"}

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Administration]**, sélectionnez **[!UICONTROL Paramètres d’administration]** et sélectionnez **[!UICONTROL Centre de connaissances]**
1. u
1. Définissez les **[!UICONTROL Nom de la société]** et **[!UICONTROL URL de la société]** que le qualificateur Marketo utilise pour rechercher votre société et rédiger des e-mails.
1. Chargez des pièces de théâtre commerciales, des profils client idéaux, des guides de positionnement et d’autres documents promotionnels au format PDF, PPTX ou DOCX.
1. Sélectionnez **[!UICONTROL Créer un playbook]**.

Chaque document chargé affiche son statut de traitement, tel que **[!UICONTROL Prêt]**, et la date de sa dernière mise à jour.

>[!NOTE]
>
>Le traitement d’un playbook peut prendre jusqu’à 24 heures.

Lorsque le manuel est prêt, les représentants peuvent l’utiliser à deux endroits :

* **Invites de courrier électronique sortant** : dans une invite de point de contact, nommez le document et décrivez le contexte à utiliser. Par exemple, saisissez `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`. Voir [&#x200B; Générer et réviser des points de contact](outbound-workflows.md#step-3-generate-and-review-touchpoints).
* **Chat IA** : Reportez-vous au Centre de connaissances dans votre question. Par exemple, saisissez `From the Knowledge Center, help me position our security solution for ABC Corp before tomorrow's call`. Voir [Conversation IA](ai-assistant.md).

Dans les deux cas, le contenu généré reflète le message de votre playbook plutôt que la recherche générique.

## Configuration du processus d’opt-out global des e-mails

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Administration]** et sélectionnez **[!UICONTROL Paramètres d’administration]**.
1. Sélectionnez **[!UICONTROL Paramètres de messagerie]** sous **[!UICONTROL Conformité]**.
1. Activez **[!UICONTROL Inclure un lien d’opt-out dans chaque e-mail]** pour ajouter un pied de page de désabonnement aux e-mails sortants.
1. Dans **[!UICONTROL Modèle de message d’opt-out]**, saisissez le texte du pied de page. Incluez le jeton `{opt_out_link}` où le lien de désabonnement doit apparaître.

Les paramètres sont enregistrés automatiquement.

Lorsqu’un prospect sélectionne le lien, le qualificateur Marketo cesse d’envoyer des e-mails à ce prospect et synchronise le statut d’opt-out sur le CRM connecté.

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
