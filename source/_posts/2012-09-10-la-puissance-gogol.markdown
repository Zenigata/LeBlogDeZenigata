---
layout: post
title: "La puissance gogol"
date: 2012-09-14 17:00
comments: true
categories: [dixit, javascript]
---
L'entrée du jour dans le __DiXIt__ est une notion mathématique : le [gogol](http://fr.wikipedia.org/wiki/Gogol_\(nombre\)).
<!--more-->
Ce terme (« [googol](http://fr.wiktionary.org/wiki/gogol) » en anglais) a été inventé pour représenter le nombre __10<sup>100</sup>__ :
<pre>10 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000</pre>  
Il est à l'origine du nom de la société [Google](http://www.google.fr/).

Le terme non moins original de « [gogolplex](http://fr.wikipedia.org/wiki/Gogolplex) » représente lui le nombre __10<sup>gogol</sup>__.  
Google s'en est encore inspiré, cette fois pour le nom du siège de l'entreprise.

Un gogol est à peu près égal à la factorielle de 70{% fn_ref 1 %}{% fn_ref 2 %} :  
<div>
  \[70! = \prod^{70}_{n=1} n = 70 \times 69 \times 68 \times \ldots \times 2 \times 1 \approx 1.2 \times 10^{100}\]
</div>

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>

Pour illustrer cette nouvelle entrée du __DiXIt__ je vous propose de réviser les fonctions trigonométriques (rien à voir certes){% fn_ref 3 %} :

<div id="box" class="jxgbox" style="width:600px;height:600px;"></div>
<script type="text/javascript">
  (function($) {
    $('body').append('<link rel="stylesheet" href="http://jsxgraph.uni-bayreuth.de/distrib/jsxgraph.css" type="text/css" />');
    $.ajax({url: "http://jsxgraph.uni-bayreuth.de/distrib/jsxgraphcore.js", dataType: "script", success: drawGraph});
    function drawGraph() {
      var brd = JXG.JSXGraph.initBoard('box', {originX: 300, originY: 300, grid:true, unitX: 100, unitY: 100});
      var ax = brd.createElement('line',[[0,0],[1,0]],{visible:false});
      var ay = brd.createElement('line',[[0,0],[0,1]],{visible:false});

      var p0 = brd.createElement('point',[0,0],{fixed:true,visible:false});
      var p1 = brd.createElement('point',[1,0],{name:'',visible:false,fixed:true});
      var c = brd.createElement('circle',[p0,p1],{dash:2,strokeWidth:1,strokeOpacity:0.6});
      var p2 = brd.createElement('glider',[0.4,1.0,c],{name:'',withLabel:false});
      var p3 = brd.createElement('point',[function(){return p2.X();},0.0],{visible:false,name:'',withLabel:false});
      var p4 = brd.createElement('point',[0.0,function(){return p2.Y();}],{visible:false,name:'',withLabel:false});

      brd.createElement('line',[p0,p2],{straightFirst:false,straightLast:false,strokeColor:'black'});   // Hypotenuse
      brd.createElement('line',[p2,p3],{straightFirst:false,straightLast:false,strokeColor:'red'});     // sin
      brd.createElement('line',[p2,p4],{straightFirst:false,straightLast:false,strokeColor:'red'});     // cos

      var t = brd.createElement('tangent',[p2],{visible:false});
      var p5 = brd.createElement('point',[brd.intersectionFunc(t,ax,0)],{visible:false,name:'',withLabel:false});
      var p6 = brd.createElement('point',[brd.intersectionFunc(t,ay,0)],{visible:false,name:'',withLabel:false});
      brd.createElement('line',[p5,p6],{straightFirst:false,straightLast:false});                       // tan + cot
      brd.createElement('line',[p0,p6],{straightFirst:false,straightLast:false,strokeColor:'green'});   // csc
      brd.createElement('line',[p0,p5],{straightFirst:false,straightLast:false,strokeColor:'green'});   // sec

      brd.createElement('text',[
            function(){return (p0.X()+p2.X())*0.5;},
            function(){return (p0.Y()+p2.Y())*0.5;},
            '1'],{});

      brd.createElement('text',[
            function(){return (p2.X()+p4.X())*0.3;},
            function(){return (p2.Y()+p4.Y())*0.5;},
            'cos'],{});

      brd.createElement('text',[
            function(){return (p2.X()+p3.X())*0.5;},
            function(){return (p2.Y()+p3.Y())*0.5;},
            'sin'],{});

      brd.createElement('text',[
            function(){return 0.1+(p2.X()+p5.X())*0.5;},
            function(){return 0.1+(p2.Y()+p5.Y())*0.5;},
            'tan'],{});

      brd.createElement('text',[
            function(){return 0.1+(p2.X()+p6.X())*0.5;},
            function(){return 0.1+(p2.Y()+p6.Y())*0.5;},
            'cot'],{});

      brd.createElement('text',[
            function(){return -0.2+(p0.X()+p6.X())*0.5;},
            function(){return (p0.Y()+p6.Y())*0.5;},
            'csc'],{});

      brd.createElement('text',[
            function(){return (p0.X()+p5.X())*0.5;},
            function(){return (p0.Y()+p5.Y())*0.5;},
            'sec'],{});
    }
  })(jQuery)
</script>

***

{% footnotes %}
  {% fn Source : <a href="http://omnilogie.fr/O/Google_et_Gogol">Omnilogie</a> %}
  {% fn Utilise la librairie <a href="http://www.mathjax.org/">MathJax</a> %}
  {% fn Utilise la librairie <a href="http://jsxgraph.uni-bayreuth.de/wiki/index.php/Trigonometric_functions">JSXGraph</a> %}
{% endfootnotes%}
