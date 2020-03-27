---
description: Ancho de Vista. Especifica el ancho de la imagen de respuesta (imagen de vista) cuando fit= no está presente en la solicitud.
seo-description: Ancho de Vista. Especifica el ancho de la imagen de respuesta (imagen de vista) cuando fit= no está presente en la solicitud.
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# wid{#wid}

Ancho de Vista. Especifica el ancho de la imagen de respuesta (imagen de vista) cuando fit= no está presente en la solicitud.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Ancho de la imagen en píxeles (int bueno que 0). </p> </td> 
 </tr> 
</table>

Si se especifican `hei=` y `scl=` , la imagen compuesta se puede recortar según el `align=` atributo. Cuando `fit=` está presente, `wid=` especifica el ancho de imagen exacto, mínimo o máximo de respuesta; consulte la descripción de `fit=` para obtener más información.

Si no `scl=` se especifica, la imagen compuesta se redimensiona para ajustarse. Si se especifican `wid=` y `hei=` y no `scl=` se especifica, la imagen se ajusta para ajustarse completamente al rectángulo wid/hei, dejando el área de fondo lo más pequeña posible. En este caso, la imagen se coloca dentro del rectángulo de vista según el `align=` atributo.

>[!NOTE]
>
>Se devuelve un error si el tamaño de la imagen de respuesta predeterminada o calculada es mayor que `attribute::MaxPix`.

## Predeterminado {#section-976d4c8554a34c899f85d172f6ac6f58}

Si no `wid=`se especifica ni `hei=`ni `scl=` , la imagen de respuesta tendrá el tamaño de la imagen compuesta o `attribute::DefaultPix`, el que sea más pequeño.

## Propiedades {#section-c93b7ce1b0d2475f80b06264b45d1285}

atributo de Vista. Se aplica independientemente de la configuración de la capa actual.

## Ejemplo {#section-82bc98b7c15a451bbe9b915d414c0470}

Solicite una imagen para que encaje en un rectángulo de 200 x 200; alinee la imagen arriba a la derecha si no es cuadrada. Cualquier área de fondo se rellena con `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

La misma imagen, que se distribuye con una anchura fija de 200 píxeles, pero con una altura variable para mantener la proporción de aspecto de la imagen. En este caso, la imagen devuelta nunca tiene áreas de relleno de fondo. Tenga en cuenta que en este caso, align= no tendría ningún efecto.

` http:// *`server`*/myRootId/myImageId?wid=200`

## Véase también {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [atributo::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
