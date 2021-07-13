---
description: Si xml se especifica como formato de respuesta, los datos de respuesta tienen formato de documento XML que puede ser analizado por cualquier analizador XML estándar.
solution: Experience Manager
title: Propiedades XML
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# Propiedades XML{#xml-properties}

Si xml se especifica como formato de respuesta, los datos de respuesta tienen formato de documento XML que puede ser analizado por cualquier analizador XML estándar.

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

El elemento `<prop-group>` se utiliza como contenedor exterior y para agrupar propiedades. Si se nombra un grupo, el nombre corresponde al nombre del objeto Java/JavaScript.

>[!NOTE]
>
>Se puede especificar la codificación de caracteres para algunos tipos `req=`. Consulte la descripción del comando específico `req=`para obtener más información.
