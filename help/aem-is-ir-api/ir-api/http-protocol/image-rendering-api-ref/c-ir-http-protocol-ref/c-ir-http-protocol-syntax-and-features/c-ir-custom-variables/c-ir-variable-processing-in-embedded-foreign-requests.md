---
title: Procesamiento de variables en solicitudes externas incrustadas
description: Las referencias $var$ que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Procesamiento de variables en solicitudes externas incrustadas{#variable-processing-in-embedded-foreign-requests}

Cualquiera `$var$` las referencias que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.

Permite colocar solicitudes externas incrustadas en una plantilla en un catálogo de imágenes.

Los valores de variable que se van a sustituir en solicitudes externas generalmente deben codificarse dos veces, ya que no se aplica ninguna recodificación antes de que el servidor intente transmitir la dirección url externa final.
