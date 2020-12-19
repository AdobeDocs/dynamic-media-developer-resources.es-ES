---
description: Alinear imagen con Vista. Alinea la imagen compuesta (posiblemente después de escalar, si también se ha especificado scl=) dentro del rectángulo de vista definido por wid= y hei=.
seo-description: Alinear imagen con Vista. Alinea la imagen compuesta (posiblemente después de escalar, si también se ha especificado scl=) dentro del rectángulo de vista definido por wid= y hei=.
seo-title: align
solution: Experience Manager
title: align
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 1%

---


# align{#align}

Alinear imagen con Vista. Alinea la imagen compuesta (posiblemente después de escalar, si también se ha especificado scl=) dentro del rectángulo de vista definido por wid= y hei=.

` align= *``*, *`horizvert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz  </span> </span> </p> </td> 
  <td class="stentry"> <p>alineación horizontal (real, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert  </span> </span> </p> </td> 
  <td class="stentry"> <p>alineación vertical (real, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Especifique `align=-1,-1` para alinear la parte superior izquierda de la imagen compuesta con la parte superior izquierda de la vista, especifique `align=1,1` para alinear la parte inferior derecha de la imagen con la parte inferior derecha de la vista. Para solicitudes de imagen estándar y miniaturas, cualquier área de la vista que no esté cubierta por datos de imagen compuesta se rellena con `bgc=`.

## Propiedades {#section-3fbec8206fc944eda4746d8be84f3b41}

atributo de vista. ( `align=` también se utiliza para definir la alineación entre una imagen de marca de agua y la imagen compuesta a la que se aplica la marca de agua). Se aplica independientemente de la configuración de la capa actual. Se omite si sólo se especifica uno de `wid=` y `hei=` y cuando `fit=constrain` o `fit=stretch`.

## Predeterminado {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, que centra la imagen en el rectángulo de vista.

## Ejemplo {#section-2c9447aa2e184fb8ab1a4370dc61d554}

La siguiente solicitud se ajusta `myImage` a un rectángulo de vista de 200 x 200 píxeles.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Si `myImage` es exactamente cuadrado, rellena todo el rectángulo de vista. Si `myImage` tiene una proporción de aspecto vertical, se aplica una escala de 200 píxeles de altura y se centra horizontalmente en la vista. Si `myImage` tiene una proporción de aspecto horizontal, se escala a 200 píxeles de ancho y se alinea con el borde superior de la vista. En todos los casos, la imagen devuelta tiene exactamente un tamaño de 200 x 200 píxeles; cualquier espacio no cubierto por el `myImage` escalado se rellena con `attribute::BkgColor` (especifique bgc= para controlar el color de fondo dinámicamente).

## Véase también {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [Watermarks](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
