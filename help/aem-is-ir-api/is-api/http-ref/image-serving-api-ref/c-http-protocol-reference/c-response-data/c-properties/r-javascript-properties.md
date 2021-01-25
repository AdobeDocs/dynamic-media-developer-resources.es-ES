---
description: Si se especifica javascript como formato de respuesta, los datos de respuesta tienen el formato de analizarse como archivo de inclusión JavaScript.
seo-description: Si se especifica javascript como formato de respuesta, los datos de respuesta tienen el formato de analizarse como archivo de inclusión JavaScript.
seo-title: Propiedades de JavaScript
solution: Experience Manager
title: Propiedades de JavaScript
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# Propiedades de JavaScript{#javascript-properties}

Si se especifica javascript como formato de respuesta, los datos de respuesta tienen el formato de analizarse como archivo de inclusión JavaScript.

Una respuesta típica de propiedades de JavaScript tiene esta estructura general:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* puede estar vacío. El espacio en blanco es opcional al principio y al final de cada línea y antes y después del separador =. Todos los valores se encierran entre comillas simples. Las comillas simples en cadenas se escapan con dos comillas simples consecutivas.

Para analizar una respuesta de propiedades de JavaScript, se deben crear todos los objetos a los que se hace referencia en la respuesta antes de cargar el archivo de propiedades. A continuación se muestra un ejemplo de uso de `req=props` para obtener el tamaño de imagen de respuesta en JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

