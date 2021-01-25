---
description: Cree una aplicación de capas de "muñeca de papel".
seo-description: Cree una aplicación de capas de "muñeca de papel".
seo-title: Ejemplo C
solution: Experience Manager
title: Ejemplo C
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Ejemplo C{#example-c}

Cree una aplicación de capas de &quot;muñeca de papel&quot;.

Una imagen de fondo contiene la fotografía de un modelo o maniquí. Los registros adicionales del catálogo de imágenes contienen varios artículos de vestimenta y accesorios, fotografiados para que coincidan con el maniquí en forma y tamaño.

Cada imagen de vestimenta o accesorio se enmascara y se recorta al cuadro delimitador de máscara para minimizar el tamaño de la imagen. Los anclajes y las resoluciones de las imágenes se controlan cuidadosamente para mantener la alineación entre las capas y la imagen de fondo, y todas las imágenes se agregan a un catálogo de imágenes, con los valores adecuados almacenados en `catalog::Resolution` y `catalog::Anchor`.

Además de las capas, también queremos cambiar el color de los elementos seleccionados. Los registros de estos elementos se preprocesan para eliminar el color original y ajustar el brillo y el contraste de una manera adecuada para el comando de coloreado. Este preprocesamiento se puede realizar sin conexión, utilizando una herramienta de edición de imágenes como Photoshop o, en casos sencillos, se puede realizar trivialmente agregando `op_brightness=` y `op_contrast=` al campo `catalog::Modifier`.

Esta aplicación no justifica una plantilla independiente, ya que todos los objetos ya están correctamente alineados por sus anclajes de imagen ( `catalog::Anchor`) y escalados ( `catalog::Resolution`). Dependemos del cliente para garantizar un orden de capas adecuado.

Una solicitud típica podría tener este aspecto:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Solo se especifica la altura. Esto permite que la imagen devuelta varíe en anchura según la proporción de aspecto de la imagen maniquí, sin que los márgenes se rellenen con el color de fondo.

No debe importar qué resolución se especifique para cada capa, siempre y cuando todos sean iguales. Es posible que esta versión no permita que las vistas sean más grandes que las imágenes compuestas. Especificar un valor de resolución grande evita problemas relacionados con esta limitación. Todo el procesamiento y la composición se realiza con la resolución óptima para el tamaño de imagen solicitado, con el fin de lograr el mejor rendimiento y la mejor calidad de salida.

Los comandos `res=` se pueden omitir si todas las imágenes de origen tienen la misma resolución a escala completa (lo que es probable para este tipo de aplicación).

Se debe especificar `rootId` para todos los comandos `src=`, incluso si son iguales a los `rootId` especificados en la ruta de URL.

Si no se va a utilizar ningún catálogo de imágenes, no es posible un enfoque de escala basado en resolución. En este caso, se deben calcular factores de escala explícitos para cada elemento de capa, en función de la relación de los valores `catalog::Resolution` de cada capa con el valor `catalog::Resolution` de la capa de fondo. La solicitud de composición (con menos capas) puede tener este aspecto:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

