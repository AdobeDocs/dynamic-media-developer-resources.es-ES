---
description: El visor muestra las regiones de los resultados de búsqueda en la vista principal para resaltar las palabras o frases que se encuentran en el catálogo.
solution: Experience Manager
title: Efecto de búsqueda
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# Efecto de búsqueda{#search-effect}

El visor muestra las regiones de los resultados de búsqueda en la vista principal para resaltar las palabras o frases que se encuentran en el catálogo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

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
   <td colname="col2"> <p>Fondo de la región de resultados de la búsqueda. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar regiones de resultados de búsqueda con un relleno amarillo semitransparente:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```
