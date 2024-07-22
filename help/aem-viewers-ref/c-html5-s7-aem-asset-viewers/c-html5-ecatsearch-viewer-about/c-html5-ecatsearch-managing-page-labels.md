---
description: Administración de etiquetas de página
solution: Experience Manager
title: Administración de etiquetas de página
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Administración de etiquetas de página{#managing-page-labels}

Existen dos lugares en la interfaz de usuario del visor donde se muestran las etiquetas de página: el modo de miniaturas y la lista desplegable de tabla de contenido.

Se pueden definir tres tipos de etiquetas:

* Etiquetas definidas por el autor mediante el mecanismo de localización SYMBOL.
* Etiquetas definidas por el autor en el servidor, dentro de Dynamic Media Classic.
* Etiquetas generadas automáticamente por el visor.

Las etiquetas basadas en SYMBOL se definen usando `MediaSet.LABEL_XX[_YY]` y `MediaSet.LABEL_DELIM` SYMBOL como se describe en [Localización de elementos de la interfaz de usuario](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Puede definir dichas etiquetas para todo el pliego del catálogo electrónico, en cuyo caso debe utilizar una sintaxis SYMBOL corta ( `MediaSet.LABEL_XX`). O bien, especifíquelo individualmente para cada página mediante la sintaxis SYMBOL completa ( `MediaSet.LABEL_XX_YY`).

Cuando define etiquetas para ambas páginas en el pliego de catálogo electrónico, el visor concatena estas etiquetas en una cadena utilizando `MediaSet.LABEL_DELIM` SYMBOL. Las etiquetas basadas en SÍMBOLOS tienen prioridad sobre las etiquetas definidas en el backend o las etiquetas generadas automáticamente por el visualizador.

Las etiquetas definidas en Dynamic Media Classic se almacenan en el registro UserData de imágenes de página individuales. Igual que con las etiquetas basadas en SÍMBOLOS. Es decir, si ambas páginas del pliego de catálogo electrónico tienen etiquetas definidas, se concatenan con `MediaSet.LABEL_DELIM` SYMBOL en modo horizontal. Las etiquetas de Dynamic Media Classic tienen prioridad sobre las etiquetas generadas automáticamente, pero se sustituyen por etiquetas basadas en SÍMBOLOS.

Las etiquetas generadas automáticamente son números secuenciales asignados a todas las páginas del catálogo electrónico. Las etiquetas generadas automáticamente se ignoran para el pliego determinado si tiene definidas etiquetas basadas en SYMBOL o Dynamic Media Classic.

En la tabla de contenido, es posible deshabilitar la visualización de etiquetas generadas automáticamente usando el parámetro `showdefault`.
