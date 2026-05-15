---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d92e56ae-2bb6-46f6-b0f7-64b867492a37
TQID: 'https://experienceleague.adobe.com/fceYX6xApL3EyDRk3FQFnzew7C4-Ax3acpPJH-HVrKw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *`paso`*[, *`límite`*]`]

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

[!DNL `1,1`]

## Ejemplo {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
