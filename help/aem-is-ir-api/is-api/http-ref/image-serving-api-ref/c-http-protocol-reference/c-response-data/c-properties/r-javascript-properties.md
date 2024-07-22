---
title: Propiedades de JavaScript
description: Si se especifica JavaScript como formato de respuesta, los datos de respuesta se formatean para que se analicen como un archivo JavaScript&trade; include.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Propiedades de JavaScript{#javascript-properties}

Si se especifica JavaScript como formato de respuesta, los datos de respuesta se formatean para que se analicen como un archivo de inclusión JavaScript.

Una respuesta típica de las propiedades de JavaScript tiene esta estructura general:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* puede estar vacío. El espacio en blanco es opcional al principio y al final de cada línea y antes y después del separador =. Todos los valores se incluyen entre comillas simples. Las comillas simples en cadenas se escapan con dos comillas simples consecutivas.

Para analizar una respuesta de propiedades de JavaScript, se debe crear cualquier objeto u objetos a los que se haga referencia en la respuesta antes de cargar el archivo de propiedades. A continuación se muestra un ejemplo de cómo usar `req=props` para obtener el tamaño de imagen de respuesta en JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
