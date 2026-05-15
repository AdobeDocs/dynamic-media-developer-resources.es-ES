---
description: Tipo de solicitud. Especifica el tipo de solicitud.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
TQID: 'https://experienceleague.adobe.com/-WzHmELeamQBbVFlzXNKbDE3fKVXw4x6pSoEz0LHav4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 10%

---

# req{#req}

Tipo de solicitud. Especifica el tipo de solicitud.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`opciones`*]`

* [catalogprops](r-catalogprops.md)
* [existe](r-exists.md)
* [imageprops](r-imageprops.md)
* [conjunto de imágenes](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [mapa](r-map-req.md)
* [enmascarar](r-mask-req.md)
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

A menos que se indique lo contrario en las descripciones detalladas, el servidor devuelve `text` respuestas con el tipo MIME `text/plain`. Muchos tipos de solicitud le permiten especificar un tipo de respuesta, como `text`, que suele ser el tipo predeterminado: `javascript`, `xml` o `json`. Los tipos MIME de respuesta asociados son `text/plain`, `text/javascript`, `text/xml` y `text/javascript`, respectivamente.

A menos que se indique lo contrario, las respuestas dan formato a la respuesta como un conjunto de `name=value` pares.

Ver [Propiedades](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
