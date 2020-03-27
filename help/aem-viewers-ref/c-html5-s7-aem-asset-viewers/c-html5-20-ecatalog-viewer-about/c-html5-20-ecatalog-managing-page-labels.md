---
description: nulo
seo-description: nulo
seo-title: Administración de etiquetas de página
solution: Experience Manager
title: Administración de etiquetas de página
topic: Dynamic media
uuid: ab3df37d-113b-4762-ba9c-b92ffc41f1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Administración de etiquetas de página{#managing-page-labels}

Hay dos lugares en la interfaz de usuario del visor donde se muestran las etiquetas de página: el modo de miniaturas y la lista desplegable de la tabla de contenido.

Existen tres tipos de etiquetas que se pueden definir:

* Etiquetas definidas por el autor utilizando el mecanismo de localización SYMBOL.
* Etiquetas definidas por el autor en el servidor, dentro de SPS.
* Etiquetas generadas automáticamente por el visor.

Las etiquetas basadas en SYMBOL se definen utilizando `MediaSet.LABEL_XX[_YY]` y `MediaSet.LABEL_DELIM` SÍMBOLOS como se describe en la [Localización de los elementos](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)de la interfaz de usuario. Puede definir dichas etiquetas para todo el pliego de catálogos electrónicos, en cuyo caso debe utilizar una sintaxis corta de SYMBOL ( `MediaSet.LABEL_XX`). O bien, especifíquelo para cada página de forma individual utilizando la sintaxis SÍMBOLO completa ( `MediaSet.LABEL_XX_YY`).

Cuando se definen etiquetas para ambas páginas en el pliego de catálogos electrónicos, el visor concatena estas etiquetas en una cadena mediante `MediaSet.LABEL_DELIM` SYMBOL. Las etiquetas basadas en SYMBOL tienen prioridad sobre las etiquetas definidas en el servidor o generadas automáticamente por el visor.

Las etiquetas definidas en SPS se almacenan en el registro UserData de imágenes de página individuales. Igual que con las etiquetas basadas en SYMBOL. Es decir, si ambas páginas del pliego de catálogos electrónicos tienen etiquetas definidas, se concatenan usando `MediaSet.LABEL_DELIM` SYMBOL en modo horizontal. Las etiquetas de SPS tienen prioridad sobre las etiquetas generadas automáticamente, pero se anulan con las etiquetas basadas en SYMBOL.

Las etiquetas generadas automáticamente son números secuenciales asignados a todas las páginas del catálogo electrónico. Las etiquetas generadas automáticamente se omiten para el pliego dado si tiene definidas etiquetas basadas en SYMBOL o etiquetas de SPS.

En la tabla de contenido, es posible desactivar la visualización de etiquetas generadas automáticamente mediante `showdefault` parámetros.
