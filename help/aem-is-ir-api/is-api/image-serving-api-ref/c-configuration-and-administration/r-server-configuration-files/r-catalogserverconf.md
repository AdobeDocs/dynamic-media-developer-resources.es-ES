---
description: Contiene la configuración relacionada con la administración de catálogos de imágenes.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Contiene la configuración relacionada con la administración de catálogos de imágenes.

Este archivo es un archivo de propiedades de JAVA. Se debe velar por el cumplimiento de las convenciones pertinentes; de lo contrario, es posible que Platform Server no se inicie. Utilice una barra invertida doble &#39;\\&#39; o una sola barra diagonal &#39;/&#39; en lugar de una barra invertida &#39;\&#39; en las rutas de archivos de Windows. La barra invertida se utiliza como carácter de escape en este tipo de archivo.

Los cambios realizados en este archivo surtirán efecto poco después de que se guarde el archivo.

En [!DNL catalog-service.conf] solo se puede cambiar la configuración que se muestra a continuación. Si no hay una configuración determinada, puede agregarla a cualquier lugar del archivo. Solo puede haber una instancia de cada configuración.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
