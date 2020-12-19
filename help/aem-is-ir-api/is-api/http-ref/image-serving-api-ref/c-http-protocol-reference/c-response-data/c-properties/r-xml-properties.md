---
description: Si se especifica xml como formato de respuesta, los datos de respuesta tienen el formato de documento XML que puede analizar cualquier analizador XML estándar.
seo-description: Si se especifica xml como formato de respuesta, los datos de respuesta tienen el formato de documento XML que puede analizar cualquier analizador XML estándar.
seo-title: Propiedades XML
solution: Experience Manager
title: Propiedades XML
topic: Scene7 Image Serving - Image Rendering API
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Propiedades XML{#xml-properties}

Si se especifica xml como formato de respuesta, los datos de respuesta tienen el formato de documento XML que puede analizar cualquier analizador XML estándar.

Un documento de respuesta de propiedades típicas tiene esta estructura general:

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

El elemento `<prop-group>` se utiliza como contenedor externo y para agrupar propiedades. Si se nombra un grupo, el nombre corresponde al nombre del objeto Java/JavaScript.

>[!NOTE]
>
>Se puede especificar la codificación de caracteres para algunos tipos `req=`. Consulte la descripción del comando `req=`específico para obtener más información.

