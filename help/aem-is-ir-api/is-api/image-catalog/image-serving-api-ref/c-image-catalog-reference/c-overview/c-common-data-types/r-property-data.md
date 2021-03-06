---
description: Los datos de propiedad constan de una cadena de texto que representa una o varias propiedades.
solution: Experience Manager
title: Datos de propiedad
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Datos de propiedad{#property-data}

Los datos de propiedad constan de una cadena de texto que representa una o varias propiedades.

Una propiedad consta de un nombre de propiedad y un valor de propiedad, separados por =.

Las propiedades múltiples se separan con separadores de línea, que pueden ser `??` o `<CR><LF>`. Si toda la cadena de datos de la propiedad no está entre comillas, el servidor reemplaza cada incidencia de `??` por `<CR><LF>` antes de transmitir los datos al cliente. Los nombres de propiedades pueden constar de letras, números, &#39;.&#39;, &#39;-&#39; y &#39;_&#39;. Los nombres de propiedades no distinguen entre mayúsculas y minúsculas.

Los valores de propiedad no deben incluir separadores de línea.

Consulte [Cadena de texto](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) para ver las reglas adicionales aplicadas a los datos de propiedad.
