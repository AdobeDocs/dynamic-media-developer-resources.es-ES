---
description: Si se especifica texto como formato de respuesta, los datos de respuesta se formatean para que se puedan leer como propiedades Java.
solution: Experience Manager
title: Propiedades de texto (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Propiedades de texto (Java){#text-java-properties}

Si se especifica texto como formato de respuesta, los datos de respuesta se formatean para que se puedan leer como propiedades Java.

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

*`propertyValue`* puede estar vacío. El espacio en blanco es opcional al principio y al final de cada línea y antes y después del separador =. Se pueden utilizar comillas simples o dobles para incluir valores de cadena, pero no son necesarias.

Los valores de cadena pueden contener caracteres de escape de estilo JAVA, como `\n`, `\t`, `\:` o `\\`.
