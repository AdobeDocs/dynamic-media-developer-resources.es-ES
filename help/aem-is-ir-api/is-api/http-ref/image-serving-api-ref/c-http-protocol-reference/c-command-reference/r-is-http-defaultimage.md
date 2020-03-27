---
description: Imagen de respuesta predeterminada. Especifica la imagen o entrada de catálogo que se utilizará cuando no se encuentre una imagen.
seo-description: Imagen de respuesta predeterminada. Especifica la imagen o entrada de catálogo que se utilizará cuando no se encuentre una imagen.
seo-title: defaultImage
solution: Experience Manager
title: defaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 7478325c-9ac5-4b85-a4c5-5c495f924eb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# defaultImage{#defaultimage}

Imagen de respuesta predeterminada. Especifica la imagen o entrada de catálogo que se utilizará cuando no se encuentre una imagen.

` defaultImage= *`objeto`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> , objeto </span></span> </p> </td> 
  <td class="stentry"> <p>Objeto de imagen. </p> </td> 
 </tr> 
</table>

*`object`* puede ser una entrada de catálogo (incluida una plantilla) o una ruta de archivo de imagen simple. Resulta útil para sustituir las imágenes que faltan por las imágenes predeterminadas. Este valor anula el valor del catálogo correspondiente `attribute::DefaultImage`. Un valor vacío ( `defaultImage=`) desactiva la administración de imágenes predeterminada.

>[!NOTE]
>
>El mecanismo de imagen predeterminado no se aplica a los objetos SVG. Se devuelve un error si no se encuentra el objeto SVG especificado en la solicitud.

Si `attribute::DefaultImageMode=0`, *`object`* reemplaza toda la solicitud original, aunque falte una sola imagen en una composición de varias imágenes. Los únicos comandos retenidos de la solicitud original son: `wid=`, `hei=`, `fmt=`, `qlt=`.

Si `attribute::DefaultImageMode=1`, el objeto reemplaza solo la imagen de capa que falta; los atributos de la capa que falta se aplican y el compuesto se procesa y devuelve como de costumbre.

## Propiedades {#section-d30923d8dc4042eba10989212dd70887}

Solicitar atributo. Se aplica independientemente de la configuración de la capa actual. Se omite si `req=` es distinto de `img` o `tmb`.

## Restrictions {#section-30df31bc8cac41cd917f1e45196779c2}

Las fuentes de imagen extranjeras no están cubiertas por el mecanismo de imagen predeterminado; se devuelve un error si un origen de imagen externo no es válido.

El servicio de imágenes vuelve a estar disponible `DefaultImageMode=0` cuando fallan las solicitudes de procesamiento de imágenes anidadas o FXG.

## Predeterminado {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Véase también {#section-745392143c3747a2955e1ae561f58e5f}

[atributo::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [atributo: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
