---
description: Si se especifica texto como formato de respuesta, se da formato a los datos de respuesta para que se puedan leer como propiedades Java.
seo-description: Si se especifica texto como formato de respuesta, se da formato a los datos de respuesta para que se puedan leer como propiedades Java.
seo-title: Propiedades de texto (Java)
solution: Experience Manager
title: Propiedades de texto (Java)
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# Propiedades de texto (Java){#text-java-properties}

Si se especifica texto como formato de respuesta, se da formato a los datos de respuesta para que se puedan leer como propiedades Java.

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

*`propertyValue`* puede estar vacío. El espacio en blanco es opcional al principio y al final de cada línea y antes y después del separador = . Las comillas simples o dobles pueden utilizarse para incluir valores de cadena, pero no son obligatorias.

Los valores de cadena pueden contener caracteres de escape de estilo JAVA, como `\n`, `\t`, `\:` o `\\`.
