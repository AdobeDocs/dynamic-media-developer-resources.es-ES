---
description: Las transformaciones se aplican a las imágenes de origen y a las capas de texto.
solution: Experience Manager
title: Transformaciones de capa
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# Transformaciones de capa{#layer-transforms}

Las transformaciones se aplican a las imágenes de origen y a las capas de texto.

Las siguientes operaciones se aplican a las imágenes de origen, en el orden dado, para lograr la relación espacial deseada con la capa 0:

1. Aplicar `crop=`, si se especifica.
1. Escala basada en `size=` o, si no se especifica `size=`, basada en `scale=`, o, si no se especifica `scale=`, basada en `res=`, o, si no se especifica `res=`, utilice la imagen de origen de resolución completa.
1. Aplicar `flip=`, si se especifica.
1. Aplicar `rotate=`, si se especifica.
1. Aplicar `extend=`, si se especifica.
1. Coloque la capa en el lienzo en función de `origin=` y `pos=` (consulte a continuación).

Las siguientes transformaciones se aplican a las capas de texto:

1. El tamaño del cuadro de texto viene determinado por `size=`, o por la anchura y la altura del texto, si `size=` solo se proporciona parcialmente o no se proporciona en absoluto. El texto se alinea dentro del cuadro de texto utilizando los atributos de alineación de texto rtf. El texto se puede recortar mediante el cuadro de texto.
1. Escale el contenido del texto según la resolución especificada con `textAttr=`.
1. Aplicar `rotate=`, si se especifica.
1. Aplicar `extend=`, si se especifica.
1. Coloque la capa en el lienzo en función de `origin=` y `pos=` (ver abajo).

Para las capas de imagen y de texto, el último paso para colocar la capa en el lienzo no se aplica a la capa 0, ya que la capa 0 constituye efectivamente el lienzo.
