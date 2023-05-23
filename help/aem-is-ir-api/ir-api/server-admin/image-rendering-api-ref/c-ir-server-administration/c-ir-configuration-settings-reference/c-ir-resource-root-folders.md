---
description: La lista de rutas, delimitada por punto y coma, sirve como raíz para todos los archivos de datos con rutas de archivo relativas.
solution: Experience Manager
title: Carpetas raíz de recursos (ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Carpetas raíz de recursos (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

La lista de rutas, delimitada por punto y coma, sirve como raíz para todos los archivos de datos con rutas de archivo relativas.

Puede ser rutas absolutas o rutas relativas a *[!DNL install_folder]*. Cuando se especifican varias rutas, el servidor probará cada raíz en el orden dado hasta que se encuentre el archivo. El valor predeterminado es [!DNL ./resources], para una ruta raíz predeterminada de [!DNL install_folder/resources].
