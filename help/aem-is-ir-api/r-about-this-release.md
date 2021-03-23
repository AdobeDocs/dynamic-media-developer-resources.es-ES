---
description: Esta versión (Image Serving 6.6.1 y Image Rendering 6.6.1) sustituye a Image Serving 6.5.3 y Image Rendering 6.5.3.
seo-description: Esta versión (Image Serving 6.6.1 y Image Rendering 6.6.1) sustituye a Image Serving 6.5.3 y Image Rendering 6.5.3.
seo-title: Acerca de esta versión
solution: Experience Manager
title: Acerca de esta versión
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# Acerca de esta versión{#about-this-release}

Esta versión (Image Serving 6.6.1 y Image Rendering 6.6.1) sustituye a Image Serving 6.5.3 y Image Rendering 6.5.3.

## Problemas conocidos y cambios de comportamiento {#section-9dbc05206187477f926a78e8108a34e1}

* Ya no se admite el uso del carácter de signo de interrogación en los ID de recurso, aunque el carácter esté codificado con la dirección URL.
* Las solicitudes de banner dinámico `/xfl/flash/` ya no son compatibles y ahora devuelven un código de error http 404.
* Las solicitudes W2P `/is/agm/` ya no son compatibles.
* Algunos mensajes de error ya no se representan en el explorador. Como tal, debe revisar el registro de seguimiento para depurar.

## Nuevas características {#section-b1386e36cb4544ebb79766a06b16842d}

* Muestra inteligente
* Recorte inteligente

## Corrección de errores {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Se ha corregido un problema por el que la opción RTF `\qc` seguida de un espacio provocaba que una solicitud no se procesara.

