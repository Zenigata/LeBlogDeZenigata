---
layout: post
title: "Pendant ce temps-là en 1985"
date: 2012-04-06 18:10
comments: true
categories: [my life, javascript]
---
Quel est votre rapport au temps qui passe ?

À défaut de lapin en chocolat pour Pâques, les Papous ont évoqué dimanche dernier ([mp3](http://media.radiofrance-podcast.net/podcast09/13364-01.04.2012-ITEMA_20356977-0.mp3)) le lapin pressé de Lewis Carroll, ainsi que le fameux Chapelier :
_« Le Temps n’admet pas qu’on le veuille marquer comme le bétail»_.

__Les jours passent comme des voitures__, dit l'autre. Jettons un coup d'oeil au rétroviseur !  
<!--more-->
<button id="tlButton">Frisez-moi !</button>
<div id="timeline" style="display:none;"></div>
<div class="tlFake" style="height:760px;display:none;"></div>
<p class="tlFake" style="display:none;">Et vous, que faisiez-vous en 1985 ?</p>
<script type="text/javascript">
  (function($) {
    $('#tlButton').click(loadTimeline);
    function loadTimeline() {
      $('head').append('<link rel="stylesheet" href="{{ root_url }}/stylesheets/timeline.css" type="text/css" />');
      $.ajax({url: "{{ root_url }}/javascripts/timeline-min.js", dataType: "script", success: initTimeline});
      $('#tlButton').hide();
      $('#timeline').show();
      $('.tlFake').show();
    }
    function initTimeline(data) {
      eval(data);
      var timeline = new VMM.Timeline(790, 760);
      timeline.init("{{ root_url }}/javascripts/json/1985.json");
    }
  })(jQuery)
</script>
