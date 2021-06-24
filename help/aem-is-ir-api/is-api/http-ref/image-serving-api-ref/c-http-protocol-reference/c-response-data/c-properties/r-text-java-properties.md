---
description: Si se especifica texto como formato de respuesta, se da formato a los datos de respuesta para que se puedan leer como propiedades Java.
solution: Experience Manager
title: Propiedades de texto (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
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
