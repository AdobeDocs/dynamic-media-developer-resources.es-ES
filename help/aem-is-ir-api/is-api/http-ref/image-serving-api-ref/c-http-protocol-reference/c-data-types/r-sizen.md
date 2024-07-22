---
description: Tamaño normalizado. Se utiliza para especificar tamaños de imagen o tamaños de rectángulo, normalizados en relación con el tamaño de la capa 0 o alguna otra imagen.
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# sizeN{#sizen}

Tamaño normalizado. Se utiliza para especificar tamaños de imagen o tamaños de rectángulo, normalizados en relación con el tamaño de la capa 0 o alguna otra imagen.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>anchura y altura normalizadas en relación con otra imagen (real, real, mayor que 0) </p></td> 
 </tr> 
</table>

Tanto *nx* como *ny* deben ser mayores que 0. 0,0 puede indicar que se debe utilizar un tamaño predeterminado específico. 1,1 especifica un tamaño igual a la imagen de referencia.
