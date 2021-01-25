---
description: Para aplicaciones avanzadas es posible utilizar el resultado de una operación de procesamiento como imagen material, al igual que una imagen obtenida del servicio de imágenes.
seo-description: Para aplicaciones avanzadas es posible utilizar el resultado de una operación de procesamiento como imagen material, al igual que una imagen obtenida del servicio de imágenes.
seo-title: Solicitudes de procesamiento de imágenes anidadas
solution: Experience Manager
title: Solicitudes de procesamiento de imágenes anidadas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# Solicitudes de procesamiento de imágenes anidadas{#nested-image-rendering-requests}

Para aplicaciones avanzadas es posible utilizar el resultado de una operación de procesamiento como imagen material, al igual que una imagen obtenida del servicio de imágenes.

Una solicitud de procesamiento se puede utilizar como imagen material especificándola en el comando `src=` de la siguiente manera:

` …&src=ir{ *[!DNL renderRequest]*}&…`

El token `ir` distingue entre mayúsculas y minúsculas.

La solicitud anidada no debe incluir la ruta raíz de procesamiento de imágenes (generalmente `http:// *[!DNL server]*/ir/render/'`), pero puede incluir tokens de reglas de preprocesamiento.

Los siguientes comandos se omiten cuando se especifican en solicitudes anidadas (ya sea en la dirección URL de la solicitud o en `catalog::Modifier` o `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

También se omiten `attribute::MaxPix` y `attribute::DefaultPix` del catálogo de materiales que se aplica a la solicitud de procesamiento anidada.

El resultado de la imagen de una solicitud IR anidada se puede almacenar en caché de forma opcional mediante `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está desactivado. El almacenamiento en caché solo debe habilitarse cuando se espera que la imagen intermedia se reutilice en una solicitud diferente dentro de un período de tiempo razonable. Se aplica la administración estándar de caché del lado del servidor. Los datos se almacenan en caché en un formato sin pérdida.
