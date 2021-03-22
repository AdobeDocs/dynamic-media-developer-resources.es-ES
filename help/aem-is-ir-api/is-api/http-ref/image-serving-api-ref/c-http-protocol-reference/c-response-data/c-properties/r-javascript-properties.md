---
description: Si javascript se especifica como formato de respuesta, los datos de respuesta tienen formato para analizarse como un archivo de inclusión JavaScript.
seo-description: Si javascript se especifica como formato de respuesta, los datos de respuesta tienen formato para analizarse como un archivo de inclusión JavaScript.
seo-title: Propiedades de JavaScript
solution: Experience Manager
title: Propiedades de JavaScript
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# Propiedades de JavaScript{#javascript-properties}

Si javascript se especifica como formato de respuesta, los datos de respuesta tienen formato para analizarse como un archivo de inclusión JavaScript.

Una respuesta de propiedades de JavaScript típica tiene esta estructura general:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* puede estar vacío. El espacio en blanco es opcional al principio y al final de cada línea y antes y después del separador = . Todos los valores se incluyen entre comillas simples. Las comillas simples en cadenas se escapan con dos comillas simples consecutivas.

Para analizar una respuesta de propiedades de JavaScript, se deben crear todos los objetos a los que se hace referencia en la respuesta antes de cargar el archivo de propiedades. A continuación se muestra un ejemplo de cómo utilizar `req=props` para obtener el tamaño de imagen de respuesta en JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

