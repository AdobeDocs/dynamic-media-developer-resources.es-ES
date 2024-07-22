---
title: Fuentes de imagen externas
description: El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP externos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Fuentes de imagen externas{#foreign-image-sources}

El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP externos.

Para especificar una dirección URL externa para un comando `src=` o `mask=`, simplemente delimite toda la dirección URL incrustada con llaves:

` …&src={ *[!DNL foreignUrl]*}&…`

Se permiten direcciones URL absolutas completas (si se establece `attribute::AllowDirectUrls`) y direcciones URL relativas a `attribute::RootUrl`. Se produce un error si una dirección URL absoluta está incrustada y el atributo: `AllowDirectUrls` es 0, o si se especifica una dirección URL relativa y `attribute::RootUrl` está vacío.

El servidor almacena en caché las imágenes externas según los encabezados de almacenamiento en caché incluidos con la respuesta HTTP.
