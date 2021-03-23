---
description: Si xml se especifica como formato de respuesta, los datos de respuesta tienen formato de documento XML que puede ser analizado por cualquier analizador XML estándar.
seo-description: Si xml se especifica como formato de respuesta, los datos de respuesta tienen formato de documento XML que puede ser analizado por cualquier analizador XML estándar.
seo-title: Propiedades XML
solution: Experience Manager
title: Propiedades XML
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
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

