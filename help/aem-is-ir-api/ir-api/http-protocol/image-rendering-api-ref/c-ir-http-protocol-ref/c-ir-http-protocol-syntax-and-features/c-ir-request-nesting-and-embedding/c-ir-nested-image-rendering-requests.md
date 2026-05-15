---
title: Solicitudes de procesamiento de imágenes anidadas
description: Para aplicaciones avanzadas, es posible utilizar el resultado de una operación de procesamiento como imagen material, al igual que una imagen obtenida del servicio de imágenes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
TQID: 'https://experienceleague.adobe.com/Fqiu-HsaRtrWMjBQudUBzr1iu3WLg7173Kf-71ikejI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Solicitudes de procesamiento de imágenes anidadas{#nested-image-rendering-requests}

Para aplicaciones avanzadas, es posible utilizar el resultado de una operación de procesamiento como imagen material, al igual que una imagen obtenida del servicio de imágenes.

Una solicitud de procesamiento se puede utilizar como imagen material especificándola en el comando `src=` de la siguiente manera:

` …&src=ir{ *[!DNL renderRequest]*}&…`

El token `ir` distingue entre mayúsculas y minúsculas.

La solicitud anidada no debe incluir la ruta raíz del procesamiento de imágenes (normalmente `http:// *[!DNL server]*/ir/render/'`), pero puede incluir tokens de reglas de preprocesamiento.

Los siguientes comandos se omiten cuando se especifican en solicitudes anidadas (en la dirección URL de la solicitud o en `catalog::Modifier` o `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

También se omiten `attribute::MaxPix` y `attribute::DefaultPix` del catálogo de materiales que se aplica a la solicitud de procesamiento anidada.

El resultado de imagen de una solicitud IR anidada se puede almacenar en caché de manera opcional incluyendo `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está deshabilitado. El almacenamiento en caché solo debe habilitarse cuando la imagen intermedia se reutilice en una solicitud diferente en un período de tiempo razonable. Se aplica la administración de caché estándar del lado del servidor. Los datos se almacenan en caché en un formato sin pérdidas.
