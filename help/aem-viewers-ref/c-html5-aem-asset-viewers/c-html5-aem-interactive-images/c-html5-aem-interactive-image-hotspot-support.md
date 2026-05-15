---
title: Compatibilidad con puntos interactivos
description: Compatibilidad con puntos interactivos
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
TQID: 'https://experienceleague.adobe.com/kvYBwi70uYXIK8D6MeNgZN74h3X6jBfmOLj1SjlKEzs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Compatibilidad con puntos interactivos{#hotspot-support}

El visor admite la renderización de iconos de puntos interactivos en la parte superior de la vista principal. El aspecto de los iconos de puntos interactivos se controla mediante CSS como se describe en la sección Puntos interactivos.

Ver [puntos interactivos](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Los puntos interactivos pueden activar una función de vista rápida en la página web de alojamiento activando una llamada de retorno de JavaScript o redirigir a un usuario a una página web externa.

## Puntos interactivos de Quickview {#section-cda48fc9730142d0bb3326bac7df3271}

Estos tipos de puntos interactivos deben crearse con el tipo de acción &quot;Vista rápida&quot; en Dynamic Media, de Adobe Experience Manager Assets: bajo demanda. Cuando un usuario activa un punto interactivo de este tipo, el visor ejecuta la llamada de retorno de JavaScript `quickViewActivate` y le pasa los datos del punto interactivo. Se espera que la página web de incrustación escuche esta llamada de retorno. Cuando almacena en déclencheur la página, abre su propia implementación de vista rápida.

## Redirigir a página web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Puntos interactivos creados para el tipo de acción &quot;Vista rápida&quot; en Dynamic Media de Experience Manager Assets: On-demand redirige al usuario a una URL externa. Según la configuración realizada durante la creación, la URL se abre en una nueva pestaña del explorador, en la misma ventana o en la ventana denominada del explorador.
