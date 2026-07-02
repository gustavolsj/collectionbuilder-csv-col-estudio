---
title: Acerca de
layout: about
permalink: /about.html
# include CollectionBuilder info at bottom
credits: true
# featured-image value can be one objectid for a photo object in this collection, a relative path to an image in this project, or a full url to any image. If left blank, no featured image will appear at top of About page.
about-featured-image: demo_031
# set background-position for featured image, "center", "top", "bottom"
position: bottom
# major heading to display over featured image
heading: Acerca de la colección
# paragraph text below heading in featured image
sub-heading:
# additional padding added to the feature to increase size. Give value in em or px, e.g. "5em".
padding: 6em
# Edit the markdown on in this file to describe your collection
# Look in _includes/feature for options to easily add features to the page
---

## Acerca de CollectionBuilder CSV

Esta colección de demostración reúne objetos de las [Colecciones Digitales](https://www.lib.uidaho.edu/digital/) de la Biblioteca de la Universidad de Idaho y está construida con [CollectionBuilder-CSV](https://github.com/CollectionBuilder/collectionbuilder-csv).

CollectionBuilder-CSV es una plantilla autónoma para crear sitios web de colecciones y exhibiciones digitales con Jekyll, a partir de:

- un CSV con los metadatos de la colección
- una carpeta con imágenes, PDF, audio o video

Guiada por los metadatos de la colección, la plantilla genera visualizaciones para recorrer y explorar los objetos.
El sitio estático resultante puede alojarse en cualquier servidor web básico.

[CollectionBuilder](https://github.com/CollectionBuilder/) es un conjunto de herramientas de código abierto para crear sitios web de colecciones y exhibiciones digitales basados en metadatos y construidos con tecnología web estática moderna.
Consulta la [documentación de CB](https://collectionbuilder.github.io/cb-docs/) para más información.

{% include feature/image.html objectid="demo_001" width="75" %}

<!-- IMPORTANT!!! DELETE this comment and the include below when you are finished editing this page for your collection. The include below introduces about page features. They will show up on your collection's about page until you delete it.  -->

{% include cb/about_the_about.md %}
