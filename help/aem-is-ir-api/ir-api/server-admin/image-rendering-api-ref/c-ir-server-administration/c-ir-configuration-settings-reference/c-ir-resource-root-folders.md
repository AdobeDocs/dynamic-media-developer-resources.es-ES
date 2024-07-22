---
title: Carpetas raíz de recursos (ir.resourceRootPaths)
description: Una lista de rutas, delimitada por punto y coma, sirve como raíz para todos los archivos de datos con rutas de archivo relativas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# Carpetas raíz de recursos (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Una lista de rutas, delimitada por punto y coma, sirve como raíz para todos los archivos de datos con rutas de archivo relativas.

Puede ser rutas de acceso absolutas o rutas de acceso relativas a *[!DNL install_folder]*. Cuando se especifican varias rutas, el servidor intenta cada raíz en el orden dado hasta que se encuentra el archivo. El valor predeterminado es [!DNL ./resources], para una ruta de acceso raíz predeterminada de [!DNL install_folder/resources].
