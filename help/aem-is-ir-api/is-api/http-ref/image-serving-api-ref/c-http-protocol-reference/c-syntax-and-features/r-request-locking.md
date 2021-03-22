---
description: Para reducir las posibilidades de manipular las solicitudes, se proporciona una sencilla instalación de bloqueo.
seo-description: Para reducir las posibilidades de manipular las solicitudes, se proporciona una sencilla instalación de bloqueo.
seo-title: Solicitar bloqueo
solution: Experience Manager
title: Solicitar bloqueo
uuid: 03239376-1e40-48d2-a396-c276802854ed
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# Solicitar bloqueo{#request-locking}

Para reducir las posibilidades de manipular las solicitudes, se proporciona una sencilla instalación de bloqueo.

Si el atributo::RequestLock está establecido, se debe añadir un valor de bloqueo a la solicitud en forma de `&xxxx`, siendo xxxx un valor hexadecimal de cuatro dígitos. Este valor hexadecimal se genera utilizando un algoritmo hash simple aplicado a la porción *modificadores* de la solicitud (después de &quot;?&quot; que separa la ruta de URL de los *modificadores*). Esto debe hacerse después de que la solicitud esté completamente codificada en http, pero antes de que se confunda (opcionalmente). Después de desconfundir la solicitud, el servidor utilizará el mismo algoritmo de hash en la cadena del modificador (excepto los últimos 5 caracteres, que contienen el valor de bloqueo). Si la clave generada no coincide con el bloqueo, se rechaza la solicitud.

>[!IMPORTANT]
>
>Si habilita esta función, tenga en cuenta que existen ciertas limitaciones en su uso que incluyen lo siguiente:<br>- Es posible que la interfaz de usuario de Dynamic Media no muestre los detalles correctos para el campo **[!UICONTROL Última publicación]**. Sin embargo, este efecto no afecta a la publicación.<br>- Actualmente, el flujo de vídeo HLS no funciona cuando se activan la **[!UICONTROL ofuscación de]** solicitudes y el  **[!UICONTROL bloqueo de]** solicitudes.<br>: Actualmente, algunos visores de Dynamic Media no funcionan cuando están activados la  **[!UICONTROL ofuscación de]** solicitudes y el  **[!UICONTROL bloqueo de]** solicitudes .

Código de ejemplo C++ para generar el valor de bloqueo de la solicitud:

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

[Codificación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7) HTTP,  [ofuscación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d) de solicitud,  [atributo::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
