---
description: nulo
seo-description: nulo
seo-title: Compatibilidad con hotspot
solution: Experience Manager
title: Compatibilidad con hotspot
topic: Dynamic media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Compatibilidad con puntos interactivos{#hotspot-support}

El visor admite la representación de iconos de zonas interactivas en la parte superior de la vista principal. El aspecto de los iconos de puntos interactivos se controla mediante CSS, tal como se describe en la sección Puntos interactivos.

Consulte [Puntos interactivos](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Las zonas interactivas pueden activar una función de Vista rápida en la página web de alojamiento activando una llamada de retorno de JavaScript o redireccionar a un usuario a una página web externa.

## Puntos interactivos de Vista rápida {#section-cda48fc9730142d0bb3326bac7df3271}

Estos tipos de zonas interactivas deben crearse utilizando el tipo de acción &quot;Vista rápida&quot; en Dynamic Media, AEM Assets - On Demand. Cuando un usuario activa una zona interactiva de este tipo, el visor ejecuta la llamada de retorno de JavaScript `quickViewActivate` y le pasa los datos de zona interactiva. Se espera que la página web de incrustación escuche esta llamada de retorno. Cuando activa la página, abre su propia implementación de Vista rápida.

## Redirigir a la página Web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Puntos interactivos creados para el tipo de acción &quot;Vista rápida&quot; en Dynamic Media de AEM Assets: On Demand redirige al usuario a una dirección URL externa. Según la configuración realizada durante la creación, la URL se abre en una nueva ficha del explorador, en la misma ventana o en la ventana del explorador con nombre.
