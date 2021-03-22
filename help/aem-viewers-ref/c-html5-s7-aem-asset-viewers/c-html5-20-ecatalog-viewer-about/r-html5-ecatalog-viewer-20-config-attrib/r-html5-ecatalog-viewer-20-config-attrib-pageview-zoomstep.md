---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
uuid: 11458300-4a1b-4623-8ea1-db804daab3cf
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 6%

---


# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> paso</span></span> </p> </td> 
   <td colname="col2"> <p> Configura el número de acciones de acercamiento y alejamiento necesarias para aumentar o reducir la resolución en un factor de dos. El cambio de resolución para cada acción de zoom es de 2^1 por paso. Establézcalo en <span class="codeph"> 0</span> para hacer zoom a resolución completa con una sola acción de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> límite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la resolución máxima de zoom, en relación con la imagen de resolución completa. El valor predeterminado es <span class="codeph"> 1.0</span>, lo que no permite ampliar el zoom más allá de la resolución completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-636d35a4791447039f1902973f568320}

Opcional.

## Predeterminado {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## Ejemplo {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
