---
title: Créer et gérer des workflows sortants
description: Découvrez comment créer, partager, réviser et gérer des workflows sortants générés par l’IA dans Sales Qualifier pour exécuter des cadences de sensibilisation axées sur des objectifs.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/n3FbuiM2zF9QSqaKx1bhBSdbsf-w7vEsEGjCQTBo3g4'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 08dd05e1d13b501d43d457e6217a43aaabdb1d0d
workflow-type: tm+mt
source-wordcount: 1897
ht-degree: 0%

---


# Workflows sortants

Un plan d’engagement est une cadence de sensibilisation axée sur les objectifs. Vous définissez l’objectif et les critères de ciblage. L’IA propose ensuite une cadence multipoint et écrit du contenu d’e-mail personnalisé pour chaque prospect. Avant d’activer le rythme, passez en revue et approuvez chaque e-mail.

Un plan d’engagement relie quatre éléments :

* **Objectif** : résultat que vous attendez de la sensibilisation, tel que la réservation d’un appel de découverte ou l’augmentation de l’enregistrement à un événement.
* **Filtres de ciblage**—Conditions déterminant les prospects éligibles.
* **Cadence des points de contact** : séquence ordonnée d’étapes d’e-mail, d’appel téléphonique et LinkedInMail.
* **Contenu d’e-mail personnalisé** : contenu généré par l’IA en fonction du profil du prospect, du contexte du compte, de l’historique de l’engagement et des actualités récentes.

L’IA utilise l’objectif pour suggérer des filtres de ciblage, concevoir la cadence, créer des brouillons d’invites de point de contact et personnaliser chaque e-mail généré.

## Principaux concepts

| Concept | Description |
| --- | --- |
| **Plan d’engagement** | Activité sortante réutilisable définie par un objectif, des filtres de ciblage, une cadence et des paramètres. |
| **Objectif** | Ce que la sensibilisation devrait accomplir. |
| **Point de contact** | Une étape de la cadence (e-mail, appel téléphonique ou LinkedInMail), planifiée par rapport à l’inscription. |
| **invite de point de contact** | Instructions que l’IA suit lors de la génération de l’objet et du corps d’un e-mail pour un prospect, notamment le ton, la longueur, le focus et le call to action. |
| **Cadence** | La séquence complète des points de contact : combien, dans quel ordre et à quels jours. |
| **Filtre de ciblage** | Condition qui limite le plan d’engagement à un sous-ensemble de prospects. |
| **Brouillon** | Un e-mail généré qui est prêt pour la révision mais pas encore approuvé. |
| **Raisonnement** | L’IA explique comment elle a écrit un e-mail donné, y compris les signaux et les sources de données qu’elle a utilisés. |
| **Inscription** | Approuver les brouillons d’un prospect, ce qui active le rythme et met en file d’attente les e-mails à envoyer pendant la fenêtre d’envoi du plan d’engagement. |

Les sections suivantes expliquent comment créer un plan d’engagement, passer en revue les e-mails générés, approuver les prospects et gérer les workflows sortants.

## Créer un plan d’engagement

L’assistant Plan d’engagement se compose de cinq étapes : **[!UICONTROL Objectif]**, **[!UICONTROL Ciblage]**, **[!UICONTROL Générer des points de contact]**, **[!UICONTROL Paramètres]** et **[!UICONTROL Ajouter des prospects]**. Votre objectif façonne les étapes restantes.

1. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Workflows sortants]**.
1. Dans l’onglet **[!UICONTROL Parcourir]**, sélectionnez **[!UICONTROL + Créer un plan d’engagement]** dans le coin supérieur droit.

### Étape 1 : définir votre objectif

L’objectif définit le résultat prévu et guide le ciblage, la cadence et la génération d’e-mails.

1. Sélectionnez **[!UICONTROL Démarrer à partir de zéro]** pour écrire votre propre objectif, ou sélectionnez **[!UICONTROL Démarrer à partir d’un modèle]** pour utiliser un modèle enregistré.

1. Sélectionnez l’un des **[!UICONTROL Objectifs recommandés]** correspondant à votre entreprise. Chaque recommandation comprend une brève explication de sa pertinence. Sélectionnez une recommandation pour remplir l’objectif, sélectionnez **[!UICONTROL Afficher tout]** pour parcourir l’ensemble complet des recommandations ou saisissez votre propre objectif. Vous pouvez également choisir dans la liste **[!UICONTROL Objectifs populaires]**.
1. Sélectionnez **[!UICONTROL Suivant : Ciblage]**.

Indiquez un résultat spécifique dans l’objectif. Par exemple, saisissez `Book a 15-minute discovery call with marketing leaders evaluating campaign automation` au lieu de `Promote campaign automation`.

