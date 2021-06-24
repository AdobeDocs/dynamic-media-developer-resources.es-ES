---
description: Los datos de propiedad se devuelven en respuesta a los siguientes tipos de imágenes req= tipos, props y props.
solution: Experience Manager
title: Propiedades
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
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
