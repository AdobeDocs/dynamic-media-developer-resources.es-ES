---
description: Tamaño normalizado. Se utiliza para especificar tamaños de imagen o rectángulos, normalizados en relación con el tamaño de la capa 0 o con alguna otra imagen.
seo-description: Tamaño normalizado. Se utiliza para especificar tamaños de imagen o rectángulos, normalizados en relación con el tamaño de la capa 0 o con alguna otra imagen.
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# sizeN{#sizen}

Tamaño normalizado. Se utiliza para especificar tamaños de imagen o rectángulos, normalizados en relación con el tamaño de la capa 0 o con alguna otra imagen.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>anchura y altura normalizadas en relación con otra imagen (real, real, bueno que 0) </p></td> 
 </tr> 
</table>

Tanto *nx* como *ny* deben ser buenos que 0. 0,0 puede indicar que se debe utilizar un tamaño predeterminado específico. 1,1 especifica un tamaño igual a la imagen de referencia.
