---
description: El servicio de imágenes implementa una función visual simple de marca de agua.
solution: Experience Manager
title: Filigranas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Filigranas{#watermarks}

El servicio de imágenes implementa una función visual simple de marca de agua.

Una marca de agua suele ser una imagen semitransparente, pero puede ser texto o una imagen compuesta de capas más compleja. El servidor coloca la marca de agua sobre la imagen de respuesta después de todos los atributos de vista ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) se han aplicado.

La marca de agua se habilita al establecer `attribute::Watermark` a una entrada de catálogo válida que contenga la imagen o plantilla de marca de agua. If `attribute::Watermark` se establece en un catálogo con nombre, el servidor agrega la marca de agua a todas las solicitudes de imagen que hacen referencia al id de catálogo en la dirección URL de la solicitud. If `default::Watermark` se ha definido (en el catálogo predeterminado, [!DNL default.ini]), la marca de agua se aplica a todas las solicitudes de imagen independientemente de si hacen referencia a un catálogo o no.

Las marcas de agua no se aplican a las imágenes devueltas como respuesta a las solicitudes de miniaturas ( `req=tmb`) y ciertas solicitudes de los visualizadores de Dynamic Media.

## Escala y alineación {#section-89ef9e5926ae438abbd8e70332749b76}

Cuando se especifica una marca de agua, el servidor genera primero la imagen compuesta (la variable *imagen de destino*) al que debe aplicarse la marca de agua (antes de aplicar las transformaciones de vista). A continuación, el servidor genera la imagen compuesta para la marca de agua como cualquier otra imagen (la *imagen de filigrana*).

A diferencia de las imágenes estándar, `sizeN=` se puede especificar para layer=0 o layer=comp de la imagen de marca de agua. Esto permite escalar la imagen de marca de agua en relación con la imagen de destino. If `sizeN=` no se ha especificado, la imagen de marca de agua mantiene su tamaño de píxel al combinarse con la imagen de destino.

Solicitar comandos (como `fmt=`) y comandos de vista (como `wid=`) se omiten en los registros de marca de agua, excepto en `align=`. `align=` se puede utilizar para colocar la imagen de marca de agua en relación con la imagen de marca de agua en relación con la imagen de destino. Esto permite colocar la marca de agua en relación con una esquina o borde de la imagen de destino.

Después de escalar y alinear, el servidor coloca la imagen de marca de agua en la imagen de destino con la variable `blendMode=` y `opac=` valores especificados para `layer=0` o `layer=comp` de la imagen de marca de agua. Por último, los comandos de solicitud y visualización especificados para la imagen de destino se aplican para construir la imagen de respuesta.

Tenga en cuenta que la imagen de marca de agua nunca se extiende sobre ningún espacio en blanco agregado a la imagen de respuesta por el `wid=` y `hei=` comandos.

## Ejemplo {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Una marca de agua típica puede consistir en una imagen RGBA simple que contiene un logotipo o un aviso de copyright. Creamos un registro en el catálogo de imágenes (o el catálogo predeterminado) con `catalog::Id` establezca en `watermark` y especifique el archivo de imagen de marca de agua en `catalog::Path`. Queremos ampliar la marca de agua para que se ajuste a la imagen de la vista (sin distorsionar la marca de agua) dejando un poco de margen adicional y reducir la opacidad al 20% de la marca de agua original, por lo que establecemos `catalog::Modifier` hasta `sizeN=0.9,0.9&opac=20`. Para activar la marca de agua, establezca `attribute::Watermark` al id de la entrada de catálogo de marcas de agua, &quot;watermark&quot; en este ejemplo. Podríamos querer experimentar con diferentes `blendMode=` opciones para lograr diferentes efectos de marca de agua.

## Véase también {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Filigrana](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
