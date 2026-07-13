---
title: Carpetas raíz de recursos (ir.resourceRootPaths)
description: Una lista de rutas, delimitada por punto y coma, sirve como raíz para todos los archivos de datos con rutas de archivo relativas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
TQID: 'https://experienceleague.adobe.com/5mKCVHonfG4riWoIenUyFHtMnSg3cmL-Lm-YTGN34fA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 0%

---

# Carpetas raíz de recursos (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Una lista de rutas, delimitada por punto y coma, sirve como raíz para todos los archivos de datos con rutas de archivo relativas.

Puede ser rutas de acceso absolutas o rutas de acceso relativas a *[!DNL install_folder]*. Cuando se especifican varias rutas, el servidor intenta cada raíz en el orden dado hasta que se encuentra el archivo. El valor predeterminado es [!DNL ./resources], para una ruta de acceso raíz predeterminada de [!DNL install_folder/resources].

