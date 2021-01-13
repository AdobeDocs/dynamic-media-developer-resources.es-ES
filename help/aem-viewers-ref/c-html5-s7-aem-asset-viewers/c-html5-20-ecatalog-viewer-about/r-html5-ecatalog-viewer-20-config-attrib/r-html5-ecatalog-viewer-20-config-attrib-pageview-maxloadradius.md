---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic media
uuid: 425624c5-3cbe-4b63-8c6b-eff31f2ed919
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---


# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica el comportamiento de precarga del componente. </p> <p>Cuando se establece en <span class="codeph"> -1</span>, el componente carga previamente todos los cuadros de catálogo cuando se encuentra en estado inactivo. </p> <p> Cuando se establece en <span class="codeph"> 0</span>, el componente carga solo el fotograma que está visible actualmente, anterior y siguiente. </p> <p>Establezca <span class="codeph"><span class="varname"> preloadnbr</span></span> para definir cuántos fotogramas invisibles alrededor del marco mostrado actualmente se cargan previamente en estado inactivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-4b7952997f9240e581d21bcdb173f9af}

Opcional.

## Predeterminado {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Ejemplo {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
