---
title: Efecto Buscar
description: El visor muestra las regiones de resultados de búsqueda en la vista principal para resaltar las palabras o frases encontradas en el catálogo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# Efecto Buscar{#search-effect}

El visor muestra las regiones de resultados de búsqueda en la vista principal para resaltar las palabras o frases encontradas en el catálogo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área de visor principal**

El aspecto de las regiones de resultados de búsqueda se controla con el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fondo </span> </p> </td> 
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
