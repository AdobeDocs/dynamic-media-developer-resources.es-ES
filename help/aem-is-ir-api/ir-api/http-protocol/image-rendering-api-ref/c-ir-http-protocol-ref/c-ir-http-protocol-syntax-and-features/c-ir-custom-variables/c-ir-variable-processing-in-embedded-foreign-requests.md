---
description: Las referencias $var$ que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.
seo-description: Las referencias $var$ que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.
seo-title: Procesamiento de variables en solicitudes externas incrustadas
solution: Experience Manager
title: Procesamiento de variables en solicitudes externas incrustadas
topic: Scene7 Image Serving - Image Rendering API
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Procesamiento de variables en solicitudes externas incrustadas{#variable-processing-in-embedded-foreign-requests}

Las referencias $var$ que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.

Esto permite colocar solicitudes externas incrustadas en una plantilla en un catálogo de imágenes.

Los valores de variable que se van a sustituir en solicitudes externas generalmente deben tener codificación de doble, ya que no se aplica ninguna recodificación antes de que el servidor intente transmitir la dirección URL externa final.
