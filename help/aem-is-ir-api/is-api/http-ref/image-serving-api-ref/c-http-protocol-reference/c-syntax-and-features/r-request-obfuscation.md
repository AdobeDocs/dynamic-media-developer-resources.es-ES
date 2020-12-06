---
description: El contenido de toda la parte de modificadores de la cadena de solicitud, incluido el sufijo de bloqueo opcional, puede quedar oscurecido al aplicar la codificación estándar base64.
seo-description: El contenido de toda la parte de modificadores de la cadena de solicitud, incluido el sufijo de bloqueo opcional, puede quedar oscurecido al aplicar la codificación estándar base64.
seo-title: Confusión de solicitudes
solution: Experience Manager
title: Confusión de solicitudes
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 1%

---


# Confusión de solicitudes{#request-obfuscation}

El contenido de toda la parte de modificadores de la cadena de solicitud, incluido el sufijo de bloqueo opcional, puede quedar oscurecido al aplicar la codificación estándar base64.

El servidor intenta descodificar si `attribute::RequestObfuscation` está configurado. Si la descodificación falla, se rechaza la solicitud. Si se aplican el bloqueo de solicitudes y la confusión de solicitudes, el sufijo de bloqueo debe generarse y anexarse antes de la codificación base64.

>[!IMPORTANT]
>
>Si habilita esta función, tenga en cuenta que hay ciertas limitaciones en su uso que incluyen lo siguiente:<br>- Es posible que la interfaz de usuario de Dynamic Media no muestre los detalles correctos para el campo **[!UICONTROL Última publicación]** . Sin embargo, esto no afecta a la publicación.<br>- Actualmente, el flujo de vídeo HLS no funciona cuando se activan la confusión **[!UICONTROL de]** solicitudes y el bloqueo **[!UICONTROL de]** solicitudes.<br>- Actualmente, algunos visores de medios dinámicos no funcionan cuando están activados la confusión **[!UICONTROL de]** solicitudes y el bloqueo **[!UICONTROL de]** solicitudes.

## Ejemplo {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica en:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Todas las incidencias de &#39;=&#39;, &#39;&amp;&#39; y &#39;%&#39; en cadenas de valor deben tener un carácter de escape mediante la codificación &#39;%xx&#39;, antes de que la solicitud se confunda. De lo contrario, no es necesario codificar http-la parte de *modificadores* de la solicitud antes o después de la confusión, aunque se aplique el bloqueo de la solicitud, ya que la codificación base64 es segura para la transmisión http.

## Véase también {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codificación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)HTTP, Bloqueo [de](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)solicitudes, [atributo::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
