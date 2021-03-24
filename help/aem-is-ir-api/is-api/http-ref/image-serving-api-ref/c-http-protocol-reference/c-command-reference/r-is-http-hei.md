---
description: Ver altura. Especifica el alto de la imagen de respuesta (ver imagen) cuando el ajuste no está presente en la solicitud.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 3%

---


# hei{#hei}

Ver altura. Especifica el alto de la imagen de respuesta (ver imagen) cuando el ajuste no está presente en la solicitud.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Altura de la imagen en píxeles (int bueno a 0). </p> </td> 
 </tr> 
</table>

Si se especifican `wid=` y `scl=`, la imagen compuesta se puede recortar según el atributo `align=`. Cuando `fit=` está presente, `hei=` especifica la altura exacta, mínima o máxima de la imagen de respuesta; consulte la descripción de ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)` para obtener más información.

Si no se especifica `scl=`, la imagen compuesta se escala para ajustarse. Si se especifican `wid=` y `hei=` y no se especifica `scl=`, la imagen se escala para que quepa completamente dentro del rectángulo ancho/largo, dejando tan área de fondo expuesta como sea posible; en este caso, la imagen se coloca dentro del rectángulo de vista según el atributo `align=`. El área de fondo se rellena con `bgc=` o, si no se especifica con `attribute::BkgColor`.

>[!NOTE]
>
>Se devuelve un error si el tamaño calculado de la imagen de respuesta es mayor que `attribute::MaxPix`.

## Propiedades {#section-534923644a1e464496eeba83dedcbd3c}

Ver atributo. Se aplica independientemente de la configuración de capa actual.

## Predeterminado {#section-76544d34806d4124a8b173e229cba71f}

Si no se especifican `wid=`, `hei=` ni `scl=`, la imagen de respuesta tiene el tamaño de la imagen compuesta o `attribute::DefaultPix`, el que sea más pequeño.

## Ejemplos {#section-eb10df7cd67e4733984810aaffd0b9e2}

Solicite una imagen para que se ajuste a un rectángulo de 200 x 200; alinee la imagen en la parte superior izquierda si no es cuadrada. Cualquier área de fondo se rellena con `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

La misma imagen, entregada a una altura fija de 200 píxeles, pero con una anchura variable para coincidir con la proporción de aspecto de la imagen. En este caso, la imagen devuelta nunca tiene áreas de relleno de fondo. Tenga en cuenta que en este caso `align=` no tendría ningún efecto.

`http://server/myRootId/myImageId?hei=200`

## Véase también {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f),  [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [atributo::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
