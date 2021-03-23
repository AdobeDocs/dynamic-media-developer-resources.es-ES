---
description: Modo de remuestreo. Selecciona el algoritmo de remuestreo o de interpolación que se utilizará para escalar los datos de imagen. También se aplica a la rotación de las capas de texto y al cambio de tamaño de las imágenes compuestas durante la transformación de la vista.
seo-description: Modo de remuestreo. Selecciona el algoritmo de remuestreo o de interpolación que se utilizará para escalar los datos de imagen. También se aplica a la rotación de las capas de texto y al cambio de tamaño de las imágenes compuestas durante la transformación de la vista.
seo-title: resMode
solution: Experience Manager
title: resMode
uuid: 8e12aa06-072c-4e7a-84e6-01437c43c57b
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 15%

---


# resMode{#resmode}

Modo de remuestreo. Selecciona el algoritmo de remuestreo o de interpolación que se utilizará para escalar los datos de imagen. También se aplica a la rotación de las capas de texto y al cambio de tamaño de las imágenes compuestas durante la transformación de la vista.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Selecciona la interpolación bilineal estándar. Método de remuestreo más rápido; pueden verse algunos defectos de solapamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Selecciona la interpolación bicúbica. Mayor densidad de CPU que la interpolación bilineal, pero producirá imágenes más nítidas con menos artefactos de solapamiento visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> agudo2  </span> </p> </td> 
   <td colname="col2"> <p>selecciona una función de ventana Lanczos modificada como un algoritmo de interpolación. Puede producir unos resultados algo más enfocados que la opción bicúbica con un uso mayor de CPU. <span class="codeph"> el punto  </span> ha sido sustituido por el  <span class="codeph"> punto 2  </span>, que tiene menos probabilidades de causar artefactos de aliento (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bici  </span> </p> </td> 
   <td colname="col2"> <p>Selecciona el reampliador predeterminado de Photoshop para reducir el tamaño de la imagen, que en Adobe Photoshop se denomina "nitidez bicúbica". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-a171bacf4ddf43c782e46b86a16d443e}

Atributo de solicitud. Se aplica a todas las operaciones de escalado involucradas en la creación de la imagen de respuesta final, incluido el escalado de todas las capas.

## Predeterminado {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Ejemplo {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Recupere una representación de mejor calidad de una imagen en capas almacenada en un catálogo de imágenes. La imagen puede incluir texto. Esperamos seguir procesando en una aplicación de edición de imágenes y, por lo tanto, solicitar un canal alfa con la imagen.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Véase también {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[atributo::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
