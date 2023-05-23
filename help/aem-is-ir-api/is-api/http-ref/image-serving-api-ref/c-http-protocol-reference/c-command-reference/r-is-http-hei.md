---
description: Ver altura. Especifica la altura de la imagen de respuesta (ver imagen) cuando el ajuste no está presente en la solicitud.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 2%

---

# hei{#hei}

Ver altura. Especifica la altura de la imagen de respuesta (ver imagen) cuando el ajuste no está presente en la solicitud.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Alto de la imagen en píxeles (int bueno que 0). </p> </td> 
 </tr> 
</table>

Si ambos `wid=` y `scl=` se especifican, la imagen compuesta se puede recortar según el `align=`atributo. Cuándo `fit=` está presente, `hei=` especifica la altura de imagen de respuesta exacta, mínima o máxima; consulte la descripción de [fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) para obtener más información.

If `scl=` no se ha especificado, la imagen compuesta se escala para ajustarse. Si ambos `wid=` y `hei=` se especifican, y `scl=` Si no se especifica, la imagen se escala para que quepa completamente dentro del rectángulo anchura/altura, dejando tan poca área de fondo expuesta como sea posible; en este caso, la imagen se coloca dentro del rectángulo de vista de acuerdo con la `align=` atributo. El área de fondo está llena de `bgc=`, o, si no se especifica con `attribute::BkgColor`.

>[!NOTE]
>
>Se devuelve un error si el tamaño de la imagen de respuesta calculada es mayor que `attribute::MaxPix`.

## Propiedades {#section-534923644a1e464496eeba83dedcbd3c}

Ver atributo. Se aplica independientemente de la configuración de capa actual.

## Predeterminado {#section-76544d34806d4124a8b173e229cba71f}

Si ninguno `wid=`, `hei=`, ni `scl=` , la imagen de respuesta tendrá el tamaño de la imagen compuesta o `attribute::DefaultPix`, el que sea más pequeño.

## Ejemplos {#section-eb10df7cd67e4733984810aaffd0b9e2}

Solicite que una imagen se ajuste a un rectángulo de 200 x 200; en la parte superior izquierda, alinee la imagen si no es cuadrada. Cualquier área del fondo está llena de `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

La misma imagen, entregada a una altura fija de 200 píxeles, pero con una anchura variable para que coincida con la proporción de aspecto de la imagen. En este caso, la imagen devuelta nunca tendrá áreas de relleno de fondo. Tenga en cuenta que en este caso `align=` no tendría ningún efecto en absoluto.

`http://server/myRootId/myImageId?hei=200`

## Véase también {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
