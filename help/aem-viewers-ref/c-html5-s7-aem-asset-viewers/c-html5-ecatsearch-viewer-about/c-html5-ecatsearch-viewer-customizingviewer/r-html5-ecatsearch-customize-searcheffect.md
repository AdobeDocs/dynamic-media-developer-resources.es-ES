---
description: El visor muestra las regiones de los resultados de búsqueda sobre la vista principal para resaltar las palabras o frases que se encuentran en el catálogo.
seo-description: El visor muestra las regiones de los resultados de búsqueda sobre la vista principal para resaltar las palabras o frases que se encuentran en el catálogo.
seo-title: Efecto de búsqueda
solution: Experience Manager
title: Efecto de búsqueda
topic: Dynamic media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Efecto de búsqueda{#search-effect}

El visor muestra las regiones de los resultados de búsqueda sobre la vista principal para resaltar las palabras o frases que se encuentran en el catálogo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto de las regiones de resultados de búsqueda se controla con el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fondo  </span> </p> </td> 
   <td colname="col2"> <p>Fondo de la región de resultados de búsqueda. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar regiones de resultados de búsqueda con un relleno amarillo y semitransparente:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

