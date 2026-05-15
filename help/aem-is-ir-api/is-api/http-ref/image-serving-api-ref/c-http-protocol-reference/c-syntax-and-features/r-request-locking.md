---
description: Para reducir las oportunidades de manipulación de solicitudes, se proporciona una facilidad de bloqueo simple.
solution: Experience Manager
title: Solicitar bloqueo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
TQID: 'https://experienceleague.adobe.com/9icGIK7meNSVUzYnsFBFM-GwG7KLe90bMDuqN89xmMk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 0%

---

# Solicitar bloqueo{#request-locking}

Para reducir las oportunidades de manipulación de solicitudes, se proporciona una facilidad de bloqueo simple.

Si se establece attribute::RequestLock, se debe anexar un valor de bloqueo a la solicitud, en forma de `&xxxx`, siendo xxxx un valor hexadecimal de cuatro dígitos. Este valor hexadecimal se genera usando un algoritmo hash simple aplicado a la parte de *modificadores* de la solicitud (después de &quot;?&quot;, que separa la ruta de la dirección URL de los *modificadores*). Esto debe hacerse después de que la solicitud esté completamente codificada en http, pero antes de que (opcionalmente) se confunda. Después de eliminar la ofuscación de la solicitud, el servidor utiliza el mismo algoritmo hash en la cadena del modificador (excluyendo los últimos 5 caracteres, que contienen el valor de bloqueo). Si la clave generada no coincide con el bloqueo, se rechaza la solicitud.

>[!IMPORTANT]
>
>Si habilita esta característica, tenga en cuenta que existen ciertas limitaciones en su uso que incluyen lo siguiente:<br>- Es posible que la interfaz de usuario de Dynamic Media no muestre los detalles correctos para el campo **[!UICONTROL Última publicación]**. Sin embargo, este efecto no afecta a la publicación.<br>- Actualmente, la transmisión de vídeo de HLS no funciona cuando **[!UICONTROL Solicitud de ofuscación]** y **[!UICONTROL Solicitud de bloqueo]** están habilitados.<br>- Actualmente, algunos visores de Dynamic Media no funcionan cuando **[!UICONTROL Solicitud de ofuscación]** y **[!UICONTROL Solicitud de bloqueo]** están habilitados.

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

[Codificación HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Confusión de solicitud](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [atributo::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
