---
title: Fuentes de imagen externas
description: El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# Fuentes de imagen externas{#foreign-image-sources}

El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP extranjeros.

Para especificar una dirección URL externa para un `src=` o `mask=` comando; delimite toda la URL incrustada con llaves:

` …&src={ *[!DNL foreignUrl]*}&…`

Direcciones URL absolutas completas (si `attribute::AllowDirectUrls` está configurado) y las direcciones URL relativas a `attribute::RootUrl` están permitidos. Se produce un error si se incrusta una dirección URL absoluta y el atributo: `AllowDirectUrls` es 0, o si se especifica una dirección URL relativa y `attribute::RootUrl` está vacío.

El servidor almacena en caché las imágenes externas según los encabezados de almacenamiento en caché incluidos con la respuesta HTTP.
