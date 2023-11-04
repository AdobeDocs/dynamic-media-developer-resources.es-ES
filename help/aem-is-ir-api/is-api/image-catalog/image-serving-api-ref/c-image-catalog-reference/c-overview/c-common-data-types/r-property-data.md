---
description: Los datos de propiedad consisten en una cadena de texto que representa una o más propiedades.
solution: Experience Manager
title: Datos de propiedad
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# Datos de propiedad{#property-data}

Los datos de propiedad consisten en una cadena de texto que representa una o más propiedades.

Una propiedad consta de un nombre de propiedad y un valor de propiedad, separados por =.

Las propiedades múltiples se separan con separadores de líneas, que pueden ser `??` o `<CR><LF>`. Si toda la cadena de datos de la propiedad no está entre comillas, el servidor reemplaza cada aparición de `??` con `<CR><LF>` antes de transmitir los datos al cliente. Los nombres de propiedades pueden constar de letras, números, &#39;.&#39;, &#39;-&#39; y &#39;_&#39;. Los nombres de propiedad no distinguen entre mayúsculas y minúsculas.

Los valores de propiedad no deben incluir separadores de líneas.

Consulte [Cadena de texto](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) para reglas adicionales aplicadas a los datos de propiedad.
