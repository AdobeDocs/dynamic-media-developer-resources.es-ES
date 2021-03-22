---
description: El contenido de toda la parte modificadora de la cadena de solicitud, incluido el sufijo de bloqueo opcional, puede oscurecerse aplicando la codificación base64 estándar.
seo-description: El contenido de toda la parte modificadora de la cadena de solicitud, incluido el sufijo de bloqueo opcional, puede oscurecerse aplicando la codificación base64 estándar.
seo-title: Confusión de solicitudes
solution: Experience Manager
title: Confusión de solicitudes
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# Confusión de solicitud{#request-obfuscation}

El contenido de toda la parte modificadora de la cadena de solicitud, incluido el sufijo de bloqueo opcional, puede oscurecerse aplicando la codificación base64 estándar.

El servidor intenta descodificar si `attribute::RequestObfuscation` está establecido. Si la descodificación falla, se rechaza la solicitud. Si se aplican tanto el bloqueo de solicitud como la ofuscación de solicitud, el sufijo de bloqueo debe generarse y añadirse antes de la codificación base64.

>[!IMPORTANT]
>
>Si habilita esta función, tenga en cuenta que existen ciertas limitaciones en su uso que incluyen lo siguiente:<br>- Es posible que la interfaz de usuario de Dynamic Media no muestre los detalles correctos para el campo **[!UICONTROL Última publicación]**. Sin embargo, este efecto no afecta a la publicación.<br>- Actualmente, el flujo de vídeo HLS no funciona cuando se activan la **[!UICONTROL ofuscación de]** solicitudes y el  **[!UICONTROL bloqueo de]** solicitudes.<br>: Actualmente, algunos visores de Dynamic Media no funcionan cuando están activados la  **[!UICONTROL ofuscación de]** solicitudes y el  **[!UICONTROL bloqueo de]** solicitudes .

## Ejemplo {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica a:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Cualquier ocurrencia de &#39;=&#39;, &#39;&amp;&#39; y &#39;%&#39; en cadenas de valor debe evitarse usando la codificación &#39;%xx&#39;, antes de que la solicitud se confunda. De lo contrario, no es necesario codificar http-la parte *modificadores* de la solicitud antes o después de la ofuscación, incluso si se aplica el bloqueo de la solicitud, ya que la codificación base64 es segura para la transmisión http.

## Véase también {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codificación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7) HTTP,  [Bloqueo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c) de solicitudes,  [atributo::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