### Étape 2 : Configuration des filtres de ciblage

Les filtres de ciblage définissent les prospects éligibles. Lorsque vous ajoutez des prospects ultérieurement, seuls ceux qui correspondent à ces filtres apparaissent dans la liste de sélection.

1. Sélectionnez la flèche vers le bas pour ouvrir la liste **[!UICONTROL Ajouter un filtre]**, puis sélectionnez un filtre.

1. Définissez des valeurs pour le filtre.
1. Ajoutez d’autres filtres si vous devez limiter l’audience.

1. Sélectionnez **[!UICONTROL Suivant : générer des points de contact]**.

### Étape 3 : génération et révision des points de contact

Une fois le ciblage configuré, l’IA analyse l’objectif et les critères de ciblage, définit la cadence et écrit une invite pour chaque point de contact. Le rythme peut inclure des étapes d’e-mail, d’appel téléphonique et LinkedInMail.

Développez un point de contact d’e-mail pour lire son invite. L’invite guide l’IA lorsqu’elle écrit l’e-mail de chaque prospect, y compris le ton, la durée, le focus et le call to action.

#### Régénérer la cadence

Si la cadence ne vous convient pas, sélectionnez **[!UICONTROL Régénérer]** et saisissez une instruction d’affinement. Par exemple :

* `Use three touchpoints across two weeks`
* `Lead with an executive briefing offer in the first email`
* `Add a nurture touch focused on a relevant case study`

L’IA réécrit la cadence complète en fonction de vos instructions. Pour ajuster un point de contact d’e-mail, modifiez son invite au lieu de générer à nouveau la cadence entière.

Définissez un délai du point de contact en jours, heures et minutes. Définissez les jours, heures et minutes à `0` pour envoyer le point de contact sans attendre après l’inscription ou l’achèvement du point de contact précédent. Utilisez un délai plus long pour espacer les points de contact ultérieurs au cours de la cadence.

#### Utiliser le Centre de connaissances dans les invites

Si votre entreprise a créé un playbook [Centre de connaissances](knowledge-center.md), reportez-vous à celui-ci dans l’invite. Nommez le document et décrivez le contexte à utiliser. Par exemple, saisissez `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`.

Lorsque le rythme et les invites sont prêts, sélectionnez **[!UICONTROL Suivant : Paramètres]**.

Affinez les invites de point de contact avant de générer les e-mails de prospect. L’IA utilise ces invites pour chaque prospect sélectionné.

### Étape 4 : configurer les paramètres du plan d’engagement

L’étape **[!UICONTROL Paramètres]** contrôle le fonctionnement du plan d’engagement.

