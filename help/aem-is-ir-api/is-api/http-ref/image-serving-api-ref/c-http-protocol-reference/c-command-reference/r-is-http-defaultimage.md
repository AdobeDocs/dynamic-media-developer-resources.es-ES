---
title: defaultImage
description: Imagen de respuesta predeterminada. Especifica la imagen o la entrada de catálogo que se utilizará cuando no se encuentre una imagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---

# defaultImage{#defaultimage}

Imagen de respuesta predeterminada. Especifica la imagen o la entrada de catálogo que se utilizará cuando no se encuentre una imagen.

` defaultImage= *`objeto`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objeto </span> </span> </p> </td> 
  <td class="stentry"> <p>Objeto de imagen. </p> </td> 
 </tr> 
</table>

*`object`* puede ser una entrada de catálogo (incluida una plantilla) o una ruta de archivo de imagen simple. Útil para sustituir imágenes que faltan por imágenes predeterminadas. Este valor anula el valor del catálogo correspondiente `attribute::DefaultImage`. Un valor vacío (`defaultImage=`) deshabilita la administración predeterminada de imágenes.

>[!NOTE]
>
>El mecanismo de imagen predeterminado no se aplica a los objetos del SVG. Se devuelve un error si no se encuentra el objeto SVG especificado en la solicitud.

Si `attribute::DefaultImageMode=0`, *`object`* reemplaza toda la solicitud original, aunque solo falte una imagen en la composición de varias imágenes. Los únicos comandos retenidos de la solicitud original son: `wid=`, `hei=`, `fmt=`, `qlt=`.

Si `attribute::DefaultImageMode=1`, el objeto reemplaza solamente la imagen de capa que falta; los atributos de la capa que falta se aplican y el compuesto se procesa y se devuelve como de costumbre.

## Propiedades {#section-d30923d8dc4042eba10989212dd70887}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Se ignora si `req=` es distinto de `img` o `tmb`.

## Restricciones {#section-30df31bc8cac41cd917f1e45196779c2}

El mecanismo de imagen predeterminado no cubre los orígenes de imagen externos; se devuelve un error si un origen de imagen externo no es válido.

El servicio de imágenes vuelve a `DefaultImageMode=0` cuando las solicitudes de procesamiento FXG o de procesamiento de imágenes anidadas fallan.

## Predeterminado {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Véase también {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [attribute:: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
