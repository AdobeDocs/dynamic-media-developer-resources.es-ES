---
description: El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.
seo-description: El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.
seo-title: Fuentes de imagen externas
solution: Experience Manager
title: Fuentes de imagen externas
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Fuentes de imagen externas{#foreign-image-sources}

El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.

Especificación de una URL externa para un `src=` comando o un `mask=` comando; simplemente delimite toda la dirección URL incrustada con llaves:

` …&src={ *[!DNL foreignUrl]*}&…`

Se permiten direcciones URL absolutas completas (si `attribute::AllowDirectUrls` se establece) y direcciones URL relativas a `attribute::RootUrl` . Se produce un error si se incrusta una dirección URL absoluta y se atribuye el atributo: `AllowDirectUrls` es 0 o si se especifica una dirección URL relativa y `attribute::RootUrl` está vacía.

El servidor almacena en caché las imágenes externas según los encabezados de caché incluidos con la respuesta HTTP.
