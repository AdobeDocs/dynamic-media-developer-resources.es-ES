---
description: Coordenadas normalizadas. Se utiliza para especificar posiciones relativas dentro de una imagen, como desplazamientos de imagen o parámetros de recorte, normalizados según el tamaño de la imagen.
seo-description: Coordenadas normalizadas. Se utiliza para especificar posiciones relativas dentro de una imagen, como desplazamientos de imagen o parámetros de recorte, normalizados según el tamaño de la imagen.
seo-title: codeN
solution: Experience Manager
title: codeN
topic: Scene7 Image Serving - Image Rendering API
uuid: e182650b-aff6-4dd2-8edb-cd0d361865fd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---


# codeN{#coordn}

Coordenadas normalizadas. Se utiliza para especificar posiciones relativas dentro de una imagen, como desplazamientos de imagen o parámetros de recorte, normalizados según el tamaño de la imagen.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> codeN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>desplazamiento de coordenadas normalizado al tamaño de una imagen (real, real) </p></td> 
 </tr> 
</table>

Los valores positivos se mueven hacia abajo a la derecha.

En muchos casos, la posición de referencia es el centro de la imagen. En este caso, 0,0 corresponde al centro de la imagen, -0,5, -0,5 a la esquina superior izquierda y 0,5 a la esquina inferior derecha.

También se utiliza para especificar los tamaños de imagen o el tamaño del rectángulo en relación con el tamaño de la capa 0. En este caso, los valores deben ser buenos que 0. 0 puede indicar que se debe utilizar un valor predeterminado específico. 1,1 especifica un tamaño igual al de la capa 0.
