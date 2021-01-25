---
description: Escala de imagen basada en resolución. Escala la imagen a la resolución solicitada.
seo-description: Escala de imagen basada en resolución. Escala la imagen a la resolución solicitada.
seo-title: res
solution: Experience Manager
title: res
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ab0c8329-5d40-4233-a122-8cb8ca01b500
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# res{#res}

Escala de imagen basada en resolución. Escala la imagen a la resolución solicitada.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>resolución de destinatarios; normalmente en píxeles por pulgada (real). </p> </td> 
 </tr> 
</table>

El factor de escala se calcula dividiendo *`val`* por `catalog::Resolution`. Tenga en cuenta que este comando no afecta a la resolución de impresión de la imagen de respuesta.

Para utilizar esta función, la resolución de las imágenes originales debe conocerse y configurarse en `catalog::Resolution`. Según la aplicación, las unidades de resolución pueden variar. En el caso de las texturas 2D repetibles o muestras de material, como los tapices o telas, la resolución puede expresarse en píxeles/pulgada o en píxeles/mm. Las fotografías y los mapas aéreos pueden estar mejor servidos por píxeles/milla o píxeles/km. En cualquier caso, las unidades utilizadas para `catalog::Resolution` deben ser las mismas que las unidades utilizadas para `res=`.

Además de obtener imágenes con resoluciones precisas, `res=` también se puede utilizar para combinar varias imágenes con la misma resolución, de modo que los elementos visibles en estas imágenes estén en proporción exacta entre sí.

>[!NOTE]
>
>Normalmente, se cambia el tamaño de una imagen compuesta al tamaño de vista de destinatario (especificado por `wid=`, `hei=` o `attribute::DefaultPix`) antes de que se devuelva al cliente. Para evitar este cambio de tamaño y obtener una imagen con la resolución exacta especificada por `res=`, puede ser necesario deshabilitar la escala de vista especificando explícitamente `scl=1`. Esto indica al servidor que recorte la imagen compuesta según el tamaño de vista del destinatario en lugar de escalarla.

## Propiedades {#section-fdbd16e59cff4952a3717146bc91412e}

Atributo de imagen/máscara de origen. Omitido por capas no asociadas con una imagen o máscara de origen. Se aplica a la capa 0 para `layer=comp`. Se omite si se especifica `scale=` o `size=` para la misma capa.

## Predeterminado {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Si no se especifica, `scale=` o `size=` determina el factor de escala o, si no se especifica ninguno, la imagen se utiliza sin escalar.

## Ejemplo {#section-eb06f333e08e4247971fb1b18922597b}

Recupere una imagen de textura con una resolución de objeto de 12 píxeles/pulgada para utilizarla con Representación de imágenes o Creación de imágenes. Especificamos un formato PNG sin pérdida y un remuestreo de mejor calidad para obtener la mejor calidad posible.

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## Véase también {#section-1f8a8f11772e493ca803c4511f397a11}

[catálogo::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ,  [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
