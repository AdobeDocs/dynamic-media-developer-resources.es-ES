---
description: Alinear imagen con vista. Alinea la imagen compuesta (posiblemente después del escalado, si también se especifica scl=) dentro del rectángulo de vista definido por wid= y hei=.
solution: Experience Manager
title: alinear
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# alinear{#align}

Alinear imagen con vista. Alinea la imagen compuesta (posiblemente después del escalado, si también se especifica scl=) dentro del rectángulo de vista definido por wid= y hei=.

` align= *`horrendo`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horrendo </span> </span> </p> </td> 
  <td class="stentry"> <p>alineación horizontal (real, -1,0...1,0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>alineación vertical (real, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Especificar `align=-1,-1` para alinear la parte superior izquierda de la imagen compuesta con la parte superior izquierda de la vista, especifique `align=1,1` para alinear la parte inferior derecha de la imagen con la parte inferior derecha de la vista. Para las solicitudes de imagen estándar y miniaturas, cualquier área de la vista que no esté cubierta por datos de imagen compuesta se rellena con `bgc=`.

## Propiedades {#section-3fbec8206fc944eda4746d8be84f3b41}

Ver atributo. ( `align=` también se utiliza para definir la alineación entre una imagen de marca de agua y la imagen compuesta a la que se aplica la marca de agua.) Se aplica independientemente de la configuración de capa actual. Ignorado si solo uno de `wid=` y `hei=` se especifica y cuando `fit=constrain` o `fit=stretch`.

## Predeterminado {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, que centra la imagen en el rectángulo de vista.

## Ejemplo {#section-2c9447aa2e184fb8ab1a4370dc61d554}

La siguiente solicitud se ajusta a `myImage` en un rectángulo de vista de 200 x 200 píxeles.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

If `myImage` es exactamente cuadrado, llena todo el rectángulo de vista. If `myImage` tiene una proporción de aspecto vertical, se escala para tener 200 píxeles de altura y se centra horizontalmente en la vista. If `myImage` tiene una proporción de aspecto horizontal, se escala para tener 200 píxeles de ancho y se alinea con el borde superior de la vista. En todos los casos, la imagen devuelta tiene exactamente 200x200 píxeles de tamaño; cualquier espacio no cubierto por la escala `myImage` está lleno de `attribute::BkgColor` (especifique bgc= para controlar el color de fondo de forma dinámica).

## Véase también {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Filigranas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
