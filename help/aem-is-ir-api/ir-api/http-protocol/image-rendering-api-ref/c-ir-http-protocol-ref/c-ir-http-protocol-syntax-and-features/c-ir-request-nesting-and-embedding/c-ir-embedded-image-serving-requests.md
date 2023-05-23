---
title: Solicitudes del servidor de imágenes incrustadas
description: Se puede utilizar una solicitud de Image Server (IS) como imagen material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Solicitudes del servidor de imágenes incrustadas{#embedded-image-server-requests}

Se puede utilizar una solicitud de Image Server (IS) como imagen material.

Especifique la solicitud en la `src=` como se indica a continuación:

` …&src=is( *[!DNL imageServingRequest]*)&…`

El `is` distingue entre mayúsculas y minúsculas.

La solicitud anidada no debe incluir la ruta raíz del servicio de imágenes (normalmente, [!DNL http:// *[!DNL server]*/is/image/"]), pero puede incluir tokens de reglas de preprocesamiento.

Los siguientes comandos IS se omiten cuando se especifican en solicitudes anidadas (en la dirección URL de la solicitud o en `catalog::Modifier` o `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

También se ignoran `attribute::MaxPix` y `attribute::DefaultPix` del catálogo de imágenes que se aplica a la solicitud de IS incrustada.

Si la imagen de resultado de la solicitud anidada incluye datos de máscara (alfa), siempre se pasa al material. Utilice una capa de imagen de fondo de color sólido para evitar alfa no deseados.

El resultado de imagen de una solicitud IS incrustada se puede almacenar en caché de forma opcional incluyendo `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está deshabilitado. El almacenamiento en caché solo debe habilitarse cuando la imagen intermedia se reutilice en una solicitud diferente en un período de tiempo razonable. Se aplica la administración de caché estándar del lado del servidor. Los datos se almacenan en caché en un formato sin pérdidas.
