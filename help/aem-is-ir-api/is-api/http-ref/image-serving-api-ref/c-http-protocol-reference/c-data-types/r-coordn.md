---
title: coordN
description: Coordenadas normalizadas. Se utiliza para especificar posiciones relativas dentro de una imagen, como desplazamientos de imagen o parámetros de recorte, normalizados según el tamaño de la imagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
TQID: 'https://experienceleague.adobe.com/-dtYByOGK-mNAWc0yQBs4nu5sO1r-Ormq70iwdDZBjg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 0%

---

# coordN{#coordn}

Coordenadas normalizadas. Se utiliza para especificar posiciones relativas dentro de una imagen, como desplazamientos de imagen o parámetros de recorte, normalizados según el tamaño de la imagen.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>desplazamiento de coordenadas normalizado al tamaño de una imagen (real, real) </p></td> 
 </tr> 
</table>

Los valores positivos se mueven hacia la parte inferior derecha.

A menudo, la posición de referencia es el centro de la imagen. En este caso, `0,0` corresponde al centro de la imagen, `-0.5,-0.5` a la esquina superior izquierda y `0.5,0.5` a la esquina inferior derecha.

También se utiliza para especificar el tamaño de la imagen o el tamaño del rectángulo en relación con el tamaño de la capa 0. En este caso, el valor debe ser mayor que 0. 0 puede indicar que se debe utilizar un valor predeterminado específico. Un valor de `1,1` especifica un tamaño igual al de la capa 0.
