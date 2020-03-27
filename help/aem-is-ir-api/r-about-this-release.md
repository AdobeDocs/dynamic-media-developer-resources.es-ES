---
description: Esta versión (servicio de imágenes 6.6.1 y procesamiento de imágenes 6.6.1) sustituye a servicio de imágenes 6.5.3 y procesamiento de imágenes 6.5.3.
seo-description: Esta versión (servicio de imágenes 6.6.1 y procesamiento de imágenes 6.6.1) sustituye a servicio de imágenes 6.5.3 y procesamiento de imágenes 6.5.3.
seo-title: Acerca de esta versión
solution: Experience Manager
title: Acerca de esta versión
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Acerca de esta versión{#about-this-release}

Esta versión (servicio de imágenes 6.6.1 y procesamiento de imágenes 6.6.1) sustituye a servicio de imágenes 6.5.3 y procesamiento de imágenes 6.5.3.

## Problemas conocidos y cambios de comportamiento {#section-9dbc05206187477f926a78e8108a34e1}

* Ya no se admite el uso del carácter de signo de interrogación en los ID de recursos, aunque el carácter esté codificado en la dirección URL.
* Las solicitudes de letreros `/xfl/flash/` dinámicos ya no son compatibles y ahora devuelven un código de error http 404.
* Ya no se admiten solicitudes W2P `/is/agm/` .
* Algunos mensajes de error ya no se representan en el explorador. Como tal, debe revisar el registro de seguimiento para depurar.

## Nuevas características {#section-b1386e36cb4544ebb79766a06b16842d}

* Muestra inteligente
* Recorte inteligente

## Corrección de errores {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Se ha solucionado el problema de la opción `\qc` RTF seguida de un espacio que impedía procesar una solicitud.

