---
layout: post
title: "Mon premier livre numérique"
date: 2012-08-08 18:10
comments: true
categories: [techno]
---
Qu'entend-on par [livre numérique](http://fr.wikipedia.org/wiki/Livre_num%C3%A9rique) ?  
Certainement beaucoup de choses ! rien qu'au niveau des formats disponibles : _.txt_, _.html_ ou _.pdf_ pour n'en citer que quelques-uns. Et bien je vais vous montrer comment réaliser votre premier&nbsp;_[.epub](http://fr.wikipedia.org/wiki/EPUB_\(format\))_. Ce format ouvert et standardisé tend à s'imposer. Vous pouvez par exemple en récupérer plein de gratuits au sein du [Projet Gutenberg](http://www.gutenberg.org/wiki/FR_Principal).
<!--more-->
Vous trouverez sur Internet les [spécifications du format](http://idpf.org/epub/30/spec/epub30-overview.html), ainsi que de nombreux [tutoriaux](http://www.ebouquin.fr/2010/02/04/comment-creer-un-fichier-epub/).

## L'archive

Un fichier _epub_, c'est juste une archive __zip__ qui contient des pages __html__ et des __métadonnées__ au sujet de votre livre. Voilà tout.

Je vous ai concocté un [exemple](https://docs.google.com/open?id=0B-NsvDqymweIU1RXS3VqOEJjbTg) :
<pre>
zenigata.epub
├── EPUB
│   ├── content.opf
│   ├── css
│   │   └── epub.css
│   ├── images
│   │   └── zenigata.jpg
│   ├── text
│   │   ├── 01-poemes.xhtml
│   │   ├── 02-fables.xhtml
│   │   ├── nav.xhtml
│   │   └── titre.xhtml
│   └── toc.ncx
├── META-INF
│   └── container.xml
└── mimetype
</pre>

## Les fichiers

Les fichiers __mimetype__ et __container.xml__ sont les mêmes pour tous les livres.

#### _content.opf_

Ce fichier contient les __métadonnées__ liées à l'ouvrage : auteur, date de parution, éditeur, genre, nombre de pages, etc.  
Il décrit également le contenu exhaustif de l'archive.

#### _toc.ncx_

Ce fichier facultatif peut être utilisé pour créer une __table des matières__ accessible à tout moment (sur le _Sony PRS-T1_ il faut faire _menu -> Naviguer page -> Table des matières_).

#### _code html_

Le reste des fichiers représente du code html basique avec du css et une image pour la couverture.

Il ne reste plus qu'à créer l'archive :
<pre>
zip -Xr zenigata.epub mimetype META-INF EPUB
</pre>

## FAQ

Pour tester votre livre numérique, de nombreux [visionneurs d'epub](http://blog.kowalczyk.info/articles/epub-ebook-reader-viewer-for-windows.html) sont disponibles selon votre système d'exploitation.

Un outil utile : le [validateur d'epub](http://code.google.com/p/epubcheck/). Très pratique !

Pensez à écrire _<!DOCTYPE html>_ et non _<!doctype html>_ si vous faites du __html 5__.

Vous trouverez des exemples d'epub fonctionnels à cet [endroit](http://code.google.com/p/epub-samples/).

Si les spécifications en ligne ne sont pas assez claires, jetez un œil sur ce [site](http://matt.garrish.ca/epub3/guidelines/). 

#### À vous les joies de l'édition !
