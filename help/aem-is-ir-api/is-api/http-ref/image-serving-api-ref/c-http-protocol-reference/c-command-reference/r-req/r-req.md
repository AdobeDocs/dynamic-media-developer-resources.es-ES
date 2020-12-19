---
description: Tipo de solicitud. Especifica el tipo de solicitud.
seo-description: Tipo de solicitud. Especifica el tipo de solicitud.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 16%

---


# req{#req}

Tipo de solicitud. Especifica el tipo de solicitud.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`opciones`*]`

* [catalogprops](r-catalogprops.md)
* [existe](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [mapa](r-map-req.md)
* [máscara](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [mensaje](r-message.md)
* [props](r-props.md)
* [resolver](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [ajustar](r-set.md)
* [objetivo](r-targets.md)
* [tmb](r-tmb.md)
* [userdata](r-userdata.md)
* [validar](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

A menos que se indique lo contrario en las descripciones detalladas, el servidor devolverá `text` respuestas con tipo MIME `text/plain`. Muchos tipos de solicitud permiten especificar un tipo de respuesta, como `text`, que es generalmente el predeterminado, `javascript`, `xml` o `json`. Los tipos MIME de respuesta asociados son `text/plain`, `text/javascript`, `text/xml` y `text/javascript`, respectivamente.

A menos que se indique lo contrario, las respuestas dan formato a la respuesta como un conjunto de pares `name=value`.

Consulte [Propiedades](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