1. Passez en revue le **[!UICONTROL nom du plan d’engagement]** et modifiez-le si nécessaire.
1. Dans **[!UICONTROL Nombre maximal de prospects par plan d’engagement]**, confirmez le nombre maximal de prospects que le plan d’engagement peut gérer simultanément.
1. Définissez la **[!UICONTROL fenêtre d’envoi]** pour les heures pendant lesquelles les e-mails sortants sont autorisés à être envoyés.
1. Sélectionnez les jours de la semaine où les e-mails peuvent être envoyés. Pour éviter les envois de week-end, sélectionnez uniquement les jours de la semaine au lieu d’utiliser un paramètre **[!UICONTROL Ignorer les week-ends]** distinct.
1. Choisissez si vous souhaitez envoyer pendant les heures les plus actives de chaque prospect.
1. Pour arrêter automatiquement les points de contact de suivi une fois qu’un prospect a réservé une réunion, activez **[!UICONTROL Pause de la réservation de réunion]**.
1. Choisissez d’utiliser le fuseau horaire de chaque prospect ou le plan d’engagement **[!UICONTROL fuseau horaire]** pour la planification de l’envoi. Si vous utilisez le fuseau horaire du plan d’engagement, vérifiez qu’il correspond à votre audience.
1. Sous **[!UICONTROL Autorisations]**, conservez **[!UICONTROL Privé]** (valeur par défaut) ou sélectionnez **[!UICONTROL Partagé avec tout le monde]**. Pour plus d’informations, voir [Partager un plan d’engagement](#share-an-engagement-plan).
1. Sélectionnez **[!UICONTROL Enregistrer et ajouter des prospects]**.

Le pied de page d’opt-out est configuré globalement par un administrateur et s’applique aux e-mails sortants indépendamment des paramètres du plan d’engagement. Voir [&#x200B; Configuration du processus d’opt-out global des e-mails](integrations.md#configure-global-email-opt-out).

### Étape 5 : ajouter des prospects et commencer la génération d’e-mails

L’enregistrement ouvre la vue de sélection des prospects avec les filtres de ciblage de l’étape 2 appliqués.

1. Passez en revue la liste.

   Les lignes comprennent généralement le nom, le compte, l’adresse e-mail, la fonction, le statut d’engagement et le statut du prospect.

1. Ajustez les filtres ici si vous devez développer ou réduire la liste.
1. Sélectionnez des prospects à l’aide des cases à cocher.
1. Sélectionnez **[!UICONTROL Suivant : consulter les points de contact]** pour commencer la génération d’e-mails par prospect.

L’IA génère un e-mail personnalisé pour chaque prospect et point de contact d’e-mail sélectionné. Les points de contact Phone et LinkedInMail restent des étapes planifiées. Pour continuer à travailler pendant la génération, sélectionnez **[!UICONTROL Notifier lorsque prêt]**.

Pour chaque prospect, l’IA associe l’invite de point de contact aux données de personne et de compte, à l’historique d’engagement et aux actualités récentes afin de produire une ligne d’objet et un corps.

## Consulter et affiner les e-mails générés

Une fois la génération terminée, la vue détaillée du plan d’engagement vous invite à examiner les brouillons. Sales Qualifier n’envoie pas d’e-mail tant que vous ne l’avez pas approuvé.

1. Dans la vue détaillée du plan d’engagement, sélectionnez **[!UICONTROL Vérifier les brouillons]** dans la bannière.
1. L’étape **[!UICONTROL Vérifier les points de contact]** comporte deux onglets :
   * **[!UICONTROL Prêt pour la révision]** : les e-mails dont la génération est terminée.
   * **[!UICONTROL Génération]** : les e-mails en cours d’écriture.
1. Dans la liste des prospects à gauche, sélectionnez un nom pour charger les points de contact de ce prospect à droite.
1. Utilisez le chevron (**>**) sur un point de contact pour développer et lire l’objet et le corps complets.

### Lire le raisonnement de l’IA

Pour chaque e-mail généré, la section **[!UICONTROL REASONING]** explique comment l’IA a conçu ce message, y compris les signaux, les attributs et les sources qui ont façonné le contenu et le call to action. Passez en revue ces informations et validez la personnalisation avant d’approuver.

### Modifier directement les e-mails

Pour les petits changements de libellé ou de ton :

1. Sur le point de contact développé, sélectionnez l’icône **[!UICONTROL Modifier]** pour ouvrir l’éditeur.
1. Modifiez l’objet ou le corps.
1. Sélectionnez **[!UICONTROL Enregistrer]**.

### Affiner les e-mails avec l’IA

Pour les modifications structurelles ou d’accentuation, utilisez **[!UICONTROL Générer avec l’IA]**. L’IA réécrit l’email tout en conservant son contexte de personnalisation.

1. Dans l’éditeur d’email, sélectionnez **[!UICONTROL Générer avec l’IA]**.

1. Saisissez une instruction claire, par exemple :
   * `Make it shorter and more direct. Keep it under 100 words.`
   * `Focus more on the prospect's role and how the solution helps them specifically.`
   * `Change the call-to-action to suggest a 15-minute introductory call instead.`
1. Passez en revue la révision et modifiez-la si nécessaire.
1. Sélectionnez **[!UICONTROL Enregistrer]**.

>[!TIP]
>
>Utiliser des modifications directes du libellé et du ton. Utilisez **[!UICONTROL Générer avec l’IA]** pour réécrire l’e-mail.

## Approuver et inscrire des prospects

La validation active le rythme d’un prospect. Le système n’envoie pas d’e-mails à un prospect tant que vous ne l’avez pas approuvé et inscrit.

1. Dans la liste de gauche des prospects, sélectionnez les prospects dont vous avez vérifié les e-mails et qui sont prêts à envoyer.
1. Sélectionnez **[!UICONTROL Approuver et inscrire les prospects]** dans le coin inférieur droit.

Les e-mails approuvés sont envoyés en fonction des jours sélectionnés du plan d’engagement, de la fenêtre d’envoi, de l’option des heures d’activité et du paramètre de fuseau horaire. Un point de contact avec un retard nul envoie sans attente ; chaque autre point de contact suit son retard configuré. Les prospects non approuvés sont toujours dans l’état **[!UICONTROL Prêt pour la révision]**.

## Partager un plan d’engagement

Chaque plan d’engagement comporte un paramètre **[!UICONTROL Autorisations]**. Les workflows sortants sont **[!UICONTROL privés]** par défaut. Le propriétaire peut sélectionner **[!UICONTROL Partagé avec tout le monde]** pour rendre un plan d’engagement disponible pour l’équipe.

>[!CAUTION]
>
>Le partage est permanent. Une fois qu’un plan d’engagement est défini sur **[!UICONTROL Partagé avec tout le monde]**, il ne peut pas être redéfini sur **[!UICONTROL Privé]**.

Dans un plan d’engagement partagé, les coéquipiers peuvent inscrire leurs propres prospects. Chaque personne ne peut gérer ou suspendre que les prospects auxquels elle est inscrite, y compris lors de l’utilisation d’actions en masse. Le propriétaire du plan d’engagement peut modifier seul les paramètres au niveau du plan, y compris la planification, le fuseau horaire, la cadence et d’autres paramètres. Ces paramètres sont en lecture seule pour les coéquipiers.

Utilisez ces filtres pour que les workflows sortants partagés et les résultats restent ciblés :

* Dans **[!UICONTROL Prospects engagés]** et **[!UICONTROL Performances]**, utilisez **[!UICONTROL Inscrit par]** pour filtrer les prospects par la personne qui les a inscrits. Le filtre correspond par défaut aux prospects que vous avez inscrits.
* Sur l’onglet **[!UICONTROL Parcourir]**, utilisez le filtre de partage pour sélectionner **[!UICONTROL Partagé par moi]**, **[!UICONTROL Partagé avec moi]**, **[!UICONTROL Privé]** ou **[!UICONTROL Tout]**.

## Gestion des réponses d’absence du bureau

Lorsqu’un prospect répond avec un message d’absence du bureau, le plan d’engagement le gère automatiquement.

* **Reprise automatique** : activé par défaut. Si la réponse d’absence du bureau comprend une date de retour, le plan d’engagement reprend le rythme à cette date. Si aucune date de retour n’est fournie, le plan d’engagement reprend après la mise en mémoire tampon de reprise que votre équipe peut configurer.
* **Options manuelles** : vous pouvez également reprendre, mettre en pause ou ignorer manuellement le prospect. Voir [&#x200B; Gestion des workflows sortants existants &#x200B;](#manage-existing-engagement-plans).

## Gestion des workflows sortants existants

Sur la page **[!UICONTROL Workflows sortants]**, l’onglet **[!UICONTROL Parcourir]** répertorie tous les plans d’engagement disponibles. Chaque carte affiche l’objectif, les points de contact configurés et les mesures de performances. Utilisez cette vue pour surveiller les workflows sortants, réviser les brouillons ou ajouter des prospects.

## Boîte d’envoi d’e-mail

La [boîte d’envoi d’e-mail](email-outbox.md) répertorie les e-mails automatisés envoyés en votre nom et les réponses.

## Réservation de réunion

Lorsque vous connectez votre calendrier, Sales Qualifier génère un lien de réservation personnel que les prospects peuvent utiliser pour planifier des heures avec vous.

* **Liens de réservation**—Configurez la connexion et la disponibilité de votre calendrier dans [Paramètres du profil](profile-settings.md). Ajoutez le lien de réservation à votre signature d’e-mail afin qu’il apparaisse dans les e-mails sortants.
* **Placement de cadence** : Sales Qualifier insère votre lien de réservation aux points pertinents d’une cadence. Vous pouvez modifier son emplacement.
* **Pause de la réservation** : lorsqu’un prospect réserve une réunion, **[!UICONTROL Pause de la réservation de la réunion]** arrête les autres suivis. Voir [Étape 4 : Configurer les paramètres du plan d’engagement](#step-4-configure-engagement-plan-settings).

Suivez les résultats de la réservation sur la page [Performances sortantes](performance.md).

## Bonnes pratiques relatives au plan d’engagement

* **Définissez un objectif spécifique.** Le ciblage, la cadence et les e-mails dérivent tous de l’objectif . Indiquez le résultat que vous souhaitez que le plan d’engagement atteigne.
* **Finalisez les invites de point de contact avant la génération par prospect.** Après la génération en bloc, les modifications sont généralement apportées un prospect à la fois.
* **Utiliser le raisonnement comme contrôle de qualité.** Si le mauvais signal est mis en évidence ou si un signal approprié est manquant, modifiez l’e-mail ou révisez l’invite de point de contact et régénérez la cadence.
* **Faire correspondre l’outil d’édition à la modification.** Utiliser des modifications directes du libellé et du ton. Utilisez **[!UICONTROL Générer avec l’IA]** pour restructurer ou recadrer.
* **Approuver uniquement ce que vous avez révisé.** Développez les points de contact, lisez le contenu et affinez-les si nécessaire avant l’inscription.

>[!MORELIKETHIS]
>
>* [Tâches](tasks.md)
>* [&#x200B; Centre de connaissances &#x200B;](knowledge-center.md)
>* [Performance sortante](performance.md)
