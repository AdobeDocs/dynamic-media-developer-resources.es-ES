---
description: Para reducir la posibilidad de manipular las solicitudes, se ofrece una sencilla instalación de bloqueo.
seo-description: Para reducir la posibilidad de manipular las solicitudes, se ofrece una sencilla instalación de bloqueo.
seo-title: Solicitud de bloqueo
solution: Experience Manager
title: Solicitud de bloqueo
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Solicitar bloqueo{#request-locking}

Para reducir la posibilidad de manipular las solicitudes, se ofrece una sencilla instalación de bloqueo.

Si se establece attribute::RequestLock, se debe anexar un valor de bloqueo a la solicitud, en forma de `&xxxx`, siendo xxxx un valor hexadecimal de cuatro dígitos. Este valor hexadecimal se genera mediante un algoritmo hash simple aplicado a la porción *modificadores* de la solicitud (después de &#39;?&#39; que separa la ruta de URL de los *modificadores*). Esto debe hacerse después de que la solicitud esté completamente codificada en http, pero antes de que se ofusque (opcionalmente). Después de anular la confusión de la solicitud, el servidor utilizará el mismo algoritmo hash en la cadena del modificador (excepto los últimos 5 caracteres, que contienen el valor de bloqueo). Si la clave generada no coincide con el bloqueo, se rechaza la solicitud.

>[!IMPORTANT]
>
>Si habilita esta función, tenga en cuenta que su uso tiene ciertas limitaciones que incluyen:<br>- Es posible que la interfaz de usuario de Dynamic Media no muestre los detalles correctos para el campo **[!UICONTROL Última publicación]**. Sin embargo, esto no afecta a la publicación.<br>- Actualmente, el flujo de vídeo HLS no funciona cuando **[!UICONTROL Solicitar]** confusión y  **[!UICONTROL Solicitar]** bloqueo están activados.<br>- Actualmente, algunos visores de Dynamic Media no funcionan cuando  **[!UICONTROL Solicitar]** confusión y  **[!UICONTROL solicitar]** bloqueo están activados.

Código de ejemplo de C++ para generar el valor de bloqueo de la solicitud:

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## Véase también {#section-a6d45406c0354669ac581793e4fa8436}

[Codificación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7) HTTP, confusión  [de solicitud](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d),  [atributo::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
