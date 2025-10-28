---
{"dg-home":true,"dg-publish":true,"dg-publish-dm":true,"permalink":"/odisea-en-teros/","tags":["gardenEntry"],"dgPassFrontmatter":true}
---

¡Bienvenido a Teros!
Este es nuestro sitio de referencia para la campaña. Aquí podrás encontrar los diarios de nuestras sesiones e información sobre los lugares que descubres y las personas con las que interactúas a lo largo de la aventura. 
## Sesiones
| File                                 | Description                                                             |
| ------------------------------------ | ----------------------------------------------------------------------- |
| [[Sesiones/Sesión 01\|Sesión 01]] | ¡La aventura comienza! Nuestras heroínas se conocen y exploran Meletis. |

{ .block-language-dataview}
## Dioses
| File                                 | Description                  |
| ------------------------------------ | ---------------------------- |
| [[Personas/Atreos\|Atreos]]       | Dios del Pasaje (él)         |
| [[Personas/Cénagos\|Cénagos]]     | Dios de la Rebeldía (él)     |
| [[Personas/Clotis\|Clotis]]       | Diosa del Destino (élla)     |
| [[Personas/Crufis\|Crufis]]       | Dios de los Horizontes (él)  |
| [[Personas/Efara\|Efara]]         | Diosa de la Polis (élla)     |
| [[Personas/Érebos\|Érebos]]       | Dios de la Muerte (él)       |
| [[Personas/Farika\|Farika]]       | Diosa de la Aflicción (élla) |
| [[Personas/Fénax\|Fénax]]         | Dios del Engaño (él)         |
| [[Personas/Heliodo\|Heliodo]]     | Dios del Sol (él)            |
| [[Personas/Iroas\|Iroas]]         | Dios de la Victoria (él)     |
| [[Personas/Karametra\|Karametra]] | Diosa de la Cosecha (élla)   |
| [[Personas/Keranos\|Keranos]]     | Dios de la Tormenta (él)     |
| [[Personas/Mogis\|Mogis]]         | Dios de la Violencia (él)    |
| [[Personas/Nilea\|Nilea]]         | Diosa de la Caza (élla)      |
| [[Personas/Pórforo\|Pórforo]]     | Dios de la Forja (él)        |
| [[Personas/Talasa\|Talasa]]       | Diosa de la Sabiduría (élla) |

{ .block-language-dataview}
## Personas
| File                                 | Description               |
| ------------------------------------ | ------------------------- |
| [[Personas/Bradeus\|Bradeus]]     | Humano Estudiante (él)    |
| [[Personas/Calafe\|Calafe]]       | Humana Marinera (élla)    |
| [[Personas/Chadeus\|Chadeus]]     | Leonido Estudiante (él)   |
| [[Personas/Cliros\|Cliros]]       | Leonido Magistrado (él)   |
| [[Personas/Cois\|Cois]]           | Humano Actor (él)         |
| [[Personas/La Víbora\|La Víbora]] | Humano Actor (él)         |
| [[Personas/Maro\|Maro]]           | Humano Dramaturgo (él)    |
| [[Personas/Metodia\|Metodia]]     | Humana Dramaturga (élla)  |
| [[Personas/Xenofia\|Xenofia]]     | Humana Filósofa (élla)    |
| [[Personas/Zagreo\|Zagreo]]       | Humano Bibliotecario (él) |

{ .block-language-dataview}
## Mapa

<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<style>
#map { height: 650px; width: 100%; }
.leaflet-control-attribution { display: none; }
</style>
<div id="map"></div>
<script>
var imageUrl = 'https://i.imgur.com/qkoMqpl.jpeg', 
imageWidth = 3300,
imageHeight = 2550,
imageBounds = [[0, 0], [imageHeight, imageWidth\|0, 0], [imageHeight, imageWidth]];
var map = L.map('map', {
crs: L.CRS.Simple,
minZoom: -2, // Allows zooming out to see the whole image
maxZoom: 2,  // Allows zooming in
});
map.fitBounds(imageBounds);
L.imageOverlay(imageUrl, imageBounds).addTo(map);
var markers = [
[769.8035, 1264.3069, "Teatro Fenaxicón", "https://teros.vercel.app/lugares/meletis/teatro-fenaxicon/"],
[1841.3334, 3020.0000, "Gran Estadio", "https://teros.vercel.app/lugares/meletis/gran-estadio/"],
[1222.1162, 1955.8574, "Dekatia", "https://teros.vercel.app/lugares/meletis/dekatia/"],
[935.8558, 1669.3613, "Templo del Conocimiento", "https://teros.vercel.app/lugares/meletis/templo-del-del-conocimiento/"],
[1265.0140, 1443.9120, "Ágora", "https://teros.vercel.app/lugares/meletis/agora/"],
[620.8333, 313.6666, "Gran Templo del Sol", "https://teros.vercel.app/lugares/meletis/gran-templo-del-sol/"],
[1897.6038, 446.4951, "Bastión Reverente", "https://teros.vercel.app/lugares/meletis/bastion-reverente/"],
[1696.3491, 292.0351, "Necrópolis", "https://teros.vercel.app/lugares/meletis/necropolis/"],
[2447.3334, 283.3333, "Santuario de la Cosecha", "https://teros.vercel.app/lugares/meletis/santuario-de-la-cosecha/"],
[929.1382, 968.7363, "Ministerio de los Doce", "https://teros.vercel.app/lugares/meletis/ministerio-de-los-doce/"],
[892.6666, 2084.3333, "Templo de las Olas", "https://teros.vercel.app/lugares/meletis/templo-de-las-olas/"],
[779.1667, 1720.5000, "Puerto", "https://teros.vercel.app/lugares/meletis/puerto/"],
[1305.3333, 3106.0000, "Teatro Agorrus", "https://teros.vercel.app/lugares/meletis/teatro-agorrus/"],
[2353.3334, 1439.3335, "Observatorio", "https://teros.vercel.app/lugares/meletis/observatorio/"],
];
markers.forEach(function(markerData) {
var y = markerData[0];
var x = markerData[1];
var title = markerData[2];
var link = markerData[3];
var popupContent = '<a href="' + link + '" target="_top">' + title + '</a>';
L.marker([y, x])
.bindPopup(popupContent, {
className: 'always-visible-popup' 
})
.addTo(map)
});
</script>