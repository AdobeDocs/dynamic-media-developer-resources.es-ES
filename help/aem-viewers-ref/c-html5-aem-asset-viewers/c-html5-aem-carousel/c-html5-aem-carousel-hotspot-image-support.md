---
title: Compatibilidad con puntos interactivos y mapas de imagen
description: Compatibilidad con puntos interactivos y mapas de imagen
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 8d5dbc2d2b5e228f8496fd71633bf1cb96218226
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Compatibilidad con puntos interactivos y mapas de imagen{#hotspot-and-image-maps-support}

El visor admite la renderización de iconos de puntos interactivos y regiones de mapa de imagen en la parte superior de la vista principal. El aspecto de los iconos y las regiones de los puntos interactivos se controla mediante CSS, tal como se describe en la sección Personalización de puntos interactivos y mapas de imagen.

Ver [puntos interactivos y mapas de imagen](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Los puntos interactivos y las regiones pueden activar una función de vista rápida en la página web de alojamiento activando una llamada de retorno de JavaScript o redireccionando a un usuario a una página web externa.

## Puntos interactivos de Quickview {#section-cda48fc9730142d0bb3326bac7df3271}

Estos tipos de puntos interactivos o mapas de imagen deben crearse con el tipo de acción &quot;Vista rápida&quot; en Dynamic Media, de Adobe Experience Manager. Cuando un usuario activa un punto interactivo o un mapa de imagen de este tipo, el visor ejecuta la llamada de retorno de JavaScript `quickViewActivate` y le pasa los datos del punto interactivo o del mapa de imagen. Se espera que la página web de incrustación escuche esta llamada de retorno. Cuando almacena en déclencheur la página, abre su propia implementación de vista rápida.

## Redirigir a página web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Los puntos interactivos o los mapas de imagen creados para el tipo de acción &quot;Vista rápida&quot; en Dynamic Media de Experience Manager redirigen al usuario a una URL externa. Según la configuración realizada durante la creación, la URL se abre en una nueva pestaña del explorador, en la misma ventana o en la ventana denominada del explorador.
