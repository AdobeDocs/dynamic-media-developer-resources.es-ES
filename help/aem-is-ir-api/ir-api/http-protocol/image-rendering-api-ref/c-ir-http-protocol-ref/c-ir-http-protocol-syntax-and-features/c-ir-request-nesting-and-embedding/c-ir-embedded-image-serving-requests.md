---
description: Una solicitud de Image Server (IS) puede utilizarse como imagen material.
seo-description: Una solicitud de Image Server (IS) puede utilizarse como imagen material.
seo-title: Solicitudes del servidor de imágenes incrustadas
solution: Experience Manager
title: Solicitudes del servidor de imágenes incrustadas
topic: Scene7 Image Serving - Image Rendering API
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Solicitudes del servidor de imágenes integrado{#embedded-image-server-requests}

Una solicitud de Image Server (IS) puede utilizarse como imagen material.

Especifique la solicitud en el comando `src=` de la siguiente manera:

` …&src=is( *[!DNL imageServingRequest]*)&…`

El token `is` distingue entre mayúsculas y minúsculas.

La solicitud anidada no debe incluir la ruta raíz del servicio de imágenes (generalmente [!DNL http:// *[!DNL server]*/is/image/&quot;]), pero puede incluir tokens de reglas de preprocesamiento.

Los siguientes comandos IS se omiten cuando se especifican en solicitudes anidadas (ya sea en la dirección URL de la solicitud o en `catalog::Modifier` o `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

También se omiten `attribute::MaxPix` y `attribute::DefaultPix` del catálogo de imágenes que se aplica a la solicitud IS incrustada.

Si la imagen resultante de la solicitud anidada incluye datos de máscara (alfa), siempre se pasa al material. Utilice una capa de imagen de fondo de color sólido para evitar el alfa no deseado.

El resultado de la imagen de una solicitud IS incrustada se puede almacenar en caché de forma opcional mediante la inclusión de `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está desactivado. El almacenamiento en caché solo debe habilitarse cuando se espera que la imagen intermedia se reutilice en una solicitud diferente dentro de un período de tiempo razonable. Se aplica la administración estándar de caché del lado del servidor. Los datos se almacenan en caché en un formato sin pérdida.
