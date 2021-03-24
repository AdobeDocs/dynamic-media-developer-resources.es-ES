---
description: Las referencias $var$ pueden ocurrir en cualquier lugar dentro de las llaves de una solicitud anidada de servicio de imágenes o renderización de imágenes, incluso a la izquierda de '?' separar la ruta de acceso de la consulta.
solution: Experience Manager
title: Procesamiento de variables en solicitudes anidadas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# Procesamiento de variables en solicitudes anidadas{#variable-processing-in-nested-requests}

Las referencias $var$ pueden ocurrir en cualquier lugar dentro de las llaves de una solicitud anidada de servicio de imágenes o renderización de imágenes, incluso a la izquierda de &#39;?&#39; separar la ruta de acceso de la consulta.

El servidor sustituye estas referencias por valores (ya sea de la dirección url o de `catalog::Modifier` del catálogo de imágenes principal) antes de seguir analizando y procesando la solicitud anidada.

Además, todas las definiciones `$ *[!DNL var]*=` de la dirección url y `catalog::Modifier` se reenvían a todas las solicitudes anidadas de servicio de imágenes y renderización de imágenes. Esto garantiza que todas las definiciones de variables estén disponibles para todas las plantillas, independientemente del nivel de anidación.

Independientemente del nivel de anidación, solo se debe aplicar una codificación HTTP de un solo paso a los valores de las variables que se van a sustituir en cualquier lugar de las solicitudes anidadas de renderización de imágenes o servicio de imágenes.
