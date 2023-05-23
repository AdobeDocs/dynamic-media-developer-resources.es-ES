---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d92e56ae-2bb6-46f6-b0f7-64b867492a37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---

# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *`escalón`*[, *`límite`*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> paso</span></span> </p> </td> 
   <td colname="col2"> <p> Configura el número de acciones de ampliar y alejar necesarias para aumentar o disminuir la resolución mediante un factor de dos. El cambio de resolución para cada acción de zoom es de 2^1 por paso. Configure como. <span class="codeph"> 0</span> para ampliar a resolución completa con una única acción de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> límite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la resolución de zoom máxima en relación con la imagen con resolución completa. El valor predeterminado es <span class="codeph"> 1,0</span>, que no permite un zoom superior a la resolución completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-636d35a4791447039f1902973f568320}

Opcional.

## Predeterminado {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## Ejemplo {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
