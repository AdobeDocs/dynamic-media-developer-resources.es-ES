---
description: Las referencias $var$ que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.
seo-description: Las referencias $var$ que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.
seo-title: Procesamiento de variables en solicitudes externas incrustadas
solution: Experience Manager
title: Procesamiento de variables en solicitudes externas incrustadas
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# Procesamiento de variables en solicitudes externas incrustadas{#variable-processing-in-embedded-foreign-requests}

Las referencias $var$ que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.

Esto permite colocar las solicitudes externas incrustadas en una plantilla en un catálogo de imágenes.

Los valores de variable que se van a sustituir en solicitudes externas generalmente deben codificarse dos veces, ya que no se aplica ninguna recodificación antes de que el servidor intente transmitir la dirección url externa final.
