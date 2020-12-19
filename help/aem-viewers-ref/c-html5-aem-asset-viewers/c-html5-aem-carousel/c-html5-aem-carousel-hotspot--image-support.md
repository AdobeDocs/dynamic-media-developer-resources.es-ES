---
description: nulo
seo-description: nulo
seo-title: Compatibilidad con zonas interactivas y mapas de imagen
solution: Experience Manager
title: Compatibilidad con zonas interactivas y mapas de imagen
topic: Dynamic media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Compatibilidad con puntos interactivos y mapas de imagen{#hotspot-and-image-maps-support}

El visor admite la representación de iconos de zonas interactivas y regiones de mapas de imagen en la parte superior de la vista principal. El aspecto de los iconos y regiones de puntos interactivos se controla mediante CSS, tal como se describe en la sección personalizar zonas interactivas y mapas de imagen.

Consulte [Puntos interactivos y mapas de imagen](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Las zonas interactivas y las regiones pueden activar una función de Vista rápida en la página web de alojamiento activando una llamada de retorno de JavaScript o redireccionando a un usuario a una página web externa.

## Puntos interactivos de Vista rápida {#section-cda48fc9730142d0bb3326bac7df3271}

Estos tipos de zonas interactivas o mapas de imagen deben crearse utilizando el tipo de acción &quot;Vista rápida&quot; en Dynamic Media, de AEM. Cuando un usuario activa una zona interactiva o mapa de imagen, el visor ejecuta la llamada de retorno de JavaScript `quickViewActivate` y le pasa los datos de zona interactiva o mapa de imagen. Se espera que la página web de incrustación escuche esta llamada de retorno. Cuando activa la página, abre su propia implementación de Vista rápida.

## Redirigir a la página Web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Las zonas interactivas o los mapas de imagen creados para el tipo de acción &quot;Vista rápida&quot; en Dynamic Media de AEM redirecciona al usuario a una dirección URL externa. Según la configuración realizada durante la creación, la URL se abre en una nueva ficha del explorador, en la misma ventana o en la ventana del explorador con nombre.
