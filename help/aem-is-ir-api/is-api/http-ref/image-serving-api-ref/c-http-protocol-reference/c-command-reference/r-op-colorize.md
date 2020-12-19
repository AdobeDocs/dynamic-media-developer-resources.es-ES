---
description: Colorear imagen. Coloriza los datos de la imagen conservando las sombras y los resaltados.
seo-description: Colorear imagen. Coloriza los datos de la imagen conservando las sombras y los resaltados.
seo-title: op_colorize
solution: Experience Manager
title: op_colorize
topic: Scene7 Image Serving - Image Rendering API
uuid: e74a85ca-73bf-4c69-ac77-768a58b33d0b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 4%

---


# op_colorize{#op-colorize}

Colorear imagen. Coloriza los datos de la imagen conservando las sombras y los resaltados.

` op_colorize= *``*[,off|norm[, *`color-contraste`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Color RGB de sustitución. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> apagado </span> </p> </td> 
  <td class="stentry"> <p>Desactive la compensación automática del brillo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm  </span> </p> </td> 
  <td class="stentry"> <p>Activar compensación de brillo automática (predeterminada). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contrastar </span> </p> </td> 
  <td class="stentry"> <p>Intervalo de contraste (0,100 real); definido en 0 para conservar el contraste de entrada. </p> </td> 
 </tr> 
</table>

El segundo argumento especifica si se debe ajustar el brillo de la imagen de origen antes de colorear. Especifique `off` para deshabilitar la compensación automática del brillo o `norm` para ajustar el brillo automáticamente de modo que el valor medio sea de una intensidad del 50%.

Establezca el valor *`contrast`* en 0 para conservar el rango de contraste de la imagen de entrada o especifique un rango de contraste deseado con un valor bueno a 0. Un valor de 100 maximiza el contraste. Los valores típicos pueden estar entre 30 y 70.

Además de los ajustes de brillo y contraste integrados, se pueden utilizar `op_brightness=` y `op_contrast=` para afinar aún más el efecto de coloreado.

>[!NOTE]
>
>El algoritmo de coloreado solo utiliza la información de luminancia de los datos de la imagen. Esta conversión a escala de grises es sencilla y no se gestiona con colores. `op_colorize` siempre genera datos RGB, aunque la entrada sea en escala de grises o CMYK.

## Propiedades {#section-c0f8bd424b864153a1108f384939f55b}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Omitido por capas de efectos.

*`color`* debe ser un valor RGB; no se admiten  *`color`* los valores gris o CMYK.

El valor *`contrast`* se ignora si se desactiva la compensación de brillo.

*`color`* se supone que existe en el espacio de color de trabajo correspondiente al tipo de píxel de  *`color`*. *`color`* se convierte con precisión si la imagen de capa tiene un tipo de píxel diferente en el momento de la combinación.

Las imágenes CMYK se convierten a RGB antes de que se aplique la operación.

## Predeterminado {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, sin colorización. El segundo y el tercer argumentos toman el valor predeterminado `norm,0` para la compensación automática del brillo y ningún cambio de contraste.

## Ejemplo {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Ajuste el brillo y el contraste de forma dinámica antes de colorear una capa de imagen:

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

Utilice el ajuste automático de brillo y contraste en su lugar:

... `&op_colorize=a0b0c0,norm,50&`...

## Véase también {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [op_brillo=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a),  [op_contraste=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), Administración  [de color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
