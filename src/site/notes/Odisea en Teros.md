---
{"dg-publish":true,"permalink":"/odisea-en-teros/","tags":["gardenEntry"]}
---

¡Bienvenido a Teros!
Este es nuestro sitio de referencia para la campaña. Aquí podrás encontrar los diarios de nuestras sesiones e información sobre los lugares que descubres y las personas con las que interactúas a lo largo de la aventura. 
## Sesiones
``` dataviewjs
let list = await dv.queryMarkdown(`LIST FROM "Sesiones" SORT file.name ASC`);
await dv.paragraph(list.value);
```
