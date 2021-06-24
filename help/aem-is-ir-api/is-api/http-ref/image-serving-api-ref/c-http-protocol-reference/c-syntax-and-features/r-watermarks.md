---
description: Image Serving implementa una sencilla función visual de marca de agua.
solution: Experience Manager
title: Filigranas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 1%

---

# Filigranas{#watermarks}

Image Serving implementa una sencilla función visual de marca de agua.

Una marca de agua suele ser una imagen semitransparente, pero puede ser texto o una imagen compuesta en capas más compleja. El servidor colocará la marca de agua sobre la imagen de respuesta después de aplicar todos los atributos de vista ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`).

La marca de agua está habilitada estableciendo `attribute::Watermark` en una entrada de catálogo válida que contendría la imagen o plantilla de marca de agua. Si `attribute::Watermark` se configura en un catálogo con nombre, el servidor agregará la marca de agua a todas las solicitudes de imagen que hagan referencia al ID de catálogo en la dirección URL de la solicitud. Si `default::Watermark` está establecido (en el catálogo predeterminado, [!DNL default.ini]), la marca de agua se aplicará a todas las solicitudes de imagen independientemente de si hacen referencia a un catálogo o no.

Las marcas de agua no se aplican a imágenes devueltas en respuesta a solicitudes de miniaturas ( `req=tmb`) y a ciertas solicitudes de los visualizadores de Dynamic Media.

## Escalado y alineación {#section-89ef9e5926ae438abbd8e70332749b76}

Cuando se especifica una marca de agua, el servidor generará primero la imagen compuesta (la *imagen de destino*) a la que debe aplicarse la marca de agua (antes de aplicar las transformaciones de vista). A continuación, el servidor genera la imagen compuesta para la marca de agua como cualquier otra imagen (la *imagen de marca de agua*).

A diferencia de las imágenes estándar, `sizeN=` puede especificarse para layer=0 o layer=comp de la imagen de marca de agua. Esto permite escalar la imagen de marca de agua en relación con la imagen de destino. Si no se especifica `sizeN=`, la imagen de marca de agua conserva su tamaño de píxel al combinarse con la imagen de destino.

Los comandos de solicitud (como `fmt=`) y los comandos de vista (como `wid=`) se omiten en los registros de marca de agua, con la excepción de `align=`. `align=` se puede utilizar para colocar la imagen de marca de agua en relación con la imagen de marca de agua en relación con la imagen de destino. Esto permite colocar la marca de agua en relación con una esquina o borde de la imagen de destino.

Después de escalar y alinear, el servidor capa la imagen de marca de agua sobre la imagen de destino utilizando los valores `blendMode=` y `opac=` especificados para `layer=0` o `layer=comp` de la imagen de marca de agua. Finalmente, los comandos request y view especificados para la imagen de destino se aplican para construir la imagen de respuesta.

Tenga en cuenta que la imagen de marca de agua nunca se extenderá sobre ningún espacio en blanco agregado a la imagen de respuesta por los comandos `wid=` y `hei=`.

## Ejemplo {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Una marca de agua típica puede consistir en una sencilla imagen RGBA que contenga un logotipo o un aviso de copyright. Creamos un registro en el catálogo de imágenes (o en el catálogo predeterminado) con `catalog::Id` establecido en `watermark` y especificamos el archivo de imagen de marca de agua en `catalog::Path`. Queremos ampliar la marca de agua para ajustarla a la imagen de visualización (sin distorsionar la marca de agua) y dejar un margen adicional, y reducir la opacidad al 20% de la marca de agua original, por lo que establecemos `catalog::Modifier` en `sizeN=0.9,0.9&opac=20`. Para activar la marca de agua, establezca `attribute::Watermark` en el id de la entrada del catálogo de marcas de agua, &quot;marca de agua&quot; en este ejemplo. Es posible que queramos experimentar con diferentes `blendMode=` opciones para lograr diferentes efectos de marca de agua.

## Véase también {#section-4d66713abacb42c7b6a0c93cbf966a97}

[atributo::marca de agua](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
