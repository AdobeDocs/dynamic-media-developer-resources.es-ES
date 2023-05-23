---
description: Colorear imagen. Colorea los datos de la imagen conservando las sombras y los resaltados.
solution: Experience Manager
title: op_colorize
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 4%

---

# op_colorize{#op-colorize}

Colorear imagen. Colorea los datos de la imagen conservando las sombras y los resaltados.

` op_colorize= *`color`*[,off|norm[, *`contrastar`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Color de RGB de repuesto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> apagado </span> </p> </td> 
  <td class="stentry"> <p>Desactive la compensación automática de brillo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norma </span> </p> </td> 
  <td class="stentry"> <p>Habilitar la compensación automática de brillo (predeterminada). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contrastar </span> </p> </td> 
  <td class="stentry"> <p>Rango de contraste (real 0..100); establezca en 0 para conservar el contraste de entrada. </p> </td> 
 </tr> 
</table>

El segundo argumento especifica si el brillo de la imagen de origen debe ajustarse antes de colorear. Especificar `off` para desactivar la compensación automática de brillo o `norm` ajustar el brillo automáticamente para que el valor de la mediana tenga una intensidad del 50%.

Configure las variables *`contrast`* valor 0 para conservar el intervalo de contraste de la imagen de entrada o especifique un intervalo de contraste deseado con un valor bueno a 0. Un valor de 100 maximiza el contraste. Los valores habituales pueden estar entre 30 y 70.

Además de los ajustes integrados de brillo y contraste, `op_brightness=` y `op_contrast=` puede utilizarse para ajustar aún más el efecto colorante.

>[!NOTE]
>
>El algoritmo de coloreado utiliza sólo la información de luminancia de los datos de la imagen. Esta conversión a escala de grises es sencilla y no se administra por colores. `op_colorize` siempre genera datos de RGB, incluso si la entrada es de escala de grises o CMYK.

## Propiedades {#section-c0f8bd424b864153a1108f384939f55b}

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por las capas de efecto.

*`color`* debe ser un valor de RGB; gris o CMYK *`color`* no se admiten valores de.

El *`contrast`* se ignora si la compensación de brillo está desactivada.

*`color`* se supone que existe en el espacio de color de trabajo correspondiente al tipo de píxel de *`color`*. *`color`* se convierte con precisión si la imagen de capa tiene un tipo de píxel diferente en el momento de la combinación.

Las imágenes CMYK se convierten en RGB antes de que se aplique la operación.

## Predeterminado {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, para que no haya coloreado. El segundo y tercer argumentos tienen el valor predeterminado `norm,0`, para la compensación automática del brillo y sin cambio de contraste.

## Ejemplo {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Ajuste dinámico del brillo y el contraste antes de colorear una capa de imagen:

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

En su lugar, utilice un ajuste automático de brillo y contraste:

… `&op_colorize=a0b0c0,norm,50&`…

## Véase también {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_bright=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Gestión de color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
