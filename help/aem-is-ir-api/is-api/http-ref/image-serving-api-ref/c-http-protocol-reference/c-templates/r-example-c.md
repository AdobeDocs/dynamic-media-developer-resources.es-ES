---
title: Ejemplo C
description: Cree una aplicación de capas de "muñeca de papel".
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Ejemplo C{#example-c}

Cree una aplicación de capas de &quot;muñeca de papel&quot;.

Una imagen de fondo contiene la foto de un modelo o maniquí. Los registros adicionales en el catálogo de imágenes contienen varias prendas y accesorios, fotografiados para que coincidan con el maniquí en forma y tamaño.

Cada foto de ropa/accesorio se enmascara y se recorta a la caja limitadora de la máscara para minimizar los tamaños de imagen. Los anclajes y las resoluciones de las imágenes se controlan cuidadosamente para mantener la alineación entre las capas y la imagen de fondo, y todas las imágenes se añaden a un catálogo de imágenes, con los valores adecuados almacenados en `catalog::Resolution` y `catalog::Anchor`.

Además de las capas, también desea cambiar el color de los elementos seleccionados. Los registros de estos elementos se preprocesan para eliminar el color original y ajustar el brillo y el contraste de una manera adecuada para el comando de coloreado. Este preprocesamiento se puede realizar sin conexión, con una herramienta de edición de imágenes como Adobe Photoshop o, en casos sencillos, añadiendo `op_brightness=` y `op_contrast=` a la `catalog::Modifier`field.

Esta aplicación no garantiza una plantilla independiente, ya que todos los objetos ya están correctamente alineados por sus anclajes de imagen ( `catalog::Anchor`) y escalado ( `catalog::Resolution`). Depende del cliente garantizar el orden de capas adecuado.

Una solicitud típica puede tener este aspecto:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Solo se especifica la altura. Al hacerlo, la imagen devuelta puede variar en anchura según la proporción de aspecto de la imagen del maniquí, sin que los márgenes se rellenen con el color de fondo.

No debería importar la resolución especificada para cada capa, siempre y cuando todas sean iguales. Es posible que esta versión no permita que las vistas sean más grandes que las imágenes compuestas. Especificar un valor de resolución grande evita problemas relacionados con esta limitación. Todo el procesamiento y la composición se realizan con la resolución óptima para el tamaño de imagen solicitado, para ayudar a lograr el mejor rendimiento y calidad de salida.

El `res=` Los comandos se pueden omitir si todas las imágenes de origen tienen la misma resolución a escala completa (lo que probablemente sea el caso para este tipo de aplicación).

El `rootId` se debe especificar para todo `src=` comandos, incluso si son los mismos que los comandos `rootId` especificado en la ruta url.

Si no se va a utilizar ningún catálogo de imágenes, no es posible aplicar un enfoque de escala basado en la resolución. En este caso, se deben calcular los factores de escala explícitos para cada elemento de capa, en función de la proporción del `catalog::Resolution` valores para cada capa en el `catalog::Resolution` valor de la capa de fondo. La solicitud de composición (con menos capas) puede tener este aspecto:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
