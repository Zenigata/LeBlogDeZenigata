---
layout: post
title: "Challenge interclubs"
date: 2014-08-13 15:00
comments: true
categories: [jeu de go]
---
Encore une année vide de tournois de go, mais quelques affrontements m'ont tout de même permis de franchir la barre du 4<sup>e</sup> kyū.
<!--more-->

Le challenge d'Île-de-France est une ancienne compétition interclubs à laquelle j'ai [déjà participé](http://ffg.jeudego.org/php/affichePersonne.php?id=6309).
Un peu comme dans _Hikaru no go_, chaque club présente une équipe de trois personnes, à raison d'un match par mois.
Par le passé, on s'affrontait également en _[rengo](http://senseis.xmp.net/?PairGo)_.

J'ai réalisé un compte-rendu de la dernière édition sur [le site du club](http://boulogne.jeudego.org/?p=459).

J'aimerais vous présenter ici la partie que j'ai faite à la troisième ronde contre
[Steven de Oliveira](http://ffg.jeudego.org/php/affichePersonne.php?id=10071) (2k) qui me donnait donc trois pierres de handicap.
Steven est aujourd'hui à un niveau _shodan_ mais il va abandonner avant la fin de cette partie, me laissant lui rafler assez de points pour passer 4<sup>e</sup> kyū.

<div id="glift"></div>

<button id="tlButton">Charger la partie</button>
<div id="glift_display1" style="height:500px; width:100%; position:relative;"></div>

<script type="text/javascript">
  (function($) {
    $('#tlButton').click(loadGlift);
    function loadGlift() {
      $.ajax({url: "{{ root_url }}/javascripts/custom/glift.min.js", dataType: "script", success: initGlift});
      $('#tlButton').hide();
    }
  })(jQuery)

  function initGlift() {
    gliftWidget = glift.create({
      sgf: {sgfString: '(;GM[1]FF[4]AP[Drago:4.21]SZ[19]CA[UTF-8]AB[pd][dd][dp]PW[Steven De Oliveira]PB[Johan Bonneau]WR[2k]WT[91sm]BR[5k]BT[92bo]TM[3600]DT[21-01-2014]RE[B+R]GN[1]EV[Challenge IDF 2013]RO[3]PC[Boulogne-Billancourt];W[qo];B[pp];W[po];B[op];W[qp];B[qq];W[rq];B[oo];W[pm];B[jp];W[cf];B[ch];W[dn];B[dl];W[fn];B[fp];W[fl];B[eh];W[im];B[ce];W[nc];B[qf];W[pb];B[qc];W[kc];B[gc];W[cc];B[be];W[ec];B[dc];W[db];B[ed];W[bb];B[fc];W[gh];B[ac];W[ab];B[ca];W[ba];B[ej];W[gj];B[qi];W[lp];B[kn];W[mn];B[kl];W[ml];B[on];W[ql];B[mo];W[lo];B[ln];W[jq];B[iq];W[ip];B[kq];W[jo];B[jr];W[ko];B[mm];W[cq];B[cp];W[dr];B[bq];W[br];B[dq];W[cr];B[bp];W[fq];B[eq];W[gp];B[gq];W[hq];B[fr];W[hr];B[mr];W[mp];B[nn];W[nq];B[nr];W[oq];B[or];W[pr];B[pq];W[qr];B[os];W[ms];B[lq];W[ks];B[kp];W[io];B[ir];W[gs];B[fs];W[nl];B[kj];W[jk];B[kk];W[ph];B[qh];W[pf];B[pi];W[qe];B[pe];W[qg];B[rf];W[rg];B[re];W[oh];B[of];W[pg];B[nj];W[mh];B[pk];W[ok];B[ni];W[nh];B[qk];W[oj];B[oi];W[pl];B[me];W[kh];B[qb];W[ob];B[ke];W[mj];B[mi];W[li];B[mk];W[lj];B[nk];W[lk];B[rh];W[ll];B[sg]MA[iq][ir][jr][kq][jp][kp][lq][mr][nr][or][os][qq][pq][pp][op][oo][on][nn][mm][mo][ln][kn][kl][kk][kj])'},
      divId: "glift_display1",
      display: {
        theme: 'TRANSPARENT'
      }
    });
  }
</script>

J'ai refait la partie de mémoire donc certains coups peuvent être approximatifs.

Aucun commentaire ne m'a malheureusement été fait de la part des membres de mon club.
C'est dommage car si l'on regarde nos positions à la fin de l'enregistrement, Blanc n'a certes pas beaucoup de points mais il maintient une pression énorme sur les pierres annotées d'une croix.

Et pourtant, quand Blanc m'a isolé ces deux groupes, je ne m'inquiétais pas plus que ça. Pourquoi donc&nbsp;? Que faire dans cette situation&nbsp;? Vous avez deux minutes...

Solution&nbsp;: <button id="solButton">afficher</button><span id="solSpan" style="display:none;">mon prochain coup fut le début d'un _[sekito-shibori](http://senseis.xmp.net/?TwoStoneEdgeSqueeze)_ que Steven n'avait pas anticipé. Il a abandonné peu après.<span>

<script type="text/javascript">
  (function($) {
    $('#solButton').click(reveal);
    function reveal() {
      $('#solButton').hide();
      $('#solSpan').show();
    }
  })(jQuery)
</script>