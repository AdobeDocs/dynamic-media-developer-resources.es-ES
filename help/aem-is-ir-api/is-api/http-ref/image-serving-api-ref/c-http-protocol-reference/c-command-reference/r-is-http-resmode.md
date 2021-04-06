---
description: Modo de remuestreo. Selecciona el algoritmo de remuestreo o de interpolación que se utilizará para escalar los datos de imagen. También se aplica a la rotación de las capas de texto y al cambio de tamaño de las imágenes compuestas durante la transformación de la vista.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
translation-type: tm+mt
source-git-commit: b08d1f5b0aa512be4a6e6a4d45d8d4dec15ca1db
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 6%

---

# resMode{#resmode}

Modo de remuestreo. Selecciona el algoritmo de remuestreo o de interpolación que se utilizará para escalar los datos de imagen. También se aplica a la rotación de las capas de texto y al cambio de tamaño de las imágenes compuestas durante la transformación de la vista.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Selecciona la interpolación bilineal estándar. Método de remuestreo más rápido; se pueden apreciar algunos artefactos de aliasing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Selecciona la interpolación bicúbica. Mayor uso intensivo de CPU que la interpolación bilineal, pero produce imágenes más nítidas con artefactos de aliasing menos visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> agudo2  </span> </p> </td> 
   <td colname="col2"> <p>selecciona una función de ventana Lanczos modificada como un algoritmo de interpolación. Puede producir resultados ligeramente más nítidos que los bicúbicos a un mayor costo de CPU. <span class="codeph"> el punto  </span> ha sido sustituido por el  <span class="codeph"> punto 2  </span>, que tiene menos probabilidades de causar artefactos de aliento (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bici  </span> </p> </td> 
   <td colname="col2"> <p>Selecciona el reampliador predeterminado de Photoshop para reducir el tamaño de la imagen, que en Adobe Photoshop se denomina "nitidez bicúbica". </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Para mantener la relación de aspecto de una imagen al utilizar `resMode=bisharp` y `fit=stretch`, se recomienda utilizar el parámetro de anchura o el parámetro de altura. Si se deben definir ambos parámetros, se pueden envolver en una capa diferente, como se muestra en el siguiente ejemplo:
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Propiedades {#section-a171bacf4ddf43c782e46b86a16d443e}

Atributo de solicitud. Se aplica a todas las operaciones de escalado involucradas en la creación de la imagen de respuesta final, incluido el escalado de todas las capas.

## Predeterminado {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Ejemplo {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Recupere una representación de mejor calidad de una imagen en capas almacenada en un catálogo de imágenes. La imagen puede incluir texto. La imagen se seguirá procesando en una aplicación de edición de imágenes y, por lo tanto, se solicitará un canal alfa con la imagen.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Véase también {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[atributo::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
