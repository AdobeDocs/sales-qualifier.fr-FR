---
title: Configurer les paramètres de profil
description: Découvrez comment configurer la connexion par e-mail, la signature et la disponibilité du calendrier dans les paramètres du profil Sales Qualifier.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/juP3sddkmc-nSTcTEKGWolbCwNWDgSA0yr6XK1X-w94'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: e7de3a1e28cb8268b58f1ab1ec10394035bdfd74
workflow-type: tm+mt
source-wordcount: 375
ht-degree: 3%

---


# Paramètres de profil

Dans le volet de navigation de gauche, développez **[!UICONTROL Configuration]** et sélectionnez **[!UICONTROL Paramètres de profil]**. Utilisez ces paramètres pour gérer vos informations personnelles, la connexion par e-mail, le calendrier et la disponibilité du chat.

## Paramètres d’e-mail

Dans l’onglet **[!UICONTROL Paramètres de messagerie]**, configurez vos connexions par e-mail.

* **[!UICONTROL Connexions par e-mail]** : sélectionnez **[!UICONTROL Connecter Outlook]** et suivez le processus de connexion à Microsoft. Voir [Connexion à Outlook](integrations.md#connect-outlook) pour connaître l&#39;accès que vous approuvez et le chemin d&#39;approbation de l&#39;administrateur, le cas échéant.
* **[!UICONTROL Signature de l&#39;email]** : ajoutez ou mettez à jour la signature utilisée dans les emails générés. Incluez votre lien [réservation de réunion](outbound-workflows.md#meeting-booking) afin que les prospects puissent planifier du temps avec vous.

### Contexte de rédaction des emails

Utilisez **[!UICONTROL contexte de rédaction des e-mails]** pour définir le ton, la structure et le style des e-mails, afin que ceux-ci soient cohérents.

Écrivez votre contexte en Markdown simple dans la zone **[!UICONTROL Contexte de rédaction d’e-mail]**.
Utilisez-la pour définir :

* Ton et voix
* Structure et longueur
* Personalization et règles de salutations
* Style de la ligne d&#39;objet
* Utilisation des signaux d’engagement
* comment les mesures, les points de BAT et les témoignages de clients sont encadrés ;

Par défaut, les brouillons utilisent un contexte de style maison, de sorte que les brouillons existants ne changent pas tant que vous n’avez pas ajouté votre propre contexte.

## Configuration du calendrier

Définissez votre fuseau horaire et votre disponibilité dans l’onglet **[!UICONTROL Configuration du calendrier]**.

* **[!UICONTROL Connexion au calendrier]**—Sélectionnez **[!UICONTROL Connexion]** et suivez le processus de connexion à Microsoft.
* **[!UICONTROL E-mail de confirmation de réunion]**—Définissez l&#39;objet et le corps de l&#39;e-mail de confirmation qu&#39;un prospect reçoit après avoir réservé une réunion.
* **[!UICONTROL Préférences]** : définissez la durée de réunion par défaut et la marge entre les réunions.

Si vous déconnectez votre calendrier :

* Les liens de réservation actifs ne fonctionnent plus.
* La page de réservation affiche un message d’indisponibilité temporaire.
* Vos paramètres sont conservés lorsque vous vous reconnectez.

## Disponibilité du calendrier

La disponibilité de votre calendrier dans Sales Qualifier repose sur deux entrées :

* Votre calendrier professionnel connecté, tel qu’Outlook ou Gmail
* Les règles de disponibilité et de créneau horaire dans **[!UICONTROL configuration du calendrier]**

Sales Qualifier lit le statut de disponibilité, et non les détails de l’événement, à partir du calendrier connecté. Il associe ce statut à vos règles afin de déterminer les créneaux horaires que les prospects peuvent réserver.

Vous pouvez configurer les éléments suivants :

* Heures de travail par jour de la semaine
* Plusieurs blocs par jour, par exemple, de 9 h à midi et de 13 h à 17 h.
* Votre fuseau horaire
* Durée de la réunion
* Mettre en mémoire tampon avant et après les réunions
* Avis minimal
* Fenêtre de réservation

>[!MORELIKETHIS]
>
>* [Workflows sortants](outbound-workflows.md)
>* [Intégrations](integrations.md)
>* [Tâches](tasks.md)
