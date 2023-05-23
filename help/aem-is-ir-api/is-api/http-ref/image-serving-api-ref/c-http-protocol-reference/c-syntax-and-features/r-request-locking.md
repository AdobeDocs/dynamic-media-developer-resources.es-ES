---
description: Para reducir las oportunidades de manipulación de solicitudes, se proporciona una facilidad de bloqueo simple.
solution: Experience Manager
title: Solicitar bloqueo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Solicitar bloqueo{#request-locking}

Para reducir las oportunidades de manipulación de solicitudes, se proporciona una facilidad de bloqueo simple.

Si se establece attribute::RequestLock, se debe anexar un valor de bloqueo a la solicitud en forma de `&xxxx`, siendo xxxx un valor hexadecimal de cuatro dígitos. Este valor hexadecimal se genera utilizando un algoritmo hash simple aplicado a *modificadores* parte de la solicitud (después de &quot;?&quot; que separa la ruta URL de la *modificadores*). Esto debe hacerse después de que la solicitud esté completamente codificada en http, pero antes de que (opcionalmente) se confunda. Después de eliminar la ofuscación de la solicitud, el servidor utilizará el mismo algoritmo hash en la cadena del modificador (excluyendo los últimos 5 caracteres, que contienen el valor de bloqueo). Si la clave generada no coincide con el bloqueo, se rechaza la solicitud.

>[!IMPORTANT]
>
>Si habilita esta función, tenga en cuenta que su uso tiene ciertas limitaciones, entre las que se incluyen las siguientes:<br>- Es posible que la interfaz de usuario de Dynamic Media no muestre los detalles correctos para **[!UICONTROL Última publicación]** field. Sin embargo, este efecto no afecta a la publicación.<br>- Actualmente, la transmisión de vídeo HLS no funciona cuando **[!UICONTROL Ofuscación de solicitud]** y **[!UICONTROL Solicitar bloqueo]** están activadas.<br>: Actualmente, algunos visores de Dynamic Media no funcionan cuando **[!UICONTROL Ofuscación de solicitud]** y **[!UICONTROL Solicitar bloqueo]** están activadas.

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

[Codificación HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Confusión de solicitud](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
