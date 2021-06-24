---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Developer,Business Practitioner
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`precarga`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica el comportamiento de precarga del componente. </p> <p>Cuando se establece en <span class="codeph"> -1</span>, el componente carga previamente todas las tramas del catálogo en estado inactivo. </p> <p> Cuando se establece en <span class="codeph"> 0</span>, el componente carga solo el fotograma que está visible actualmente, anterior y siguiente. </p> <p>Establezca <span class="codeph"><span class="varname"> precarga</span></span> para definir cuántos marcos invisibles alrededor del marco mostrado actualmente se cargan previamente en estado inactivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-4b7952997f9240e581d21bcdb173f9af}

Opcional.

## Predeterminado {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Ejemplo {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
