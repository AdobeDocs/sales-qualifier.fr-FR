---
title: Comptes dans Sales Qualifier
description: Découvrez comment passer en revue les renseignements sur les comptes dans Sales Qualifier, y compris les recherches sur l’IA, les actualités récentes, les opportunités et les contacts les plus engagés, afin de donner la priorité à la sensibilisation.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 8573d3891d5c8ec8a05637f160f120f933b0ec61
workflow-type: tm+mt
source-wordcount: 632
ht-degree: 0%

---


# Comptes

La vue de compte combine les recherches générées par l’IA, les actualités récentes, les opportunités ouvertes, la valeur du pipeline et les contacts engagés. Utilisez ces informations pour comprendre et classer par priorité un compte avant de vous adresser à .

## Ouvrir un compte

Ouvrez un compte à partir du profil d’un prospect qui lui est associé.

1. Sélectionnez **[!UICONTROL Prospects]** dans le volet de navigation de gauche, puis ouvrez un prospect. Voir [ Prospects ](prospects.md).
1. Sur la page des détails du prospect, sélectionnez l’onglet **[!UICONTROL Compte]**.

Sales Qualifier identifie le compte à partir de l’enregistrement CRM du prospect. La même vue de compte est disponible pour chaque prospect associé à ce compte. Si Sales Qualifier ne peut pas correspondre à un compte, l’onglet affiche _Aucun compte trouvé_.

>[!NOTE]
>
>Les sections et mesures disponibles dépendent de votre CRM, de la configuration de votre organisation et des données du compte. Si une section décrite ici n’apparaît pas, les données ou la fonctionnalité requises ne sont pas configurées.

La vue de compte comporte deux onglets : **[!UICONTROL Détails]** et **[!UICONTROL Recherche de compte]**.

## Consulter les détails du compte

L’onglet **[!UICONTROL Détails]** vous donne un instantané du compte et de son pipeline.

### Présentation du compte

La carte d’aperçu située en haut de l’onglet identifie le compte et résume sa valeur :

* Nom du compte et région
* **Chiffre d’affaires annuel récurrent (ARR)** : chiffre d’affaires annuel récurrent pour tous les abonnements actifs. Sélectionnez **[!UICONTROL Afficher tout]** pour consulter le montant total autorisé par produit dans la boîte de dialogue **[!UICONTROL Revenus récurrents annuels]**.
* Statistiques du compte, y compris le nombre d’opportunités ouvertes et de contacts et la valeur du pipeline

### Résumé de l’aperçu du compte

Le panneau **[!UICONTROL Présentation du compte]** résume le compte en fonction des données CRM et de la recherche Account Qualification Agent. Si la recherche est en cours, le panneau affiche un état de chargement. Si aucune recherche n’est disponible, le panneau affiche un message.

### Informations sur le compte

Utilisez les boutons situés sous la vue d’ensemble pour basculer entre les vues de compte. Les vues disponibles dépendent de votre CRM et de votre configuration :

| Affichage | Ce qu’il montre |
| --- | --- |
| **[!UICONTROL Opportunités]** | Opportunités ouvertes liées au compte, avec des champs clés pour chacune. Sélectionnez **[!UICONTROL Afficher tout]** pour afficher la liste complète dans un tableau. Les détails de l’opportunité, tels que l’étape, le type et la date de fermeture, peuvent également être utilisés pour filtrer les contacts du compte dans **[!UICONTROL Mes contacts d’opportunité]** lorsqu’un administrateur rend ces champs filtrables. |
| **[!UICONTROL Membres principaux]** | Les contacts les plus engagés du compte, classés par engagement. Chaque contact affiche son intitulé de poste, son adresse e-mail, son score d’engagement et son indicateur d’urgence. |
| **[!UICONTROL Données d’intention]** | Signaux d’intention d’achat pour le compte, tels que les produits et les sujets sur lesquels le compte fait des recherches. |
| **[!UICONTROL Membres de l’équipe de compte]** | Personnes affectées au compte, avec leur adresse e-mail, fonction, territoire et groupe de produits. |
| **[!UICONTROL champs CRM]** | Champs de compte importés de votre CRM, tels que configurés dans le mapping entrant. Pour plus d&#39;informations, consultez la section [ Intégrations ](integrations.md#map-crm-fields-inbound-mapping). |

Dans la vue **[!UICONTROL Membres principaux]**, effectuez l’une des actions suivantes pour un contact :

* **[!UICONTROL Ajouter au workflow sortant]**—Inscrire le contact dans un [workflow sortant](outbound-workflows.md).
* **[!UICONTROL Ajouter à la campagne Marketo]** : déclenchez une campagne [!DNL Marketo] pour le contact.

## Effectuer des recherches sur le compte

L’onglet **[!UICONTROL Recherche de compte]** contient trois zones :

* **[!UICONTROL Catégories de recherche]**—Thèmes de recherche. Sélectionnez une catégorie pour afficher sa recherche dans le volet central.
* **Contenu de la recherche** - Cartes de recherche générées par l&#39;IA regroupées par catégorie. Une carte peut inclure le domaine source et les dates de la première et de la dernière détection du signal.
* **[!UICONTROL Informations récentes]** : informations à jour sur le compte, notamment les dates, les balises et les liens sources.

Si la recherche ou les actualités ne peuvent pas se charger, chaque zone propose une action **[!UICONTROL Recharger]** pour réessayer.

## Utiliser les renseignements sur les comptes dans la sensibilisation

L’intelligence de compte est la plus précieuse lorsqu’elle façonne ce que vous envoyez :

* Référencez un article récent ou un signal de recherche pour rendre votre ouverture pertinente au lieu d&#39;utiliser un argumentaire générique.
* Vérifiez les opportunités ouvertes et la valeur du pipeline pour décider si vous souhaitez donner la priorité au compte.
* Utilisez **[!UICONTROL Membres principaux]** pour identifier les personnes à contacter, puis inscrivez-les à un workflow sortant.
* Demandez à [AI Chat](ai-assistant.md) de développer le positionnement du compte avant un appel.

>[!MORELIKETHIS]
>
>* [Prospects](prospects.md)
>* [Workflows sortants](outbound-workflows.md)
>* [Conversation IA](ai-assistant.md)
