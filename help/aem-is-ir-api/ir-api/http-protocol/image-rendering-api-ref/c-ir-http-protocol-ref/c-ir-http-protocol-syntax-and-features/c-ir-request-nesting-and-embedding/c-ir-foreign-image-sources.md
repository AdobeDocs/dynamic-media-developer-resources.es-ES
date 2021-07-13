---
description: El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.
solution: Experience Manager
title: Fuentes de imagen externas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Fuentes de imagen externas{#foreign-image-sources}

El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.

Para especificar una dirección URL externa para un comando `src=` o `mask=`; delimite toda la URL incrustada con llaves:

` …&src={ *[!DNL foreignUrl]*}&…`

Se permiten direcciones URL absolutas completas (si `attribute::AllowDirectUrls` está establecido) y direcciones URL relativas a `attribute::RootUrl`. Se produce un error si se incrusta una dirección URL absoluta y el atributo: `AllowDirectUrls` es 0, o si se especifica una dirección URL relativa y `attribute::RootUrl` está vacía.

El servidor almacena en caché las imágenes externas según los encabezados de almacenamiento en caché incluidos con la respuesta HTTP.
