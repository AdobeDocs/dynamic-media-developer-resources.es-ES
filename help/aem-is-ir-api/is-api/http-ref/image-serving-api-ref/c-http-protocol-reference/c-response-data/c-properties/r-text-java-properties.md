---
description: Si el texto se especifica como formato de respuesta, se aplica formato a los datos de respuesta para que sean legibles como propiedades de Java.
seo-description: Si el texto se especifica como formato de respuesta, se aplica formato a los datos de respuesta para que sean legibles como propiedades de Java.
seo-title: Propiedades de texto (Java)
solution: Experience Manager
title: Propiedades de texto (Java)
topic: Scene7 Image Serving - Image Rendering API
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Propiedades de texto (Java){#text-java-properties}

Si el texto se especifica como formato de respuesta, se aplica formato a los datos de respuesta para que sean legibles como propiedades de Java.

Una respuesta típica de propiedades de texto tiene esta estructura general:

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* puede estar vacío. El espacio en blanco es opcional al principio y al final de cada línea y antes y después del separador =. Las comillas simples o dobles pueden utilizarse para incluir valores de cadena, pero no son obligatorias.

Los valores de cadena pueden contener caracteres de escape de estilo JAVA, como `\n`, `\t`, `\:` o `\\`.
