---
description: Esta versión (Image Serving 6.6.1 e Image Rendering 6.6.1) reemplaza a Image Serving 6.5.3 y Image Rendering 6.5.3.
solution: Experience Manager
title: Acerca de esta versión
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---

# Acerca de esta versión{#about-this-release}

Esta versión (Image Serving 6.6.1 e Image Rendering 6.6.1) reemplaza a Image Serving 6.5.3 y Image Rendering 6.5.3.

## Problemas conocidos y cambios de comportamiento {#section-9dbc05206187477f926a78e8108a34e1}

* Ya no se admite el uso del carácter de signo de interrogación en los ID de recurso, aunque el carácter tenga codificación URL.
* Titular dinámico `/xfl/flash/` Las solicitudes de ya no son compatibles y ahora devuelven un código de error http 404.
* W2P `/is/agm/` Las solicitudes de ya no son compatibles.
* Algunos mensajes de error ya no se representan en el explorador. Como tal, debe revisar el registro de seguimiento para depurarlo.

## Nuevas características {#section-b1386e36cb4544ebb79766a06b16842d}

* Muestra inteligente
* Recorte inteligente

## Corrección de errores {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Se ha corregido un problema por el que `\qc` La opción RTF seguida de un espacio hizo que una solicitud no se procesara.
