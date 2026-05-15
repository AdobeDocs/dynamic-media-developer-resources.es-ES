---
title: res
description: Escalado de imagen basado en la resolución. Escala la imagen a la resolución solicitada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
TQID: 'https://experienceleague.adobe.com/cvzfgWpPXIxwN0HaehiHOL8vAcfb369UJnC0tVuKFFI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 329
ht-degree: 1%

---

# res{#res}

Escalado de imagen basado en la resolución. Escala la imagen a la resolución solicitada.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Resolución de destino; normalmente en píxeles por pulgada (real). </p> </td> 
 </tr> 
</table>

El factor de escala se calcula dividiendo *`val`* por `catalog::Resolution`. Tenga en cuenta que este comando no afecta a la resolución de impresión de la imagen de respuesta.

Para usar esta característica, la resolución de las imágenes de origen originales debe conocerse y establecerse en `catalog::Resolution`. Dependiendo de la aplicación, las unidades de resolución pueden variar. En el caso de texturas 2D repetibles o muestras de material, como fondos de pantalla o tejidos, la resolución puede expresarse en píxeles/pulgada o píxeles/mm. Las fotos aéreas y los mapas pueden ser mejor servidos por píxeles/milla o píxeles/km. En cualquier caso, las unidades utilizadas para `catalog::Resolution` deben ser las mismas que las utilizadas para `res=`.

Además de obtener imágenes con resoluciones precisas, `res=` también se puede usar para combinar varias imágenes con la misma resolución, de modo que los elementos visibles en estas imágenes estén en proporción precisa entre sí.

>[!NOTE]
>
>Normalmente, se cambia el tamaño de una imagen compuesta al tamaño de vista de destino (especificado por `wid=`, `hei=` o `attribute::DefaultPix`) antes de que se devuelva al cliente. Para evitar este cambio de tamaño y obtener una imagen con la resolución exacta especificada por `res=`, puede ser necesario deshabilitar la escala de vista especificando explícitamente `scl=1`. Esto indica al servidor que recorte la imagen compuesta al tamaño de la vista de destino en lugar de escalarla.

## Propiedades {#section-fdbd16e59cff4952a3717146bc91412e}

Atributo de imagen/máscara de Source. Ignorado por capas no asociadas a una imagen o máscara de origen. Se ha aplicado a la capa 0 para `layer=comp`. Se omite si `scale=` o `size=` se especifican para la misma capa.

## Predeterminado {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Si no se especifica, `scale=` o `size=` determinan el factor de escala o, si no se especifica ninguno, la imagen se utiliza sin escala.

## Ejemplo {#section-eb06f333e08e4247971fb1b18922597b}

Recupere una imagen de textura con una resolución de objeto de 12 píxeles/pulgada para su uso con procesamiento de imágenes o Image Authoring. Especificamos el formato PNG sin pérdidas y un remuestreo de mejor calidad para la mejor calidad posible,

` http:// *`servidor`*/myTexture?res=12&fmt=png&resMode=sharp`

## Véase también {#section-1f8a8f11772e493ca803c4511f397a11}

[catálogo::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
