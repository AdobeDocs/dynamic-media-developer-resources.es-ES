---
description: Los datos de propiedad se devuelven en respuesta a los siguientes tipos de imágenes req= tipos, props y props.
seo-description: Los datos de propiedad se devuelven en respuesta a los siguientes tipos de imágenes req= tipos, props y props.
seo-title: Propiedades
solution: Experience Manager
title: Propiedades
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# Propiedades{#properties}

Los datos de propiedad se devuelven en respuesta a los siguientes tipos req=: imageprops y props.

Los datos de respuesta tienen el formato para que se puedan leer como propiedades Java. Una respuesta típica de propiedades de texto tiene esta estructura general:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` puede estar vacío. El espacio en blanco es opcional al principio y al final de cada línea y antes y después del separador &#39;=&#39;. Las comillas simples o dobles pueden utilizarse para incluir valores de cadena, pero no son obligatorias.

Los valores de cadena pueden contener caracteres de escape de estilo JAVA, como `\n`, `\t`, `\:`. o `\\`.

**Véase también**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
