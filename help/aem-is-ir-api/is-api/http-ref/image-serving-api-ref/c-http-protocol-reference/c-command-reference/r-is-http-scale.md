---
description: Escalar imagen. Escala una imagen de origen de capa por factor en relación con la imagen de resolución completa.
seo-description: Escalar imagen. Escala una imagen de origen de capa por factor en relación con la imagen de resolución completa.
seo-title: scale
solution: Experience Manager
title: scale
topic: Scene7 Image Serving - Image Rendering API
uuid: f5540df8-60d9-4efc-99fe-733cdc8268ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scale{#scale}

Escalar imagen. Escala una imagen de origen de capa por factor en relación con la imagen de resolución completa.

`scale= *`factor`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> factor</span> </p> </td> 
  <td class="stentry"> <p>Factor de escala (real, bueno que 0,0). </p></td> 
 </tr> 
</table>

No se aplica ninguna escala cuando `scale=1`. *`factor`* menor que 1,0 reduce la escala y mayor que 1,0 amplía la imagen de origen.

## Propiedades {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Atributo de imagen/máscara de origen. Se omite si `size=` se especifica también para la capa actual. Overrides `res=`. Se aplica a la capa 0 si se especifica para `layer=comp`. Se omite si la capa no está asociada a una imagen o máscara.

## Predeterminado {#section-26e64904362342a5a62c5f6598f330c4}

Si no se especifica, `res=` se utiliza. Si no `res=` se especifica, la imagen se utiliza sin escalar.

## Véase también {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
