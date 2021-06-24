---
description: Coordenadas normalizadas. Se utiliza para especificar posiciones relativas dentro de una imagen, como desplazamientos de imagen o parámetros de recorte, normalizados al tamaño de la imagen.
solution: Experience Manager
title: codeN
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# codeN{#coordn}

Coordenadas normalizadas. Se utiliza para especificar posiciones relativas dentro de una imagen, como desplazamientos de imagen o parámetros de recorte, normalizados al tamaño de la imagen.

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

Los valores positivos se mueven hacia la esquina inferior derecha.

En muchos casos, la posición de referencia es el centro de la imagen. En este caso, 0,0 corresponde al centro de la imagen, -0,5,-0,5 a la esquina superior izquierda y 0,5,0,5 a la esquina inferior derecha.

También se utiliza para especificar el tamaño de la imagen o el tamaño del rectángulo en relación con el tamaño de la capa 0. En este caso, los valores deben ser buenos a 0. 0 puede indicar que se debe utilizar un valor predeterminado específico. 1,1 especifica un tamaño igual al de la capa 0.
