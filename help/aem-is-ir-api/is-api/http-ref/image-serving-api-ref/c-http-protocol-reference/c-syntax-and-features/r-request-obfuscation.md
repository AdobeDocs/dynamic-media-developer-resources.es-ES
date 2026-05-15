---
description: El contenido de toda la parte de modificadores de la cadena de solicitud, incluido el sufijo de bloqueo opcional, puede oscurecerse al aplicar la codificación base64 estándar.
solution: Experience Manager
title: Ofuscación de solicitud
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
TQID: 'https://experienceleague.adobe.com/77Q5rV3cP4KoBz3rFKlEmBlumS0TBthuLbLQBETPitE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 1%

---

# Ofuscación de solicitud{#request-obfuscation}

El contenido de toda la parte de modificadores de la cadena de solicitud, incluido el sufijo de bloqueo opcional, puede oscurecerse al aplicar la codificación base64 estándar.

El servidor intenta descodificar si `attribute::RequestObfuscation` está establecido. Si la descodificación falla, se rechaza la solicitud. Si se aplican tanto el bloqueo de solicitud como la ofuscación de solicitud, el sufijo de bloqueo debe generarse y anexarse antes de la codificación base64.

>[!IMPORTANT]
>
>Si habilita esta característica, tenga en cuenta que existen ciertas limitaciones en su uso que incluyen lo siguiente:<br>- Es posible que la interfaz de usuario de Dynamic Media no muestre los detalles correctos para el campo **[!UICONTROL Última publicación]**. Sin embargo, este efecto no afecta a la publicación.<br>- Actualmente, la transmisión de vídeo de HLS no funciona cuando **[!UICONTROL Solicitud de ofuscación]** y **[!UICONTROL Solicitud de bloqueo]** están habilitados.<br>- Actualmente, algunos visores de Dynamic Media no funcionan cuando **[!UICONTROL Solicitud de ofuscación]** y **[!UICONTROL Solicitud de bloqueo]** están habilitados.

## Ejemplo {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica en:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Cualquier aparición de &#39;=&#39;, &#39;&amp;&#39; y &#39;%&#39; en cadenas de valor debe evitarse con la codificación &#39;%xx&#39;, antes de que la solicitud se confunda. No es necesario codificar mediante http los *modificadores* que forman parte de la solicitud antes o después de la ofuscación, incluso si se aplica el bloqueo de la solicitud, ya que la codificación base64 es segura para la transmisión mediante http.

## Véase también {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codificación HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Bloqueo de solicitudes](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [atributo::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
