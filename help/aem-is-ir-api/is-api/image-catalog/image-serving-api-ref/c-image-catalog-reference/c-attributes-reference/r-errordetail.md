---
description: Detalle del mensaje de error. Especifica el nivel de detalle de los mensajes de error devueltos por HTTP como valor error.message.
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
TQID: 'https://experienceleague.adobe.com/CZ2k-H1kZI3t3ZAtgm7qj8eo97u4NPmumdErNU--uvU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 4%

---

# ErrorDetail{#errordetail}

Detalle del mensaje de error. Especifica el nivel de detalle de los mensajes de error devueltos por HTTP como valor error.message.

Se permiten los siguientes valores:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Solo título. Devuelve una breve descripción general del error. Recomendado para servidores activos a los que se puede acceder públicamente. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Mensaje breve. Reservado para uso futuro. Actualmente devuelve la misma información que 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Mensaje detallado. Proporciona detalles a nivel de usuario sobre el error. Puede incluir información confidencial, como rutas de archivo. Recomendado para servidores de ensayo, control de calidad y desarrollo de aplicaciones. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Información de depuración completa. Agrega seguimientos de pila Java cuando corresponde. Las imágenes de error nunca incluyen seguimientos de pila y, en su lugar, devuelven información de nivel 2 en <span class="codeph"> $error.message</span>. Esta información puede resultar útil cuando se notifican problemas al soporte técnico de Dynamic Media. </p></td> 
 </tr> 
</table>

## Propiedades {#section-e167895723ca4ad4ba283d3d7b4324de}

El valor enumerado debe ser 0, 1, 2 o 3.

## Predeterminado {#section-8f27098e509945a18676aca0675c8f41}

Se hereda de `default::ErrorDetail` si no se especifica o si está vacío.

## Véase también {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
