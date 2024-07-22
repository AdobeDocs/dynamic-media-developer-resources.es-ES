---
title: Procesamiento de variables en solicitudes anidadas
description: Las referencias $var$ pueden producirse en cualquier lugar dentro de las llaves de una solicitud de servicio o procesamiento de imágenes anidada, incluso a la izquierda de "?" separar la ruta de la consulta.
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

Las referencias $var$ pueden producirse en cualquier lugar dentro de las llaves de una solicitud de servicio o procesamiento de imágenes anidada, incluso a la izquierda de &quot;?&quot; separar la ruta de la consulta.

El servidor sustituye estas referencias por valores (desde la dirección URL o desde `catalog::Modifier` del catálogo de imágenes principal) antes de analizar y procesar más la solicitud anidada.

Además, todas las definiciones de `$ *[!DNL var]*=` de la dirección URL y `catalog::Modifier` se reenvían a todas las solicitudes anidadas de servicio y procesamiento de imágenes. Al hacerlo, se asegura de que todas las definiciones de variables estén disponibles para todas las plantillas, independientemente del nivel de anidación.

Independientemente del nivel de anidamiento, solo se debe aplicar la codificación HTTP de un solo paso a los valores de variable que se van a sustituir en cualquier lugar de las solicitudes anidadas de Image Rendering o Image Serving.
