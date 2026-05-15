---
description: Si se especifica texto como formato de respuesta, los datos de respuesta se formatean para que se puedan leer como propiedades Java.
solution: Experience Manager
title: Propiedades de texto (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
TQID: 'https://experienceleague.adobe.com/WNIuNvCPLdbeweHB5gkcFfeZu2WDDUk53us6SHtmO-A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
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
