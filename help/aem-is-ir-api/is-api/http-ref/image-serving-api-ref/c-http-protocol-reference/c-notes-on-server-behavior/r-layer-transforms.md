---
description: Las transformaciones se aplican a las imágenes de origen y a las capas de texto.
seo-description: Las transformaciones se aplican a las imágenes de origen y a las capas de texto.
seo-title: Transformaciones de capas
solution: Experience Manager
title: Transformaciones de capas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# La capa se transforma{#layer-transforms}

Las transformaciones se aplican a las imágenes de origen y a las capas de texto.

Las siguientes operaciones se aplican a las imágenes de origen, en un orden determinado, para lograr la relación espacial deseada con la capa 0:

1. Aplicar `crop=`, si se especifica.
1. Escala basada en `size=` o, si no se especifica `size=`, basada en `scale=`, o, si no se especifica `scale=`, basada en `res=` o, si no se especifica `res=`, utilice la imagen de origen de resolución completa.
1. Aplicar `flip=`, si se especifica.
1. Aplicar `rotate=`, si se especifica.
1. Aplicar `extend=`, si se especifica.
1. Coloque la capa en el lienzo en función de `origin=` y `pos=` (véase más adelante).

Las siguientes transformaciones se aplican a las capas de texto:

1. El tamaño del cuadro de texto está determinado por `size=`, o la anchura y altura del texto, si `size=` sólo se proporciona parcialmente o no se proporciona en absoluto. El texto se alinea dentro del cuadro de texto utilizando los atributos de alineación de texto rtf. El texto se puede recortar mediante el cuadro de texto.
1. Escale el contenido del texto según la resolución especificada con `textAttr=`.
1. Aplicar `rotate=`, si se especifica.
1. Aplicar `extend=`, si se especifica.
1. Coloque la capa en el lienzo en función de `origin=` y `pos=` (ver abajo).

Tanto para las capas de imagen como de texto, el último paso para colocar la capa en el lienzo no se aplica a la capa 0, ya que la capa 0 constituye efectivamente el lienzo.
