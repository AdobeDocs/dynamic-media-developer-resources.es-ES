---
description: El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.
seo-description: El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.
seo-title: Fuentes de imagen externas
solution: Experience Manager
title: Fuentes de imagen externas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Fuentes de imagen externas{#foreign-image-sources}

El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.

Para especificar una dirección URL externa para un comando `src=` o `mask=`; simplemente delimite toda la dirección URL incrustada con llaves:

` …&src={ *[!DNL foreignUrl]*}&…`

Se permiten direcciones URL absolutas completas (si `attribute::AllowDirectUrls` está establecido) y direcciones URL relativas a `attribute::RootUrl`. Se produce un error si se incrusta una dirección URL absoluta y se atribuye el atributo: `AllowDirectUrls` es 0, o si se especifica una dirección URL relativa y `attribute::RootUrl` está vacía.

El servidor almacena en caché las imágenes externas según los encabezados de caché incluidos con la respuesta HTTP.
