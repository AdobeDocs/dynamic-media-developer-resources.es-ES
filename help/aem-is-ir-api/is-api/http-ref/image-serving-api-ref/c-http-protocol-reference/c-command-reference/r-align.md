---
description: Alinee la imagen con la vista. Alinea la imagen compuesta (posiblemente después de la escala, si scl= también se especifica) dentro del rectángulo de vista definido por wid= y hei=.
seo-description: Alinee la imagen con la vista. Alinea la imagen compuesta (posiblemente después de la escala, si scl= también se especifica) dentro del rectángulo de vista definido por wid= y hei=.
seo-title: align
solution: Experience Manager
title: align
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---


# align{#align}

Alinee la imagen con la vista. Alinea la imagen compuesta (posiblemente después de la escala, si scl= también se especifica) dentro del rectángulo de vista definido por wid= y hei=.

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

Especifique `align=-1,-1` para alinear la parte superior izquierda de la imagen compuesta con la parte superior izquierda de la vista, especifique `align=1,1` para alinear la parte inferior derecha de la imagen con la parte inferior derecha de la vista. Para las solicitudes estándar de imagen y miniatura, cualquier área de la vista que no esté cubierta por datos de imagen compuesta se rellena con `bgc=`.

## Propiedades {#section-3fbec8206fc944eda4746d8be84f3b41}

Ver atributo. ( `align=` también se utiliza para definir la alineación entre una imagen de marca de agua y la imagen compuesta a la que se aplica la marca de agua). Se aplica independientemente de la configuración de capa actual. Se omite si solo se especifica uno de `wid=` y `hei=` y cuando `fit=constrain` o `fit=stretch`.

## Predeterminado {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, que centra la imagen en el rectángulo de vista.

## Ejemplo {#section-2c9447aa2e184fb8ab1a4370dc61d554}

La siguiente solicitud se ajusta `myImage` a un rectángulo de vista de 200 x 200 píxeles.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Si `myImage` es exactamente cuadrado, rellena el rectángulo de vista completo. Si `myImage` tiene una relación de aspecto vertical, se escala para que tenga 200 píxeles de altura y se centra horizontalmente en la vista. Si `myImage` tiene una relación de aspecto horizontal, se escala a 200 píxeles de ancho y se alinea con el borde superior de la vista. En todos los casos, la imagen devuelta tiene exactamente un tamaño de 200 x 200 píxeles; cualquier espacio que no esté cubierto por el `myImage` escalado se rellena con `attribute::BkgColor` (especifique bgc= para controlar dinámicamente el color de fondo).

## Véase también {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [Marcas de agua](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
