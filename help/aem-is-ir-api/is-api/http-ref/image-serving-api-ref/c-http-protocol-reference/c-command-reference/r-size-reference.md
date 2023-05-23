---
description: Tamaño de capa. Especifica el tamaño o el tamaño máximo de capa de una capa, antes de aplicar rotate=, perspectiva= y extend= a la capa.
solution: Experience Manager
title: tamaño
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# tamaño{#size}

Tamaño de capa. Especifica el tamaño o el tamaño máximo de capa de una capa, antes de aplicar rotate=, perspectiva= y extend= a la capa.

` size= *`anchura`*, *`altura`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> anchura </span>, <span class="varname"> altura </span> </span> </p> </td> 
  <td class="stentry"> <p>Restricción de tamaño de capa en píxeles (int, int, 0 o bueno). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>Restricción de tamaño de capa normalizada en relación con el tamaño de capa 0 (real, real, 0,0...1,0). </p> </td> 
 </tr> 
</table>

Cuando se especifica para una capa de imagen, size= limita la anchura, la altura o ambas cosas de la imagen de capa. La imagen se escala para que no sea mayor que `size=`. Si se especifica un tamaño normalizado, es relativo al tamaño de la capa 0. Si ambos *`width`* y *`height`* se especifican, la imagen de origen se escala (tras `crop=` se aplica) para que ninguna dimensión supere el tamaño especificado. La proporción de aspecto del rectángulo de origen se mantiene en todos los casos. Cualquiera *`width`* o *`height`* puede establecerse en 0; en este caso, el servidor calcula el valor en función de la proporción de aspecto de la imagen.

Cuando se especifica para una capa de texto, `size=` especifica el tamaño del cuadro de texto. *`width`* es obligatorio; *`height`* puede establecerse en 0, en cuyo caso se utiliza la altura del texto diseñado como altura de la capa. De forma predeterminada, los motores de diseño de texto insertan saltos de línea para garantizar que el texto siempre se ajuste horizontalmente al espacio disponible. If *`height`* se especifica, las líneas que no caben en el espacio disponible se recortan ( `text=`) u omitido ( `textPs=`). `text=` admite modos de ajuste adicionales; consulte `textAttr=` para obtener más información.

Cuando se especifica para una capa de color sólido, `size=` define el tamaño exacto de la capa; se deben especificar ambos valores (a menos que se proporcione una máscara). If `mask=` también se especifica, el tamaño de la imagen de la máscara es el adecuado `size=` del mismo modo que las imágenes se escalan en las capas de imagen.

## Propiedades {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Atributo de capa. Se aplica a la capa 0 si `layer=comp`. `sizeN=` no está permitido para `layer=0` o `layer=comp`. `sizeN=` está permitido para `layer=0` y `layer=comp` solo en registros de catálogo que definen imágenes de marca de agua. En este caso, `sizeN` define la escala de la imagen de marca de agua en relación con la imagen compuesta a la que se aplica la marca de agua. If `size=` se ha especificado, `res=` y `scale=` se ignoran para esta capa. Ignorado por las capas de efecto.

## Predeterminado {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`Sin embargo, el tamaño de la capa no está restringido. Para las capas de imagen, el tamaño de la capa se determina en función del tamaño de la imagen de la capa después de cualquier `crop=`, `scale=`, o `res=` se han aplicado las operaciones. Para capas de texto, si `size=` no se ha especificado, el tamaño de la capa se ajusta automáticamente al texto procesado.

Las capas de color sólido requieren una especificación completa `size=`, a `mask=`, o `clipPath=`.

## Ejemplo {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Consulte [Ejemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Véase también {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Capas de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
