---
layout: post
title: "Stop starting and start finishing"
date: 2014-02-17 14:00
comments: true
categories: [agile]
---
Trente minutes de présentation sur la méthode _Lean Kanban_&nbsp;: _challenge accepted!_
<!--more-->

<iframe src="//slid.es/zenigata/kanban/embed" width="576" height="420" scrolling="no" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

Maintenant je vais vous faire un tour d’horizon de cette fameuse méthode. Par contre, soyez indulgents,
je ne l’ai pas directement expérimentée moi-même, sauf sous son aspect _Scrumban_ –&nbsp;un mix entre _Scrum_ et _Kanban_ qui a le vent en poupe.

D’où vient le terme&nbsp;? À l’origine _kanban_ est un mot japonais qui désignait les fiches cartonnées
que l’on fixait sur les bacs de pièces dans une ligne d’assemblage. Comme celle-ci.
Et très vite toute un ensemble de pratiques ont vu le jour au sein du _Lean_ chez Toyota, des pratiques basées sur le management visuel.

Celles-ci sont aujourd’hui adaptées à l’environnement IT, et sa formalisation par David Anderson est toute récente (2010).
À ce propos je vous recommande la lecture de ce livre de référence en français écrit par Laurent Morisseau.

Mais concrètement, le management visuel ça donne quoi&nbsp;? Eh bien ça donne ça, ou ça. Ça ne vous rappelle rien&nbsp;?
Et oui, les tableaux de tâches _Scrum_ sont des tableaux _kanban_ simplifiés et adaptés.

En gros, _Kanban_ propose une méthode d'amélioration continue par des processus que j’évoquerai plus loin.
Celle-ci cherche à fluidifier le travail en le rendant visuel, en le contraignant par des limites et en cherchant la bonne séquence d'activités.
Elle est non prescriptive, peut être appliquée à n’importe quelle méthode déjà en place, et se construit principalement de manière empirique.
Il n’y a pas de rôle défini comme dans _Scrum_, mais _Kanban_ partage les valeurs agiles.

Je parlais de management visuel pour observer le flux d’activités dans son ensemble. En voici un exemple sur une équipe de réalisation.
Toutes les tâches sont visibles et leur cycle de vie traverse des états représentés ici par des colonnes.
Sur les tableaux _kanban_ on parle plutôt de _minimal marketable feature_ au lieu de _User Story_.
Ces _MMF_ représentent le plus petit incrément de valeur livrable en production.
On utilise des cartes _kanban_ pour les afficher et les manipuler.
Ces cartes présentent diverses informations comme la date d’entrée ou une description succinte.

En voici un autre exemple. On peut notamment jouer avec les couleurs et les lignes pour que l’information soit la plus claire et efficace possible.
Et il y a des chiffres au niveau des noms de colonne.

Ces chiffres sont là pour limiter le _WIP_. _WIP_ signifie _Work In Progress_ ou _Work In Process_, qui a été traduit par Travaux À Faire.
Des études montrent que le multitâche est contre-productif. Le _context switching_ fait perdre beaucoup de temps.
C’est pour ça qu’un des principes de base de _Kanban_ est de limiter le travail en cours en posant des limites sur certaines colonnes ou groupes de colonnes.
On ne peut commencer une nouvelle tâche si le nombre maximum de tâches en cours est atteint. Il faut d’abord libérer de la place en terminant des éléments.
_Stop starting and start finishing_. Ces limites sont appelées limites hautes.
Il existe aussi des limites basses qu’on peut utiliser pour déclencher certains événements.
Par exemple si j’ai moins de deux tâches prêtes on peut déclencher une phase d’alimentation de la colonne Prête.

Tout ceci tend à fluidifier le flux d’activités et à éviter les files d’attente et les stocks.
En effet, la principale préoccupation de _Kanban_ est d’optimiser le flux de valeur et de réduire le _time to market_.
Le système _Kanban_ peut embrasser tous les cycles de vie d’une _MMF_, depuis sa conception jusqu’à sa livraison en production.
Mais qu’est-ce qui se passe quand ça coince&nbsp;?

Des goulets d’étranglement peuvent se former comme des files d’attente, donc du stock.
Ces problèmes apparaîtront clairement dans le système, et il faudra les purger,
par exemple en ajustant les limites ou en modifiant les règles comme ne jamais commencer un travail s’il y a un risque probable de blocage.

