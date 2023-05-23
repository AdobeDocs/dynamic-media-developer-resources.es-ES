---
title: resMode
description: Modo de remuestreo. Elige el algoritmo de remuestreo o interpolación que se utilizará para escalar los datos de imagen. También se aplica a la rotación de capas de texto y al cambio de tamaño de imágenes compuestas durante la transformación de la vista.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# resMode{#resmode}

Modo de remuestreo. Elige el algoritmo de remuestreo o interpolación que se utilizará para escalar los datos de imagen. También se aplica a la rotación de capas de texto y al cambio de tamaño de imágenes compuestas durante la transformación de la vista.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Selecciona la interpolación bilineal estándar. Método de remuestreo más rápido; pueden verse algunos defectos de solapamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Selecciona la interpolación bicúbica. Requiere más CPU que la interpolación bilineal, pero genera imágenes más nítidas con defectos de solapamiento menos evidentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>selecciona una función de ventana Lanczos modificada como un algoritmo de interpolación. Puede producir resultados ligeramente más nítidos que los bicúbicos a un mayor coste de CPU. <span class="codeph"> afilado </span> se ha reemplazado por <span class="codeph"> sharp2 </span>, que tiene una menor probabilidad de causar artefactos de solapamiento (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Selecciona el remuestreador predeterminado de Photoshop para reducir el tamaño de la imagen, que se denomina "enfoque bicúbico" en Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Para mantener la proporción de aspecto de una imagen cuando se utilizan ambos `resMode=bisharp` y `fit=stretch`Sin embargo, se recomienda utilizar el parámetro width o el parámetro height. Si se deben definir ambos parámetros, se pueden envolver en una capa diferente como se muestra en el siguiente ejemplo:
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Propiedades {#section-a171bacf4ddf43c782e46b86a16d443e}

Atributo de solicitud. Se aplica a todas las operaciones de escalado implicadas en la creación de la imagen de respuesta final, incluido el escalado de todas las capas.

## Predeterminado {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Ejemplo {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Recupere una representación de la mejor calidad de una imagen con capas almacenada en un catálogo de imágenes. La imagen puede incluir texto. La imagen se procesa posteriormente en una aplicación de edición de imágenes y, por lo tanto, se solicita un canal alfa con la imagen.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Véase también {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
