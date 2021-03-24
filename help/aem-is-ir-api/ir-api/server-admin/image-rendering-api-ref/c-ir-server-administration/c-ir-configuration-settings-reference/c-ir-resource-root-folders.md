---
description: La lista de rutas, delimitada por punto y coma, sirve de base para todos los archivos de datos con rutas de archivo relativas.
solution: Experience Manager
title: Carpetas raíz de recursos (ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Carpetas raíz de recursos (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

La lista de rutas, delimitada por punto y coma, sirve de base para todos los archivos de datos con rutas de archivo relativas.

Puede ser una ruta absoluta o una ruta relativa a *[!DNL install_folder]*. Cuando se especifican varias rutas, el servidor prueba cada raíz en el orden dado hasta que se encuentra el archivo. El valor predeterminado es [!DNL ./resources], para una ruta raíz predeterminada de [!DNL install_folder/resources].
