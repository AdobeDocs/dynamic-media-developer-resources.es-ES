---
title: Solicitudes de renderización de imágenes anidadas
description: Para aplicaciones avanzadas, es posible utilizar el resultado de una operación de renderización como imagen material, al igual que una imagen obtenida de Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Solicitudes de renderización de imágenes anidadas{#nested-image-rendering-requests}

Para aplicaciones avanzadas, es posible utilizar el resultado de una operación de renderización como imagen material, al igual que una imagen obtenida de Image Serving.

Una solicitud de renderización puede utilizarse como imagen material especificándola en la variable `src=` como se indica a continuación:

` …&src=ir{ *[!DNL renderRequest]*}&…`

La variable `ir` distingue entre mayúsculas y minúsculas.

La solicitud anidada no debe incluir la ruta raíz de renderización de imágenes (normalmente `http:// *[!DNL server]*/ir/render/'`), pero puede incluir tokens de reglas de preprocesamiento.

Los siguientes comandos se omiten cuando se especifican en solicitudes anidadas (ya sea en la url de la solicitud o en `catalog::Modifier` o `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

También se ignoran `attribute::MaxPix` y `attribute::DefaultPix` del catálogo de materiales que se aplica a la solicitud de procesamiento anidada.

El resultado de la imagen de una solicitud IR anidada se puede almacenar en caché de forma opcional incluyendo `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está deshabilitado. El almacenamiento en caché solo debe habilitarse cuando la imagen intermedia se reutiliza en una solicitud diferente en un periodo de tiempo razonable. Se aplica la administración estándar de caché del lado del servidor. Los datos se almacenan en caché en un formato sin pérdidas.
