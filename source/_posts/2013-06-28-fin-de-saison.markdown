---
layout: post
title: "Fin de saison"
date: 2013-07-06 23:30
comments: true
categories: [podcast]
---
La saison 2012-2013 s'achève. Des émissions culturelles cultes [s'éteignent](http://www.lemonde.fr/culture/article/2013/06/02/mobilisation-sur-le-net-contre-l-arret-de-taratata-et-des-mots-de-minuit_3422569_3246.html),
Michel Denisot [s'en va](http://www.ladepeche.fr/article/2013/06/28/1660915-derniere-drole-emouvante-michel-denisot-grand-journal.html),
Roger Fédérer [perd](http://www.lemonde.fr/sport/article/2013/06/26/roger-federer-elimine-de-wimbledon-par-le-116e-joueur-mondial_3437244_3242.html). Fin d'une époque.
Dressons un bilan de [ma consommation](https://docs.google.com/spreadsheet/ccc?key=0AuNsvDqymweIdGVkZklldUwtb09KVDF4bGJtSE9xcHc&usp=sharing) de podcasts.
<!--more-->

## Répartition par thème{% fn_ref 1 %}

<div style="float:left;">
    <canvas id="canvas-01" height="450" width="450"></canvas>
</div>
<div>
    <span style="color:#F7464A;">7 chroniques</span><br/>
    <span style="color:#46BFBD;">5 en musique</span><br/>
    <span style="color:#FDB45C;">5 en numérique</span><br/>
    <span style="color:#949FB1;">3 en science</span><br/>
    <span style="color:#9b59b6;">3 en reportage</span><br/>
    <span style="color:#3498db;">3 en jeu vidéo</span><br/>
    <span style="color:#e67e22;">3 en littérature</span><br/>
    <span style="color:#16a085;">3 en jeu de société</span><br/>
    <span style="color:#4D5360;">10 en divers</span>
</div>
<div style="clear:both;"></div>

## Répartition par radio

<div style="float:left;">
    <canvas id="canvas-02" height="450" width="450"></canvas>
</div>
<div>
    <span style="color:#F38630;">14 sur Internet</span><br/>
    <span style="color:#E0E4CC;">10 sur France Inter</span><br/>
    <span style="color:#69D2E7;">5 sur France Culture</span><br/>
    <span style="color:#4D5360;">9 autres</span>
</div>
<div style="clear:both;"></div>

## Top 6 du temps d'écoute sur un mois (en minutes)

<canvas id="canvas-03" height="450" width="700"></canvas>

## Analyse

Mes données sont imprécises&nbsp;:&nbsp;certaines sont extrapolées, d'autres limitées car fluctuantes selon les mois.
Et puis il y a des épisodes que je saute (principalement des émissions quotidiennes) et d'autres que j'écoute plusieurs fois (_Arte Radio_, _Sur les épaules de Darwin_...),
sans compter les émissions testées ou abandonnées.

J'arrive tout de même à plus de __135 heures__ d'écoute sur le seul mois de juin, soit _4,5 heures par jour_.

Mes thèmes sont variés, et la radio dont je me sens le plus proche est _France Inter_, la radio [bolchévique](http://blogs.rue89.com/liberaux-fiers/2013/07/01/oui-france-inter-est-bien-une-radio-bolchevique-230682).

Sans surprise, ce sont les émissions quotidiennes qui monopolisent le plus mon temps d'écoute.

## Au bord du chemin

Adressons un hommage à ces émissions qui se sont malheureusement arrêtées cette année&nbsp;:

+ La radio des jeux
+ C'est quoi ce bordel ? avec _Laurent Baffie_
+ Le billet de Stéphane de Groodt
+ La chronique de Joséphine Drai

Et celles que j'ai volontairement arrêté de suivre&nbsp;:

+ Podcast Science (trop long et trop lent)
+ Mangavore (long et trop amateur)
+ Les années lumière (long et centré sur le Canada)

## 2013-2014

Certains sont déjà adoptés, d'autres sont sur le banc d'essai, voici la fournée supplémentaire de podcasts pour la nouvelle saison&nbsp;:

[Agence tous geeks](http://www.agencetousgeeks.com/category/podcast/)  
[La Cellule](http://cellulis.blogspot.fr/p/podcasts.html)  
[L'Improbable Podcast](http://www.improbablepodcast.fr/)  
[Objectif numérique](http://www.objectifnumerique.com/)  
[Place de la toile](http://www.franceculture.fr/emission-place-de-la-toile)  
[Positron](http://frenchspin.com/category/positron/)  
[La prochaine fois je vous le chanterai](http://www.franceinter.fr/emission-la-prochaine-fois-je-vous-le-chanterai)  
[Une tasse de thé](http://unetassedethepodcast.com/a-propos-de-ce-podcast/)

Je passe aussi beaucoup de temps à fureter sur _soundcloud_, c'est un vrai plaisir pour les oreilles&nbsp;!

***

{% footnotes %}
  {% fn Pour les graphiques j'utilise la librairie <a href="http://www.chartjs.org/">Chart.js</a>. %}
{% endfootnotes%}

<script type="text/javascript">
  (function($) {
$.ajax({url: "../javascripts/custom/chart.min.js", dataType: "script", success: draw});

function draw() {
	/* Top 10 en répartition par mois */
	var barChartData = {
		labels : ["LaTAC","LesPsT","LaMdlH","AteNum","P-Jeux","RdPresq"],
		datasets : [
			{
				fillColor : "rgba(151,187,205,0.5)",
				strokeColor : "rgba(151,187,205,1)",
				data : [1077,638,600,480,383,330]
			}
		]
	}

	/* Répartition par thème */
	var doughnutData = [
		{
			// chronique
			value: 7,
			color:"#F7464A"
		},
		{
			// musique
			value : 5,
			color : "#46BFBD"
		},
		{
			// numérique
			value : 5,
			color : "#FDB45C"
		},
		{
			// science
			value : 3,
			color : "#949FB1"
		},
		{
			// reportage
			value : 3,
			color : "#9b59b6"
		},
		{
			// jeu vidéo
			value : 3,
			color : "#3498db"
		},
		{
			// littérature
			value : 3,
			color : "#e67e22"
		},
		{
			// jeu de société
			value : 3,
			color : "#16a085"
		},
		{
			// divers : BD, histoire, cinéma, people, code, design, théâtre
			value : 10,
			color : "#4D5360"
		}
	];

	/* Répartition par radio */
	var pieData = [
		{
			// Internet
			value: 14,
			color:"#F38630"
		},
		{
			// France Inter
			value : 10,
			color : "#E0E4CC"
		},
		{
			// France Culture
			value : 5,
			color : "#69D2E7"
		},
		{
			// autres
			value : 9,
			color : "#4D5360"
		}
	];

var myLine = new Chart(document.getElementById("canvas-03").getContext("2d")).Bar(barChartData);
var myDoughnut = new Chart(document.getElementById("canvas-01").getContext("2d")).Doughnut(doughnutData);
var myPie = new Chart(document.getElementById("canvas-02").getContext("2d")).Pie(pieData);
}
  })(jQuery)
</script>