Pour cela _Kanban_ fait émerger un système en flux tiré au lieu du classique flux poussé.
On parle bien du mouvement des élements dans le système _kanban_. Prenons un exemple.
En flux poussé, le responsable fonctionnel peut écrire toutes les specs dès qu’il a le temps. Comme lors du cycle en V.
En flux tiré, il le fera quand le développeur en aura besoin, par exemple quelques jours avant.
On peut dire que l’activité en amont est calée sur l’activité en aval. J’ai inséré un exemple que vous pourrez lire à tête reposée.

Le jeu est d’être transparent et d’afficher tous les indicateurs, limites ou règles,
sur le tableau _kanban_ pour que tout le monde se les approprient et les fassent évoluer.
Par exemple, que fait-on quand un élément est bloqué depuis plusieurs jours&nbsp;? ou quand il avance trop lentement&nbsp;?
Quels sont les critères de changement de colonne&nbsp;? Quel élément sélectionne-t-on au sein d’une file d’attente&nbsp;?

Le temps pris pour réaliser une _MMF_ s’appelle le temps de cycle.
On parle de temps de traversée concernant le système complet, de la demande client à la livraison.
En notant les temps de cycle on peut dessiner des cartes de contrôle et repérer a posteriori les éléments les plus problématiques.
On pourra aussi calculer le débit moyen du système pour pouvoir planifier à moyen et long terme.
On pourra également mesurer le niveau de performance à la date d’échéance, c’est-à-dire entre le temps initialement prévu et le temps effectif.
Avec ces indicateurs on peut établir des diagrammes de flux cumulé qui permettent de contrôler l’état du système.
Certains mettent même en place des _obeyas_, des tableaux de bords riches qui, des fois, remplissent carrément toute une salle.

La méthode _Kanban_ est empirique. On ajuste en permanence les contraintes et les règles. L’amélioration continue est au cœur du système.
En ce sens _Kanban_ s’inscrit totalement dans la philosophie _Kaizen_ et suis le modèle _PDSA_ : _Plan_, _Do_, _Study_ et _Act_
pour obtenir régulièrement du _feedback_ et s’améliorer le plus rapidement possible.
Vous en verrez un exemple dans l’atelier qui suit cette présentation.

Pour aller plus loin, l’expérience acquise dans l’univers industriel pour les flux d’activités nous permet d’utiliser des méthodes scientifiques
pour améliorer notre système. Je ne vais pas les expliciter ici car ça devient un peu technique. 

Voici un rappel des itérations _Scrum_ qui regroupent en un même rythme la priorisation des tâches, la démo client, la rétrospective et la livraison.
En _Kanban_ ces cadences sont découplées et s’adaptent au projet. Il n’y a certes pas d’itération mais un flux en continu qui applique le modèle _PDSA_.
Parmi les rituels récurrents on peut aussi citer l’injection des éléments, le triage des files d’attente ou la livraison des _MMF_.
Dans les systèmes les plus optimisés on peut viser le juste-à-temps afin d’obtenir un flux tendu total. Pas de stock.

Pour mettre en œuvre tout ce qu’on a vu, _Kanban_ propose quatre principes de base.
_Start with what you do now_&nbsp;: ce qui veut dire qu’on peut mettre en place _Kanban_ conjointement avec n’importe quelle méthode de gestion de projet déjà en place.
_Agree to pursue incremental, evolutionary change_&nbsp;: s’améliorer en continue, de manière incrémentale.
_Respect the current process, roles, responsibilities and titles_&nbsp;: le changement se fait en douceur, à chaque nouvelle amélioration.
Pas de changement de paradigme comme c’est le cas de _Scrum_. _Encourage acts of leadership at all levels_&nbsp;:
pour des équipes responsables qui ajustent le système à tous les niveaux et à leur initiative.

Ces principes sont déclinés en six pratiques que nous venons de voir.
On peut résumer tout ça sur un tableau _kanban_ en visualisant les contraintes, les règles et les cadences.

Un des buts du management visuel est l’appropriation du système par l’équipe. Si le _kanban_ n’évolue pas régulièrement, c’est mauvais signe.
Voici un exemple de tableau vertical, puis un autre plus exotique encore. Celui-ci est utilisé pour faire mûrir un _backlog_.
Ici nous avons un portefeuille de projets. Des services comme le _marketing_, la _TMA_ ou l’exploitation sont aussi friands de _Kanban_.
Un autre exemple sur la gestion d’une cave à vin.
Un autre sur une consommation de jeux vidéo, et pour finir un exemple de _Kanban_ personnel pour gérer ses tâches quotidiennes.

En conclusion, je dirai que la force de _Kanban_ est son adaptation à tous les environnements grâce à son développement en flux
qui vise à optimiser la production de valeur et à minimiser le gaspillage, le tout de manière empirique et sans changement radical de vos process.

Merci pour votre attention.