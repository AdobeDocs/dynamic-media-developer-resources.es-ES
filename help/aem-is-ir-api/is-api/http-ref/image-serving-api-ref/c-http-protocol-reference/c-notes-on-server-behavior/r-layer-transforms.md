---
description: Las transformaciones se aplican a las imágenes de origen y a las capas de texto.
solution: Experience Manager
title: Transformaciones de capa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Transformaciones de capa{#layer-transforms}

Las transformaciones se aplican a las imágenes de origen y a las capas de texto.

Las siguientes operaciones se aplican a las imágenes de origen, en el orden dado, para lograr la relación espacial deseada con la capa 0:

1. Aplicar `crop=`, si se especifica.
1. Escala basada en `size=` o, si `size=` no se ha especificado, según `scale=`, o, si `scale=` no se ha especificado, según `res=`, o, si `res=`no se ha especificado, utilice la imagen de origen de resolución completa.
1. Aplicar `flip=`, si se especifica.
1. Aplicar `rotate=`, si se especifica.
1. Aplicar `extend=`, si se especifica.
1. Coloque la capa en el lienzo basándose en `origin=` y `pos=` (ver más abajo).

Las siguientes transformaciones se aplican a las capas de texto:

1. El tamaño del cuadro de texto está determinado por `size=`, o la anchura y altura del texto, si `size=` solo se proporciona parcialmente o en absoluto. El texto se alinea dentro del cuadro de texto mediante los atributos de alineación de texto rtf. El texto se puede recortar mediante el cuadro de texto.
1. Escalar el contenido del texto en función de la resolución especificada con `textAttr=`.
1. Aplicar `rotate=`, si se especifica.
1. Aplicar `extend=`, si se especifica.
1. Coloque la capa en el lienzo basándose en `origin=` y `pos=`(ver más abajo).

Tanto para las capas de imagen como para las de texto, el último paso (colocar la capa en el lienzo) no se aplica a la capa 0, ya que la capa 0 constituye efectivamente el lienzo.
