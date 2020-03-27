---
description: Detalles del mensaje de error. Especifica el nivel de detalle de los mensajes de error devueltos mediante HTTP como valor de error.message.
seo-description: Detalles del mensaje de error. Especifica el nivel de detalle de los mensajes de error devueltos mediante HTTP como valor de error.message.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Scene7 Image Serving - Image Rendering API
uuid: aab11640-95d7-427d-b79f-c477b2c9047e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ErrorDetail{#errordetail}

Detalles del mensaje de error. Especifica el nivel de detalle de los mensajes de error devueltos mediante HTTP como valor de error.message.

## Título {#section-c10d75d72ee24d16a67cc8d927f1deba}

Se permiten los siguientes valores:

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Solo título. Devuelve una breve descripción general del error. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Breve mensaje. Reservado para uso futuro. Actualmente devuelve la misma información que 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Mensaje detallado. Proporciona detalles de nivel de usuario sobre el error. Puede incluir información confidencial, como rutas de archivos. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Información de depuración completa. Añade los seguimientos de pila Java cuando corresponde. Las imágenes de error nunca incluyen trazos de pila y, en su lugar, devuelven información de nivel 2 en <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* Se recomienda el nivel 0 para los servidores activos a los que se puede acceder públicamente.
* Se recomienda el nivel 2 para servidores de ensayo, garantía de calidad y desarrollo de aplicaciones.
* La información de nivel 3 puede resultar útil cuando se producen problemas de sistema de informes a la asistencia técnica de Scene7.

## Propiedades {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

El valor enumerado debe ser 0, 1, 2 o 3.

## Predeterminado {#section-5e78d550050840cc9a1de811c581b94f}

Se hereda de `default::ErrorDetail` si no se especifica o si está vacío.

## Véase también {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
