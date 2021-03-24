---
description: Colorice la imagen. Coloriza los datos de la imagen preservando sombras y resaltados.
solution: Experience Manager
title: op_colorize
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 4%

---


# op_colorize{#op-colorize}

Colorice la imagen. Coloriza los datos de la imagen preservando sombras y resaltados.

` op_colorize= *``*[,off|norm[, *`colorcontrast`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Color RGB de reemplazo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> apagado </span> </p> </td> 
  <td class="stentry"> <p>Desactive la compensación automática del brillo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm  </span> </p> </td> 
  <td class="stentry"> <p>Habilite la compensación de brillo automática (predeterminada). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contrastar </span> </p> </td> 
  <td class="stentry"> <p>Intervalo de contraste (real 0.1.100); configurado en 0 para conservar el contraste de entrada. </p> </td> 
 </tr> 
</table>

El segundo argumento especifica si el brillo de la imagen de origen debe ajustarse antes de colorear. Especifique `off` para deshabilitar la compensación automática de brillo o `norm` para ajustar el brillo automáticamente de modo que la mediana del valor sea del 50% de intensidad.

Establezca el valor *`contrast`* en 0 para conservar el intervalo de contraste de la imagen de entrada o especifique un intervalo de contraste deseado con un valor bueno a 0. Un valor de 100 maximiza el contraste. Los valores típicos pueden estar entre 30 y 70.

Además de los ajustes integrados de brillo y contraste, se pueden utilizar `op_brightness=` y `op_contrast=` para ajustar aún más el efecto colorante.

>[!NOTE]
>
>El algoritmo de coloreado utiliza solamente la información de luminancia en los datos de la imagen. Esta conversión a escala de grises es sencilla y no se administra con el color. `op_colorize` siempre genera datos RGB, incluso si la entrada es escala de grises o CMYK.

## Propiedades {#section-c0f8bd424b864153a1108f384939f55b}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por capas de efecto.

*`color`* debe ser un valor RGB; no se admiten  *`color`* valores grises o CMYK.

El valor *`contrast`* se ignora si se desactiva la compensación de brillo.

*`color`* se supone que existe en el espacio de color de trabajo correspondiente al tipo de píxel de  *`color`*. *`color`* se convierte con precisión si la imagen de capa tiene un tipo de píxel diferente en el momento de la fusión.

Las imágenes CMYK se convierten a RGB antes de aplicar la operación.

## Predeterminado {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, para no colorear. El segundo y tercer argumentos tienen el valor predeterminado `norm,0`, para obtener una compensación automática del brillo y sin ningún cambio de contraste.

## Ejemplo {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Ajuste el brillo y el contraste de forma dinámica antes de colorear una capa de imagen:

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

Utilice el ajuste automático de brillo y contraste:

... `&op_colorize=a0b0c0,norm,50&`...

## Véase también {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [op_bright=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a),  [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), Gestión de  [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
