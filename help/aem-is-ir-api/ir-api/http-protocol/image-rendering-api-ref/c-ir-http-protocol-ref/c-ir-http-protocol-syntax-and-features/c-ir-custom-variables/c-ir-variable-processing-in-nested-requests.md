---
description: Las referencias $var$ pueden ocurrir en cualquier lugar dentro de las llaves de una solicitud de servicio de imágenes o procesamiento de imágenes anidada, incluso a la izquierda de '?' separar la ruta de la consulta.
seo-description: Las referencias $var$ pueden ocurrir en cualquier lugar dentro de las llaves de una solicitud de servicio de imágenes o procesamiento de imágenes anidada, incluso a la izquierda de '?' separar la ruta de la consulta.
seo-title: Procesamiento de variables en solicitudes anidadas
solution: Experience Manager
title: Procesamiento de variables en solicitudes anidadas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# Procesamiento de variables en solicitudes anidadas{#variable-processing-in-nested-requests}

Las referencias $var$ pueden ocurrir en cualquier lugar dentro de las llaves de una solicitud de servicio de imágenes o procesamiento de imágenes anidada, incluso a la izquierda de &#39;?&#39; separar la ruta de la consulta.

El servidor sustituye estas referencias por valores (ya sea de la dirección URL o de `catalog::Modifier` del catálogo de imágenes principal) antes de seguir analizando y procesando la solicitud anidada.

Además, todas las definiciones `$ *[!DNL var]*=` de la dirección URL y `catalog::Modifier` se reenvían a todas las solicitudes anidadas de servicio de imágenes y procesamiento de imágenes. Esto garantiza que todas las definiciones de variables estén disponibles para todas las plantillas, independientemente del nivel de anidación.

Independientemente del nivel de anidación, solo se debe aplicar codificación HTTP de un solo paso a los valores de variables que se van a sustituir en cualquier lugar de las solicitudes anidadas de procesamiento de imágenes o de servicio de imágenes.
