---
description: Los datos de propiedad consisten en una cadena de texto que representa una o más propiedades.
solution: Experience Manager
title: Datos de propiedad
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
TQID: 'https://experienceleague.adobe.com/jE8U1fgDsG9wdzG4O-BsPHvPOGLXDxZRMdZvL9LuYZE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 0%

---

# Datos de propiedad{#property-data}

Los datos de propiedad consisten en una cadena de texto que representa una o más propiedades.

Una propiedad consta de un nombre de propiedad y un valor de propiedad, separados por =.

Las propiedades múltiples están separadas por separadores de líneas, que pueden ser `??` o `<CR><LF>`. Si toda la cadena de datos de la propiedad no está entre comillas, el servidor reemplaza cada ocurrencia de `??` por `<CR><LF>` antes de transmitir los datos al cliente. Los nombres de propiedades pueden constar de letras, números, &#39;.&#39;, &#39;-&#39; y &#39;_&#39;. Los nombres de propiedad no distinguen entre mayúsculas y minúsculas.

Los valores de propiedad no deben incluir separadores de líneas.

Consulte [Cadena de texto](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) para ver las reglas adicionales aplicadas a los datos de propiedad.
