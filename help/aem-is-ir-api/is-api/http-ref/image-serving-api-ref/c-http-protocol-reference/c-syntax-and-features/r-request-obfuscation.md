---
description: El contenido de toda la parte de modificadores de la cadena de solicitud, incluido el sufijo de bloqueo opcional, puede oscurecerse al aplicar la codificación base64 estándar.
solution: Experience Manager
title: Ofuscación de solicitud
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# Ofuscación de solicitud{#request-obfuscation}

El contenido de toda la parte de modificadores de la cadena de solicitud, incluido el sufijo de bloqueo opcional, puede oscurecerse al aplicar la codificación base64 estándar.

El servidor intenta descodificar si `attribute::RequestObfuscation` está configurado. Si la descodificación falla, se rechaza la solicitud. Si se aplican tanto el bloqueo de solicitud como la ofuscación de solicitud, el sufijo de bloqueo debe generarse y anexarse antes de la codificación base64.

>[!IMPORTANT]
>
>Si habilita esta función, tenga en cuenta que su uso tiene ciertas limitaciones, entre las que se incluyen las siguientes:<br>- Es posible que la interfaz de usuario de Dynamic Media no muestre los detalles correctos para **[!UICONTROL Última publicación]** field. Sin embargo, este efecto no afecta a la publicación.<br>- Actualmente, la transmisión de vídeo HLS no funciona cuando **[!UICONTROL Ofuscación de solicitud]** y **[!UICONTROL Solicitar bloqueo]** están activadas.<br>: Actualmente, algunos visores de Dynamic Media no funcionan cuando **[!UICONTROL Ofuscación de solicitud]** y **[!UICONTROL Solicitar bloqueo]** están activadas.

## Ejemplo {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica en:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Cualquier aparición de &#39;=&#39;, &#39;&amp;&#39; y &#39;%&#39; en cadenas de valor debe evitarse con la codificación &#39;%xx&#39;, antes de que la solicitud se confunda. No es necesario codificar mediante http el *modificadores* forma parte de la solicitud antes o después de la ofuscación, incluso si se aplica el bloqueo de solicitud, ya que la codificación base64 es segura para la transmisión http.

## Véase también {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codificación HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Solicitar bloqueo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
