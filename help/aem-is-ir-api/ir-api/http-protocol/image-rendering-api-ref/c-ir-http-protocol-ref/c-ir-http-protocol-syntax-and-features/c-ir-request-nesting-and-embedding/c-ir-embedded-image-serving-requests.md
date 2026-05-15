---
title: Solicitudes del servidor de imágenes incrustadas
description: Se puede utilizar una solicitud de Image Server (IS) como imagen material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
TQID: 'https://experienceleague.adobe.com/dt-baBh9jAyJdjqopFR3AoqRvz5zqLzi8B3SnE04xEs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Solicitudes del servidor de imágenes incrustadas{#embedded-image-server-requests}

Se puede utilizar una solicitud de Image Server (IS) como imagen material.

Especifique la solicitud en el comando `src=` de la siguiente manera:

` …&src=is( *[!DNL imageServingRequest]*)&…`

El token `is` distingue entre mayúsculas y minúsculas.

La solicitud anidada no debe incluir la ruta raíz del servicio de imágenes (normalmente  [!DNL http:// *[!DNL server]*/is/image/"]), pero puede incluir tokens de reglas de preprocesamiento.

Los siguientes comandos IS se omiten cuando se especifican en solicitudes anidadas (en la dirección URL de la solicitud o en `catalog::Modifier` o `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

También se omiten `attribute::MaxPix` y `attribute::DefaultPix` del catálogo de imágenes que se aplica a la solicitud de IS incrustada.

Si la imagen de resultado de la solicitud anidada incluye datos de máscara (alfa), siempre se pasa al material. Utilice una capa de imagen de fondo de color sólido para evitar alfa no deseados.

El resultado de imagen de una solicitud IS incrustada se puede almacenar en caché de manera opcional incluyendo `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está deshabilitado. El almacenamiento en caché solo debe habilitarse cuando la imagen intermedia se reutilice en una solicitud diferente en un período de tiempo razonable. Se aplica la administración de caché estándar del lado del servidor. Los datos se almacenan en caché en un formato sin pérdidas.
