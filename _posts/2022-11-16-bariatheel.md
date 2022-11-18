---
title: Bariatheel
author: cotes
date: 2022-11-16 20:20:20 +0200
categories: [Place, City]
tags: [grimor, marirines]
geojson:
  type: Feature
  properties:  
    state: Grimor
    region: 'Bariatheel'
    name: 'Bariatheel'
    amenity: 'Città'
    description: 'La città più antica e grande di Grimor nonchè la sua la capitale politica ed economica.'
  geometry:
    type: Point
    coordinates: [1136, 1334]
map_data: 
  id: 'Bariatheel'
  url: 'https://www.worldanvil.com/uploads/maps/332dfdead036a200342f5c4a7a4b8c6d.png'
  options:
    center: [1143, 1312.5]
    zoom: 0
---

## Storia recente

La città di Bariatheel è la città più antica e grande di Grimor diventandone di conseguenza anche la capitale politica ed economica.
Negli ultimi secoli la città di Bariatheel ha avuto diversi sconvolgimenti politico in seguito alla ricomparsa di Yvuul e la scomparsa prematura della famiglia regnante dei Marirines.
 
Dopo l'avvento di Yvuul sulla città ed i conseguenti scontri la città ha impiegato parecchio tempo per recuperare dalle ferite subite,
in particolar modo in seguito alla morte dei membri della famiglia dei Marirines la città ha dovuto affrontare un periodo di governi dalla breve durata
e caratterizzati da una forte impronta militare questo periodo, noto come "I regni dei cinque re", ha visto numerosi scontri tra le famiglie nobiliari
ed il popolo ormai piegato dalla fame e dalla miseria.
Evento di particolare importanza è quello legato al "Inverno rosso di Bariatheel" dove un nuovo gruppo di rivoluzionari guidati
da quello che in seguito diventerà re dichiarò apertamente guerra al governo reggente causando una nuova e violenta serie di scontri.
 
Dopo la caduta di quest'ultimo governo, l'elfo Eberon controlla la città e, per prevenire ulteriori governi dittatoriali,
viene creato il "Consiglio di Bariatheel" organo che, assieme al re, governa la vita cittadina e l'intero apparato militare della regione.
 
Attualmente la città si trova in una posizione scomoda: in seguito agli eventi della rosa nera la popolazione ripone meno fiducia nelle guarnigione cittadina e,
col malcontento ormai dilagante, gli affiliati del corvo stanno riuscendo ad influenzare sempre di più la popolazione.
Nel tempo sono comparse diverse rivolte ma la maggior parte di esse si sono concluse con solamente qualche arresto ...
tuttavia la lontananza dell'esercito da Bariatheel e la necessità di risolvere i problemi nati dalla caduta di Anstol
stanno causando un aumento sempre più rapido del malcontento: ormai è solo questione di tempo prima che qualcosa scoppi.

## Mappa


{% include custom_map.html id=page.map_data.id url=page.map_data.url options=page.map_data.options %}

{%- for post in site.posts -%}
  {% if post.POIs and post.location and post.location.state == page.geojson.properties.state and post.location.region == page.geojson.properties.name %}
    {%- for POI in post.POIs -%}

      {% include custom_map_marker.html mapid=page.map_data.id geoJSONFeature=POI url=post.url %}
      
    {% endfor %}
  {% endif %}
{% endfor %}
