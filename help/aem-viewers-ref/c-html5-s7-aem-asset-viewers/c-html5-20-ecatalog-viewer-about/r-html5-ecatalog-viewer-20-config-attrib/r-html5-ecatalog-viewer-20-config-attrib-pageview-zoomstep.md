---
title: PageView.zoomstep
description: PageView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 64cce312-c13b-49c7-af85-3349ff5c4322
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *`paso`*[, *`límite`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> paso</span></span> </p> </td> 
   <td colname="col2"> <p> Configura el número de acciones de ampliar y alejar necesarias para aumentar o disminuir la resolución mediante un factor de dos. El cambio de resolución para cada acción de zoom es de 2^1 por paso. Definir en <span class="codeph"> 0</span> para ampliar a la resolución completa con una única acción de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> límite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la resolución de zoom máxima en relación con la imagen con resolución completa. El valor predeterminado es <span class="codeph"> 1.0</span>, que no permite un zoom superior a la resolución completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-636d35a4791447039f1902973f568320}

Opcional.

## Predeterminado {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## Ejemplo {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
