---
description: El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.
solution: Experience Manager
title: Fuentes de imagen externas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Fuentes de imagen externas{#foreign-image-sources}

El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.

Para especificar una dirección URL externa para un comando `src=` o `mask=`; delimite toda la URL incrustada con llaves:

` …&src={ *[!DNL foreignUrl]*}&…`

Se permiten direcciones URL absolutas completas (si `attribute::AllowDirectUrls` está establecido) y direcciones URL relativas a `attribute::RootUrl`. Se produce un error si se incrusta una dirección URL absoluta y el atributo: `AllowDirectUrls` es 0, o si se especifica una dirección URL relativa y `attribute::RootUrl` está vacía.

El servidor almacena en caché las imágenes externas según los encabezados de almacenamiento en caché incluidos con la respuesta HTTP.
