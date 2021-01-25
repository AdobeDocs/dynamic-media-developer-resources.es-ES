---
description: Los datos de propiedad se devuelven en respuesta a los siguientes req= type imageprops y props.
seo-description: Los datos de propiedad se devuelven en respuesta a los siguientes req= type imageprops y props.
seo-title: Propiedades
solution: Experience Manager
title: Propiedades
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 5%

---


# Propiedades{#properties}

Los datos de propiedad se devuelven en respuesta a los siguientes tipos req=: props de imágenes y props.

Los datos de respuesta están formateados para que sean legibles como propiedades de Java. Una respuesta típica de propiedades de texto tiene esta estructura general:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` puede estar vacío. El espacio en blanco es opcional al principio y al final de cada línea y antes y después del separador &#39;=&#39;. Las comillas simples o dobles pueden utilizarse para incluir valores de cadena, pero no son obligatorias.

Los valores de cadena pueden contener caracteres de escape de estilo JAVA, como `\n`, `\t`, `\:`. o `\\`.

**Véase también**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
