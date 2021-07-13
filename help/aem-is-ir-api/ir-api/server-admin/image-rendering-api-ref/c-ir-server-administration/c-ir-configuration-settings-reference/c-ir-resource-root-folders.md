---
description: La lista de rutas, delimitada por punto y coma, sirve de base para todos los archivos de datos con rutas de archivo relativas.
solution: Experience Manager
title: Carpetas raíz de recursos (ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# Carpetas raíz de recursos (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

La lista de rutas, delimitada por punto y coma, sirve de base para todos los archivos de datos con rutas de archivo relativas.

Puede ser una ruta absoluta o una ruta relativa a *[!DNL install_folder]*. Cuando se especifican varias rutas, el servidor prueba cada raíz en el orden dado hasta que se encuentra el archivo. El valor predeterminado es [!DNL ./resources], para una ruta raíz predeterminada de [!DNL install_folder/resources].
