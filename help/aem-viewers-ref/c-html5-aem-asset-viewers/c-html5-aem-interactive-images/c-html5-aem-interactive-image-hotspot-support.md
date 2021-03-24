---
description: Compatibilidad con puntos interactivos
solution: Experience Manager
title: Compatibilidad con puntos interactivos
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Compatibilidad con puntos interactivos{#hotspot-support}

El visor admite la renderización de iconos de zonas interactivas en la parte superior de la vista principal. El aspecto de los iconos de zona interactiva se controla mediante CSS, tal como se describe en la sección Puntos interactivos .

Consulte [Puntos interactivos](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Las zonas interactivas pueden activar una función de vista rápida en la página web de alojamiento activando una llamada de retorno de JavaScript o redireccionando a un usuario a una página web externa.

## Puntos interactivos de vista rápida {#section-cda48fc9730142d0bb3326bac7df3271}

Estos tipos de puntos interactivos deben crearse utilizando el tipo de acción &quot;Vista rápida&quot; en Dynamic Media, de AEM Assets, bajo demanda. Cuando un usuario activa una zona interactiva de este tipo, el visor ejecuta la llamada de retorno de JavaScript `quickViewActivate` y le pasa los datos de la zona interactiva. Se espera que la página web de incrustación escuche esta llamada de retorno. Cuando déclencheur la página, abre su propia implementación de vista rápida.

## Redirigir a una página web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Puntos interactivos creados para el tipo de acción &quot;Vista rápida&quot; en Dynamic Media de AEM Assets: On demand redirige al usuario a una URL externa. Según la configuración realizada durante la creación, la dirección URL se abre en una nueva pestaña del explorador, en la misma ventana o en la ventana del explorador con nombre.
