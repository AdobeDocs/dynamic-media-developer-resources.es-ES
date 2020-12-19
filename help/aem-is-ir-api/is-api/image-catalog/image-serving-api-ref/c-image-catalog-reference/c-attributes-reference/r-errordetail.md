---
description: Detalles del mensaje de error. Especifica el nivel de detalle de los mensajes de error devueltos mediante HTTP como valor de error.message.
seo-description: Detalles del mensaje de error. Especifica el nivel de detalle de los mensajes de error devueltos mediante HTTP como valor de error.message.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Scene7 Image Serving - Image Rendering API
uuid: 46ebb8c7-930e-4844-8664-ec6a63691523
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 4%

---


# ErrorDetail{#errordetail}

Detalles del mensaje de error. Especifica el nivel de detalle de los mensajes de error devueltos mediante HTTP como valor de error.message.

Se permiten los siguientes valores:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Solo título. Devuelve una breve descripción general del error. Recomendado para servidores activos a los que se puede acceder públicamente. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Breve mensaje. Reservado para uso futuro. Actualmente devuelve la misma información que 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Mensaje detallado. Proporciona detalles de nivel de usuario sobre el error. Puede incluir información confidencial, como rutas de archivos. Recomendado para servidores de ensayo, garantía de calidad y desarrollo de aplicaciones. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Información de depuración completa. Añade los seguimientos de pila Java cuando corresponde. Las imágenes de error nunca incluyen trazos de pila y, en su lugar, devuelven información de nivel 2 en <span class="codeph"> $error.message</span>. Esta información puede resultar útil cuando se producen problemas de sistema de informes en la asistencia técnica de Scene7. </p></td> 
 </tr> 
</table>

## Propiedades {#section-e167895723ca4ad4ba283d3d7b4324de}

El valor enumerado debe ser 0, 1, 2 o 3.

## Predeterminado {#section-8f27098e509945a18676aca0675c8f41}

Se hereda de `default::ErrorDetail` si no se especifica o si está vacío.

## Véase también {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
