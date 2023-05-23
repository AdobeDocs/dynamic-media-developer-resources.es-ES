---
description: Ver anchura. Especifica la anchura de la imagen de respuesta (ver imagen) cuando fit= no está presente en la solicitud.
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# wid{#wid}

Ver anchura. Especifica la anchura de la imagen de respuesta (ver imagen) cuando fit= no está presente en la solicitud.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Ancho de la imagen en píxeles (int bueno que 0). </p> </td> 
 </tr> 
</table>

Si ambos `hei=` y `scl=` se especifican, la imagen compuesta se puede recortar según el `align=` atributo. Cuándo `fit=` está presente, `wid=` especifica el ancho de imagen de respuesta exacto, mínimo o máximo; consulte la descripción de `fit=` para obtener más información.

If `scl=` no se ha especificado, la imagen compuesta se escala para ajustarse. Si ambos `wid=` y `hei=` se especifican, y `scl=` no se especifica, la imagen se escala para ajustarse por completo al rectángulo wid/hei, dejando el menor área de fondo expuesta como sea posible. En este caso, la imagen se coloca dentro del rectángulo de vista según la variable `align=` atributo.

>[!NOTE]
>
>Se devuelve un error si el tamaño de imagen de respuesta calculado o predeterminado es mayor que `attribute::MaxPix`.

## Predeterminado {#section-976d4c8554a34c899f85d172f6ac6f58}

Si ninguno `wid=`, `hei=`, ni `scl=` se han especificado, la imagen de respuesta tendrá el tamaño de la imagen compuesta o `attribute::DefaultPix`, el que sea más pequeño.

## Propiedades {#section-c93b7ce1b0d2475f80b06264b45d1285}

Ver atributo. Se aplica independientemente de la configuración de capa actual.

## Ejemplo {#section-82bc98b7c15a451bbe9b915d414c0470}

Solicite que una imagen se ajuste a un rectángulo de 200 x 200; alinee la imagen en la parte superior derecha si no es cuadrada. Cualquier área del fondo está llena de `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

La misma imagen, entregada a una anchura fija de 200 píxeles, pero con una altura variable para mantener la proporción de aspecto de la imagen. En este caso, la imagen devuelta nunca tendrá áreas de relleno de fondo. Tenga en cuenta que en este caso align= no tendría ningún efecto.

` http:// *`server`*/myRootId/myImageId?wid=200`

## Véase también {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
