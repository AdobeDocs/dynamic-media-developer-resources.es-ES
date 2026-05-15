---
description: Esta versión (Image Serving 6.6.1 e Image Rendering 6.6.1) reemplaza a Image Serving 6.5.3 y Image Rendering 6.5.3.
solution: Experience Manager
title: Acerca de esta versión
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
TQID: 'https://experienceleague.adobe.com/Mv84kHB7jsBYAvY1j--l8Ly5VZtKwFq-SsNdz2TIQOE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 1%

---

# Acerca de esta versión{#about-this-release}

Esta versión (Image Serving 6.6.1 e Image Rendering 6.6.1) reemplaza a Image Serving 6.5.3 y Image Rendering 6.5.3.

## Problemas conocidos y cambios de comportamiento {#section-9dbc05206187477f926a78e8108a34e1}

* Ya no se admite el uso del carácter de signo de interrogación en los ID de recurso, aunque el carácter tenga codificación URL.
* Las solicitudes del titular dinámico `/xfl/flash/` ya no son compatibles y ahora devuelven un código de error HTTP 404.
* Ya no se admiten las solicitudes W2P `/is/agm/`.
* Algunos mensajes de error ya no se representan en el explorador. Como tal, debe revisar el registro de seguimiento para depurarlo.

## Nuevas características {#section-b1386e36cb4544ebb79766a06b16842d}

* Muestra inteligente
* Recorte inteligente

## Corrección de errores {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Se corrigió un problema en el cual la opción RTF `\qc` seguida de un espacio provocaba que una solicitud no se procesara.
