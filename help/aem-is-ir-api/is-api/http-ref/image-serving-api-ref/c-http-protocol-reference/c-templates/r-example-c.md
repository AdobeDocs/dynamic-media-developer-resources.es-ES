---
description: Cree una aplicación de capas de "muñeca de papel".
seo-description: Cree una aplicación de capas de "muñeca de papel".
seo-title: Ejemplo C
solution: Experience Manager
title: Ejemplo C
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---


# Ejemplo C{#example-c}

Cree una aplicación de capas de &quot;muñeca de papel&quot;.

Una imagen de fondo contiene la foto de un modelo o maniquí. Los registros adicionales del catálogo de imágenes contienen varias prendas de vestir y accesorios, fotografiados para que coincidan con el maniquí en forma y tamaño.

Cada foto de ropa o accesorio está enmascarada y recortada al cuadro delimitador de la máscara para minimizar el tamaño de la imagen. Los anclajes y las resoluciones de las imágenes se controlan cuidadosamente para mantener la alineación entre las capas y la imagen de fondo, y todas las imágenes se añaden a un catálogo de imágenes, con los valores adecuados almacenados en `catalog::Resolution` y `catalog::Anchor`.

Además de las capas, también queremos cambiar el color de los elementos seleccionados. Los registros de estos elementos se procesan previamente para eliminar el color original y ajustar el brillo y el contraste de una manera adecuada para el comando de coloreado. Este preprocesamiento puede realizarse sin conexión, utilizando una herramienta de edición de imágenes como Photoshop o, en casos sencillos, trivialmente añadiendo `op_brightness=` y `op_contrast=` al campo `catalog::Modifier`.

Esta aplicación no justifica una plantilla independiente, ya que todos los objetos ya están correctamente alineados por sus anclajes de imagen ( `catalog::Anchor`) y escalados ( `catalog::Resolution`). Dependemos del cliente para garantizar un orden de capa adecuado.

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

Solo se especifica la altura. Esto permite que la imagen devuelta varíe en anchura según la relación de aspecto de la imagen del maniquí, sin que se rellenen los márgenes con el color de fondo.

No importa qué resolución se especifique para cada capa, siempre y cuando sean iguales. Es posible que esta versión no permita que las vistas sean más grandes que las imágenes compuestas. Si se especifica un valor de resolución grande, se evitarán problemas relacionados con esta limitación. Todo el procesamiento y la composición se realiza con la resolución óptima para el tamaño de imagen solicitado, para ayudar a lograr el mejor rendimiento y calidad de salida.

Los comandos `res=` se pueden omitir si todas las imágenes de origen tienen la misma resolución a escala completa (lo que es probable que sea el caso de este tipo de aplicación).

El `rootId` debe especificarse para todos los comandos `src=`, incluso si son iguales al `rootId` especificado en la ruta de la url.

Si no se va a utilizar ningún catálogo de imágenes, no es posible un enfoque de escalado basado en resolución. En este caso, se deben calcular factores de escala explícitos para cada elemento de capa, según la relación entre los valores `catalog::Resolution` de cada capa y el valor `catalog::Resolution` de la capa de fondo. La solicitud de composición (con menos capas) puede tener este aspecto:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

