---
description: Escalar imagen. Escala una imagen por factor en relación con la imagen de resolución completa.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 8%

---

# scale{#scale}

Escalar imagen. Escala una imagen por factor en relación con la imagen de resolución completa.

`scale= *`factor`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> factor</span></span> </p> </td> 
  <td class="stentry"> <p>Factor de escala (real, &gt;0). </p></td> 
 </tr> 
</table>

## Predeterminado {#section-e9e53959b35844579f0f1d7721b71f8e}

Si no se especifica, la imagen se utilizará sin escalar.

## Ejemplo {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
