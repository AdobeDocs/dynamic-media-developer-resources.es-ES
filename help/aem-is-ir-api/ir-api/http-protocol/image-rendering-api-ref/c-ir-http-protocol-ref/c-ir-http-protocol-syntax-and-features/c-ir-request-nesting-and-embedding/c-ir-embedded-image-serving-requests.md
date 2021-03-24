---
description: Una solicitud de Image Server (IS) puede utilizarse como imagen material.
solution: Experience Manager
title: Solicitudes del servidor de imágenes incrustadas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Solicitudes del servidor de imágenes incrustadas{#embedded-image-server-requests}

Una solicitud de Image Server (IS) puede utilizarse como imagen material.

Especifique la solicitud en el comando `src=` de la siguiente manera:

` …&src=is( *[!DNL imageServingRequest]*)&…`

El token `is` distingue entre mayúsculas y minúsculas.

La solicitud anidada no debe incluir la ruta raíz de Image Serving (normalmente [!DNL http:// *[!DNL server]*/is/image/&quot;]), pero puede incluir tokens de reglas de preprocesamiento.

Los siguientes comandos IS se omiten cuando se especifican en solicitudes anidadas (ya sea en la dirección URL de la solicitud o en `catalog::Modifier` o `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

También se ignoran `attribute::MaxPix` y `attribute::DefaultPix` del catálogo de imágenes que se aplica a la solicitud IS incrustada.

Si la imagen de resultado de la solicitud anidada incluye datos de máscara (alfa), siempre se pasa al material. Utilice una capa de imagen de fondo de color sólido para evitar alfa no deseado.

El resultado de la imagen de una solicitud IS incrustada se puede almacenar en caché de forma opcional incluyendo `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está deshabilitado. El almacenamiento en caché solo debe habilitarse cuando se espera que la imagen intermedia se reutilice en una solicitud diferente en un periodo de tiempo razonable. Se aplica la administración estándar de caché del lado del servidor. Los datos se almacenan en caché en un formato sin pérdidas.
