---
description: Tamaño normalizado. Se utiliza para especificar tamaños de imagen o rectángulos, normalizados en relación con el tamaño de la capa 0 o alguna otra imagen.
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# sizeN{#sizen}

Tamaño normalizado. Se utiliza para especificar tamaños de imagen o rectángulos, normalizados en relación con el tamaño de la capa 0 o alguna otra imagen.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>anchura y altura normalizadas relativas a otra imagen (real, real, bueno que 0) </p></td> 
 </tr> 
</table>

Tanto *nx* como *ny* deben ser buenos que 0. 0,0 puede indicar que se debe utilizar un tamaño predeterminado específico. 1,1 especifica un tamaño igual a la imagen de referencia.
