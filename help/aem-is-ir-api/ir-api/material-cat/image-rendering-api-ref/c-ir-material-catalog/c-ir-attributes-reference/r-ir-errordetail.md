---
title: ErrorDetail
description: Detalle del mensaje de error. Especifica el nivel de detalle de los mensajes de error devueltos por HTTP como valor error.message.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 4%

---

# ErrorDetail{#errordetail}

Detalle del mensaje de error. Especifica el nivel de detalle de los mensajes de error devueltos por HTTP como valor error.message.

## Título {#section-c10d75d72ee24d16a67cc8d927f1deba}

Se permiten los siguientes valores:

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Solo título. Devuelve una breve descripción general del error. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Mensaje breve. Reservado para uso futuro. Actualmente devuelve la misma información que 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Mensaje detallado. Proporciona detalles a nivel de usuario sobre el error. Puede incluir información confidencial, como rutas de archivo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Información de depuración completa. Agrega seguimientos de pila de Java™ cuando corresponde. Las imágenes de error nunca incluyen seguimientos de pila y, en su lugar, devuelven información de nivel 2 en <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* Se recomienda el nivel 0 para servidores activos a los que se puede acceder públicamente.
* Se recomienda el nivel 2 para los servidores de ensayo, garantía de calidad y desarrollo de aplicaciones.
* La información del nivel 3 puede resultar útil cuando se informa de problemas al servicio de asistencia técnica de Dynamic Media.

## Propiedades {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

El valor enumerado debe ser 0, 1, 2 o 3.

## Predeterminado {#section-5e78d550050840cc9a1de811c581b94f}

Se hereda de `default::ErrorDetail` si no se especifica o si está vacío.

## Véase también {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
