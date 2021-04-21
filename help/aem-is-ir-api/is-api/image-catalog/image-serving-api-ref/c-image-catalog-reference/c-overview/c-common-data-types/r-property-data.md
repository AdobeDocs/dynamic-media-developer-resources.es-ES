---
description: Los datos de propiedad constan de una cadena de texto que representa una o varias propiedades.
solution: Experience Manager
title: Datos de propiedad
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Datos de propiedad{#property-data}

Los datos de propiedad constan de una cadena de texto que representa una o varias propiedades.

Una propiedad consta de un nombre de propiedad y un valor de propiedad, separados por =.

Las propiedades múltiples se separan con separadores de línea, que pueden ser `??` o `<CR><LF>`. Si toda la cadena de datos de la propiedad no está entre comillas, el servidor reemplaza cada incidencia de `??` por `<CR><LF>` antes de transmitir los datos al cliente. Los nombres de propiedades pueden constar de letras, números, &#39;.&#39;, &#39;-&#39; y &#39;_&#39;. Los nombres de propiedades no distinguen entre mayúsculas y minúsculas.

Los valores de propiedad no deben incluir separadores de línea.

Consulte [Cadena de texto](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) para ver las reglas adicionales aplicadas a los datos de propiedad.
