---
description: Si se especifica JavaScript™ como formato de respuesta, los datos de respuesta tienen el formato que se va a analizar como un archivo de inclusión JavaScript™.
solution: Experience Manager
title: Propiedades de JavaScript™
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# Propiedades de JavaScript™{#javascript-properties}

Si se especifica JavaScript™ como formato de respuesta, los datos de respuesta tienen el formato que se va a analizar como un archivo de inclusión JavaScript™.

Una respuesta típica de propiedades de JavaScript™ tiene esta estructura general:

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

Para analizar una respuesta de propiedades de JavaScript™, cualquier objeto u objeto al que se haga referencia en la respuesta debe crearse antes de cargar el archivo de propiedades. A continuación se muestra un ejemplo de cómo utilizar `req=props` para obtener el tamaño de imagen de respuesta en JavaScript™:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

