---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica el comportamiento de carga previa del componente. </p> <p>Cuando se establece en <span class="codeph"> -1</span> el componente carga de forma previa todos los fotogramas de catálogo cuando está en espera. </p> <p> Cuando se establece en <span class="codeph"> 0</span> el componente solo carga el marco que está visible actualmente, el anterior y el siguiente. </p> <p>Establecer <span class="codeph"><span class="varname"> preloadnbr</span></span> para definir cuántos fotogramas invisibles alrededor del fotograma mostrado actualmente se cargan previamente en estado inactivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-4b7952997f9240e581d21bcdb173f9af}

Opcional.

## Predeterminado {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Ejemplo {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
