---
title: Procesamiento de variables en solicitudes anidadas
description: Las referencias $var$ pueden ocurrir en cualquier lugar dentro de las llaves de una solicitud anidada de servicio de imágenes o renderización de imágenes, incluso a la izquierda de '?' separar la ruta de acceso de la consulta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Procesamiento de variables en solicitudes anidadas{#variable-processing-in-nested-requests}

Las referencias $var$ pueden ocurrir en cualquier lugar dentro de las llaves de una solicitud anidada de servicio de imágenes o renderización de imágenes, incluso a la izquierda de &#39;?&#39; separar la ruta de acceso de la consulta.

El servidor sustituye estas referencias por valores (ya sea de la dirección url o de `catalog::Modifier` del catálogo de imágenes principal) antes de seguir analizando y procesando la solicitud anidada.

Además, todas las `$ *[!DNL var]*=` definiciones de la dirección url y `catalog::Modifier` se reenvían a todas las solicitudes anidadas de Image Serving y Image Rendering. Al hacerlo, se garantiza que todas las definiciones de variables estén disponibles para todas las plantillas, independientemente del nivel de anidación.

Independientemente del nivel de anidación, solo se debe aplicar una codificación HTTP de un solo paso a los valores de las variables que se van a sustituir en cualquier lugar de las solicitudes anidadas de renderización de imágenes o servicio de imágenes.
