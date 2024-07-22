---
title: Propiedades
description: Los datos de propiedad se devuelven en respuesta a los siguientes req= tipos imageprops y props.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Propiedades{#properties}

Los datos de propiedad se devuelven en respuesta a los siguientes req= tipos: imageprops y props.

Los datos de respuesta tienen el formato para que se puedan leer como propiedades Java™. Una respuesta típica de propiedades de texto tiene esta estructura general:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` puede estar vacío. El espacio en blanco es opcional al principio y al final de cada línea y antes y después del separador &quot;=&quot;. Se pueden utilizar comillas simples o dobles para incluir valores de cadena, pero no son necesarias.

Los valores de cadena pueden contener caracteres de escape de estilo JAVA, como `\n`, `\t`, `\:` o `\\`.

**Ver también**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
