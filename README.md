# FUT AutoBuyer

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![Total Downloads](https://img.shields.io/github/downloads/DevFRpyjs/FUT-Auto-Buyer/total.svg)]()

<p align="center"> 
  <h3 align="center">FUT AutoBuyer</h3>

  <p align="center">
    Autobuyer pour FIFA Ultimate Team Webapp!
    <br />  
    <br /> 
    <a href="https://github.com/DevFRpyjs/FUT-Auto-Buyer/issues">Signaler un bug</a>
    ·
    <a href="https://github.com/DevFRpyjs/FUT-Auto-Buyer/issues">Demander une fonctionnalité</a>
  <hr>
  <p align="center">
  <a center" href="https://discord.gg/MKbzeRMQ9Y">
    <img  src="https://img.shields.io/discord/895353301011419147?style=for-the-badge&color=gold&label=Discord&logo=discord&logoColor=white">
  </a>
                                                                                                                         </p>
  <hr>
  # À lire absolument :no_entry_sign:
  
  Cet outil est développé à des fins d'apprentissage pour démontrer comment quelqu'un peut développer un script pour modifier une application Web en automatisant des taches.
  
   Il se peut qu'EA vous interdise (à titre provisoire) d'utiliser le marché des transferts de l'application Web si vous utilisez cet outil. Une interdiction continue peut également conduire à une interdiction permanente. De plus, l'utilisation de cet outil comme celui-ci pour obtenir un avantage sur les autres joueurs ce qui n'est pas conforme à l'éthique..  
   
   Utilisez cet outil à vos propres risques, les développeurs qui contribuent à ce dépôt ne seront pas tenus responsables si votre compte est banni.
  </p>
</p>

<!-- TABLE OF CONTENTS -->

## Table des matières

- [Installation](#installation)
- [Configuration du solveur de Captcha](#Captcha)
- [Utilisation](#Usage)
- [Conditions préalables](#prerequisites)
- [Guide d'installation pour Telegram](#Telegram-Installation-Guide)
- [Feuille de route](#Roadmap)
- [Guide du développeur](#Developer-Guide)
- [Contribution](#contributing)
- [Contact](#contact)

<!-- installation -->

## Installation

- Ajouter l'extension Tamper Monkey à votre navigateur - [Link](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en-GB).
- Cliquez sur fut-auto-buyer.user.js à partir de - [Latest Release](https://github.com/DevFRpyjs/FUT-Auto-Buyer/releases/).
- Cliquez ensuite sur Installer/Mettre à jour.
- Installation et démonstration - [Video Guide](https://www.youtube.com/watch?v=WATch4hxhtk).

Maintenant, dans Ultimate Team Web App, un nouveau menu sera ajouté : AutoBuyer.

## Captcha

### Configuration du solveur de Captcha

- Follow this [video](https://www.youtube.com/watch?v=9p_IMe52LBo) if you are not sure how to set it up.

<!-- Usage -->

## Usage

### Paramètres de l'AutoBuyer

### Prix de vente (Sell Price)

- Si cette option est spécifiée, l'acheteur listera automatiquement l'article acheté au prix spécifié.
- L'outil listera toutes les cartes en transfert, assurez-vous de déplacer vos cartes vers le club avant de lancer l'outil pour éviter de perdre la carte.
- Donnez un prix de vente de -1 pour envoyer à la liste des transferts sans vendre..

### Prix d'achat (Buy Price)

- Si spécifié, l'acheteur achètera automatiquement la carte correspondant aux critères de recherche pour un prix inférieur ou égal au prix spécifié.

### Prix de l'enchère (Bid Price)

- Si cela est spécifié, l'acheteur enchérira automatiquement sur la carte correspondant aux critères de recherche pour un prix inférieur ou égal au prix spécifié..

### Nombre de cartes à acheter (No. of cards to buy)

- Nombre de cartes que l'acheteur doit acheter avant de s'arrêter..
- Valeur par défaut (`10`).

### Prix exact de l'enchère (Bid Exact Price)

- Par défaut, l'outil fera une offre au prix le plus bas possible et augmentera progressivement l'offre, si ce bouton est activé, le robot fera une offre directe au prix spécifié.

### Trouver le prix de vente (Find Sale Price)

- Si activé, il utilisera l'api FUTBIN pour obtenir le prix du joueur.

### Prix de vente Pourcentage (Sell Price Percent)

- Lorsque la recherche du prix de vente est activée, ce champ permet de spécifier le prix de vente à partir du pourcentage du prix FUTBIN..
- Valeur par défaut (`100`).

### Articles d'enchères expirant le (Bid items expiring in)

- Si cette option est spécifiée, l'outil n'enchérira que sur les articles arrivant à échéance dans la plage de temps indiquée.
- Valeur par défaut (`1H`) (S pour Secondes, M pour Minutes, H pour Heures).

### Relister les articles invendus (Relist Unsold Items)

- Si cette option est activée, le robot vérifiera périodiquement et réinscrira l'article expiré au prix spécifié précédemment.

### \* Note : Cela réinscrit tous les articles expirés, et pas seulement l'article que le bot liste. Vérifiez donc la liste des transferts avant d'activer cette fonction pour éviter de perdre des cartes.

### Temps d'attente (Wait Time)

- Le bot attendra le temps spécifié avant de faire la prochaine demande de recherche.
- Valeur par défaut (`7 - 15`).

### Effacer le nombre de ventes (Clear sold count)

- Le bot efface tous les articles vendus de la liste de transfert lorsque le nombre d'articles dépasse la valeur spécifiée.
- Valeur par défaut (`10`).

### Seuil d'évaluation (Rating Threshold)

- La carte ne sera listée que si le classement de la carte est inférieur à cette valeur.
- Valeur par défaut (`100`).

### Achats maximum par recherche (Max purchases per search request)

- Indique le nombre de cartes que le bot doit acheter ou enchérir à partir des résultats de chaque requête.
- Valeur par défaut (`3`).

### Arrêt après (Stop After)

- Si cette option est spécifiée, le bot s'arrêtera automatiquement après avoir fonctionné pendant l'intervalle spécifié.
- Valeur par défaut (`1H`) (S for Secondes, M for Minutes, H for Heures).

### Pause (Pause For)

- Le paramètre dépend du montant du cycle.
- Le bot se met en pause pendant l'intervalle spécifié, si le nombre de demandes de recherche dans le cycle donné correspond au nombre de cycles spécifié.
- Valeur par défaut (`0-0S`) (S for Secondes, M for Minutes, H for Heures).

### Cycle de pause (Pause Cycle)

- Indique le nombre de demandes de recherche à effectuer avant de mettre l'outil en pause.
- Valeur par défaut (`10`).

### Note minimale (Min Rating)

- Si cette option est spécifiée, l'outil n'enchérira que sur les articles dont le classement est supérieur ou égal à cette valeur.
- Valeur par défaut (`10`).

### Note maximale (Max Rating)

- Si cette option est spécifié, il n'enchérira que sur les articles dont le classement est inférieur ou égal à cette valeur.
- Valeur par défaut (`100`).

### Délai à ajouter (Delay To Add)

- Si l'ajout d'un délai après l'achat est activé, ce champ ajoute une durée d'attente.
- Valeur par défaut (`1S`) (S for Secondes, M for Minutes, H for Heures).

### Ajouter un délai après l'achat (Add Delay After Buy)

- Si cette option est activée, l'outil attendra le temps spécifié après avoir essayé d'acheter/enchérir sur des cartes.

### Valeur maximale de l'achat minimale aléatoire (Max value of random min bid)

- Si l'utilisation de l'achat minimale aléatoire est activée, ce champ spécifie la valeur maximale jusqu'à laquelle l'achat minimale peut être générée.
- Valeur par défaut (`300`).

### Valeur maximale de l'enchère aléatoire min (Max value of random min buy)

- Si l'utilisation de l'achat minimum aléatoire est activée, ce champ spécifie la valeur maximale jusqu'à laquelle l'achat minimum peut être généré.
- Valeur par défaut (`300`).

### Utiliser l'enchère minimale aléatoire (Use Random Min Bid)

- Si l'outil est activé, il rendra aléatoire l'enchère minimale pour chaque recherche afin d'éviter les résultats en cache.

### Utiliser l'achat minimum aléatoire (Use Random Min Buy)

- Si l'outil est activé, il rendra aléatoire l'achat minimum pour chaque recherche afin d'éviter les résultats en cache.

### Passez GK (Skip GK)

- Si cette option est activée, l'outil évitera d'enchérir/acheter des cartes GOAL.

### Fermer sur déclencheur Captcha (Close On Captcha Trigger)

- Si l'option est activée, l'outil fermera l'application web lorsque Captcha sera déclenché.

### Délai après l'achat (Delay After Buy)

- Si l'outil est activé, il ajoutera un délai de 1 seconde après chaque demande d'achat.

### Codes d'erreur pour arrêter le bot (Error Codes to stop bot)

- Liste des codes d'erreur pour lesquels le robot doit s'arrêter, la valeur doit être au format csv.
- Ex - 421,461,512

### Notification sonore (Sound Notification)

- Si l'outil est activé, il émettra une notification sonore pour les actions telles que le déclenchement de la carte d'achat ou du captcha etc...

## Prerequisites

- Pour utiliser cet outil, l'utilisateur doit avoir accès au marché des transferts.
- Il faut donc jouer le nombre de matchs requis pour avoir accès au marché des transferts avant d'essayer cet outil.

<!-- Telegram -->

## Telegram-Installation-Guide

- Installer Telegram
- Ajouter @BotFather comme contact dans le télégramme
- Envoyer BotFather /newbot
- Saisissez vos données personnelles, comme votre nom, etc.
- Suivez les instructions, et enfin, copiez le jeton(TOKEN) HTTP API.
- Ajoutez votre bot comme contact
- Envoyez /start à votre bot
- Visitez cette URL : https://api.telegram.org/botXXX:YYYYY/getUpdates (remplacez le XXX : YYYYY par votre jeton(TOKEN) d'API HTTP BOT que vous venez de recevoir du BotFather de Telegram)
- Vous y trouverez votre identifiant de chat (ce processus peut prendre quelques minutes). --> ex: "chat":{"id":133333338,"first_name":"John","last_name":"Player"
- Vous pouvez maintenant ajouter votre jeton (TOKEN) de bot et votre identifiant de chat dans les paramètres de notification de l'interface graphique du robot (vers le bas).

<!-- ROADMAP -->

## Roadmap

Voir les [questions ouvertes] (https://github.com/DevFRpyjs/FUT-Auto-Buyer/issues) pour une liste des fonctionnalités proposées (et des problèmes connus).

## 💬 Community

Si vous cherchez de l'aide ou une nouvelle demande de fonctionnalité, rejoignez notre groupe discord.

<img  src="https://img.shields.io/discord/895353301011419147?style=for-the-badge&color=gold&label=Discord&logo=discord&logoColor=white">

<a href="https://discord.gg/MKbzeRMQ9Y">Rejoignez</a>

<!-- DevGuide -->

## Developer-Guide

<a href="https://discord.gg/MKbzeRMQ9Y">Rejoignez ce canal discord</a>

<!-- CONTACT -->

## Contact

Project Link: [https://github.com/DevFRpyjs/FUT-Auto-Buyer](https://github.com/DevFRpyjs/FUT-Auto-Buyer)

<!-- MARKDOWN LINKS & IMAGES -->

[contributors-shield]: https://img.shields.io/github/contributors/DevFRpyjs/FUT-Auto-Buyer.svg?style=flat-square
[contributors-url]: https://github.com/DevFRpyjs/FUT-Auto-Buyer/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/DevFRpyjs/FUT-Auto-Buyer.svg?style=flat-square
[forks-url]: https://github.com/DevFRpyjs/FUT-Auto-Buyer/network/members
[stars-shield]: https://img.shields.io/github/stars/DevFRpyjs/FUT-Auto-Buyer.svg?style=flat-square
[stars-url]: https://github.com/DevFRpyjs/FUT-Auto-Buyer/stargazers
[issues-shield]: https://img.shields.io/github/issues/DevFRpyjs/FUT-Auto-Buyer.svg?style=flat-square
[issues-url]: https://github.com/DevFRpyjs/FUT-Auto-Buyer/issues
