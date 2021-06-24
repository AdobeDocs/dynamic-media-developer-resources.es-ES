---
description: Las referencias $var$ que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.
solution: Experience Manager
title: Procesamiento de variables en solicitudes externas incrustadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Procesamiento de variables en solicitudes externas incrustadas{#variable-processing-in-embedded-foreign-requests}

Las referencias $var$ que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.

Esto permite colocar las solicitudes externas incrustadas en una plantilla en un catálogo de imágenes.

Los valores de variable que se van a sustituir en solicitudes externas generalmente deben codificarse dos veces, ya que no se aplica ninguna recodificación antes de que el servidor intente transmitir la dirección url externa final.
