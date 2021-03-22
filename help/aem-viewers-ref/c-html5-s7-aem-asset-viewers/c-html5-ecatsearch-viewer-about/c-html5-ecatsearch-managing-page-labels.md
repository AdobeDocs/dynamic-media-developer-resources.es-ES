---
description: Administración de etiquetas de página
solution: Experience Manager
title: Administración de etiquetas de página
uuid: 49444fe6-ef34-4e5b-a293-e23830a67b4d
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# Administración de etiquetas de página{#managing-page-labels}

Hay dos lugares en la interfaz de usuario del visor donde se muestran las etiquetas de página: el modo de miniaturas y la lista desplegable de tabla de contenido.

Existen tres tipos de etiquetas que se pueden definir:

* Etiquetas definidas por el autor mediante el mecanismo de localización SYMBOL.
* Etiquetas definidas por el autor en el servidor, dentro de Dynamic Media Classic.
* Etiquetas generadas automáticamente por el visor.

Las etiquetas basadas en SYMBOL se definen utilizando `MediaSet.LABEL_XX[_YY]` y `MediaSet.LABEL_DELIM` SYMBOLs como se describe en [Localización de los elementos de la interfaz de usuario](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Puede definir dichas etiquetas para todo el catálogo electrónico, en cuyo caso debe utilizar una sintaxis corta de SYMBOL ( `MediaSet.LABEL_XX`). O bien, especifíquelo para cada página individualmente utilizando la sintaxis SYMBOL completa ( `MediaSet.LABEL_XX_YY`).

Cuando define etiquetas para ambas páginas en la extensión del catálogo electrónico, el visor concatena estas etiquetas en una cadena utilizando `MediaSet.LABEL_DELIM` SYMBOL. Las etiquetas basadas en SYMBOL tienen prioridad sobre las etiquetas definidas en el servidor o que el visor genera automáticamente.

Las etiquetas definidas en Dynamic Media Classic se almacenan en el registro UserData de imágenes de página individuales. Igual que con las etiquetas basadas en SYMBOL. Es decir, si ambas páginas del catálogo electrónico tienen etiquetas definidas, se concatenan utilizando `MediaSet.LABEL_DELIM` SYMBOL en modo horizontal. Las etiquetas de Dynamic Media Classic tienen prioridad sobre las etiquetas generadas automáticamente, pero las etiquetas basadas en SYMBOL las anulan.

Las etiquetas generadas automáticamente son números secuenciales asignados a todas las páginas del catálogo electrónico. Las etiquetas generadas automáticamente se ignoran para el pliego dado si tiene definidas etiquetas basadas en SYMBOL o etiquetas de Dynamic Media Classic definidas.

En la tabla de contenido, es posible desactivar la visualización de etiquetas generadas automáticamente utilizando el parámetro `showdefault`.
