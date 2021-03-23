---
description: Compatibilidad con zonas interactivas y mapas de imágenes
solution: Experience Manager
title: Compatibilidad con zonas interactivas y mapas de imágenes
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# Compatibilidad con zonas interactivas y mapas de imágenes{#hotspot-and-image-maps-support}

El visor admite la representación de iconos de zona interactiva y regiones de mapa de imagen en la parte superior de la vista principal. El aspecto de los iconos y regiones de puntos interactivos se controla mediante CSS, tal como se describe en la sección de personalización de puntos interactivos y mapas de imágenes .

Consulte [Puntos interactivos y mapas de imágenes](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Las zonas interactivas y las regiones pueden activar una función de vista rápida en la página web de alojamiento activando una llamada de retorno de JavaScript o redireccionando a un usuario a una página web externa.

## Puntos interactivos de vista rápida {#section-cda48fc9730142d0bb3326bac7df3271}

Estos tipos de zonas interactivas o mapas de imágenes deben crearse utilizando el tipo de acción &quot;Vista rápida&quot; en Dynamic Media, de AEM. Cuando un usuario activa una zona interactiva o mapa de imagen, el visor ejecuta la llamada de retorno de JavaScript `quickViewActivate` y le pasa los datos de zona interactiva o mapa de imagen. Se espera que la página web de incrustación escuche esta llamada de retorno. Cuando déclencheur la página, abre su propia implementación de vista rápida.

## Redirigir a una página web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Puntos interactivos o mapas de imágenes creados para el tipo de acción &quot;Vista rápida&quot; en Dynamic Media de AEM redirige al usuario a una URL externa. Según la configuración realizada durante la creación, la dirección URL se abre en una nueva pestaña del explorador, en la misma ventana o en la ventana del explorador con nombre.
