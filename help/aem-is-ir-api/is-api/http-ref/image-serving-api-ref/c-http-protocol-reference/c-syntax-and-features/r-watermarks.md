---
description: El servicio de imágenes implementa una función visual simple de marca de agua.
solution: Experience Manager
title: Filigranas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Filigranas{#watermarks}

El servicio de imágenes implementa una función visual simple de marca de agua.

Una marca de agua suele ser una imagen semitransparente, pero puede ser texto o una imagen compuesta de capas más compleja. El servidor coloca la marca de agua sobre la imagen de respuesta después de aplicar todos los atributos de vista ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`).

La marca de agua se habilita estableciendo `attribute::Watermark` en una entrada de catálogo válida que contendría la imagen o plantilla de la marca de agua. Si `attribute::Watermark` se establece en un catálogo con nombre, el servidor agrega la marca de agua a todas las solicitudes de imagen que hacen referencia al ID de catálogo en la dirección URL de la solicitud. Si se establece `default::Watermark` (en el catálogo predeterminado, [!DNL default.ini]), la marca de agua se aplica a todas las solicitudes de imagen independientemente de si hacen referencia a un catálogo o no.

Las marcas de agua no se aplican a las imágenes devueltas como respuesta a las solicitudes de miniaturas ( `req=tmb`) y a ciertas solicitudes de los visualizadores de Dynamic Media.

## Escala y alineación {#section-89ef9e5926ae438abbd8e70332749b76}

Cuando se especifica una marca de agua, el servidor genera primero la imagen compuesta (la *imagen de destino*) a la que debe aplicarse la marca de agua (antes de aplicar las transformaciones de vista). A continuación, el servidor genera la imagen compuesta para la marca de agua como cualquier otra imagen (la *imagen de marca de agua*).

A diferencia de las imágenes estándar, se puede especificar `sizeN=` para layer=0 o layer=comp de la imagen de marca de agua. Esto permite escalar la imagen de marca de agua en relación con la imagen de destino. Si no se especifica `sizeN=`, la imagen de marca de agua conservará su tamaño de píxel al combinarse con la imagen de destino.

Los comandos de solicitud (como `fmt=`) y de vista (como `wid=`) se omiten en los registros de marcas de agua, a excepción de `align=`. `align=` se puede usar para colocar la imagen de marca de agua en relación con la imagen de marca de agua en relación con la imagen de destino. Esto permite colocar la marca de agua en relación con una esquina o borde de la imagen de destino.

Después de escalar y alinear, el servidor coloca la imagen de marca de agua en la imagen de destino con los valores `blendMode=` y `opac=` especificados para `layer=0` o `layer=comp` de la imagen de marca de agua. Por último, los comandos de solicitud y visualización especificados para la imagen de destino se aplican para construir la imagen de respuesta.

Tenga en cuenta que la imagen de marca de agua nunca se extiende sobre ningún espacio en blanco agregado a la imagen de respuesta por los comandos `wid=` y `hei=`.

## Ejemplo {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Una marca de agua típica puede consistir en una imagen RGBA simple que contiene un logotipo o un aviso de copyright. Creamos un registro en el catálogo de imágenes (o en el catálogo predeterminado) con `catalog::Id` establecido en `watermark` y especificamos el archivo de imagen de marca de agua en `catalog::Path`. Queremos ampliar la marca de agua para que se ajuste a la imagen de la vista (sin distorsionar la marca de agua) dejando un poco de margen adicional y reducir la opacidad al 20% de la marca de agua original, por lo que establecemos `catalog::Modifier` en `sizeN=0.9,0.9&opac=20`. Para activar la marca de agua, establezca `attribute::Watermark` en el identificador de la entrada de catálogo de la marca de agua, &quot;marca de agua&quot; en este ejemplo. Es posible que queramos experimentar con diferentes opciones de `blendMode=` para lograr diferentes efectos de marca de agua.

## Véase también {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Filigrana](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
