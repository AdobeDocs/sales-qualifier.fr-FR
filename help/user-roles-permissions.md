---
title: Rôles utilisateur et autorisations
description: Découvrez comment les groupes d’utilisateurs Sales Qualifier contrôlent l’accès aux applications et à l’administration.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/9X9DYGMvLGcPG--G6rHcDEk91hdT9-XYc9wbiL2Qoww'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4bid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 8573d3891d5c8ec8a05637f160f120f933b0ec61
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 4%

---


# Rôles utilisateur et autorisations

Sales Qualifier utilise deux groupes d’utilisateurs requis pour séparer les tâches de vente de la configuration à l’échelle de l’entreprise.

## Groupes d’utilisateurs requis

| Groupe | À qui appartient | Ce qu&#39;il accorde |
| --- | --- | --- |
| `Sales Qualifier` | Chaque utilisateur, y compris les administrateurs | Accès à l’application : prospects, comptes, workflows sortants, tâches, performances et paramètres de profil. |
| `Sales Qualifier Admins` | Administrateurs uniquement, en plus du groupe `Sales Qualifier` | Accès à **[!UICONTROL Paramètres d’administration]**, qui régit les connexions CRM, le Centre de connaissances et les paramètres de conformité pour l’ensemble de l’organisation. |

Les utilisateurs standard n’ont besoin que du groupe `Sales Qualifier` . Les administrateurs doivent être membres des deux groupes. Voir [Commencer](getting-started.md) pour créer ces groupes.

Les organisations peuvent également créer un groupe de `Sales Qualifier BDR managers` facultatif. Les membres peuvent accéder aux rapports de performances des e-mails.

## Accès administrateur

**[!UICONTROL Paramètres d’administration]** s’affiche sous **[!UICONTROL Administration]** uniquement pour les utilisateurs qui appartiennent aux deux groupes requis. Les modifications apportées à ces paramètres s’appliquent à l’ensemble de l’organisation.

## Ce que les administrateurs contrôlent

| Paramètre | Où le configurer | Effet |
| --- | --- | --- |
| Connexion CRM et mappage des champs | [Intégrations](integrations.md#map-crm-fields-inbound-mapping) | Détermine quels champs CRM apparaissent pour un prospect ou un compte et quels champs sont disponibles en tant que filtres. |
| Désinscription globale des e-mails | [Intégrations](integrations.md#configure-global-email-opt-out) | Ajoute un pied de page de désabonnement à chaque e-mail sortant. |
| Centre de connaissances et guide pratique | [ Centre de connaissances ](knowledge-center.md) | Rend le playbook d’entreprise disponible dans les invites sortantes et le [chat IA](ai-assistant.md). |
| Synchronisation de l’activité | [Intégrations](integrations.md#configure-activity-sync-outbound-mapping) | Détermine si les activités de sensibilisation de Sales Qualifier apparaissent dans le CRM. |

Les utilisateurs standard peuvent utiliser ces paramètres, mais ne peuvent pas les modifier. Si un filtre attendu, une référence de playbook ou un champ CRM est manquant, contactez un administrateur.

>[!MORELIKETHIS]
>
>* [Commencer](getting-started.md)
>* [Intégrations](integrations.md)
>* [ Centre de connaissances ](knowledge-center.md)
