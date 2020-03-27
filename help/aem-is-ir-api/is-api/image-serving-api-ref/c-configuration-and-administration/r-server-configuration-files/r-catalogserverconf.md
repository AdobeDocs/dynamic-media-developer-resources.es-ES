---
description: Contiene la configuración relacionada con la administración de catálogos de imágenes.
seo-description: Contiene la configuración relacionada con la administración de catálogos de imágenes.
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# catalog-server.conf{#catalog-server-conf}

Contiene la configuración relacionada con la administración de catálogos de imágenes.

Este archivo es un archivo de propiedades de JAVA. Se debe velar por el cumplimiento de las convenciones pertinentes; de lo contrario, puede que el Servidor de plataforma no pueda realizar el inicio. Utilice una barra invertida de doble &#39;\\&#39; o una sola barra diagonal inversa &#39;/&#39; en lugar de una barra invertida &#39;\&#39; en las rutas de archivos de Windows. La barra invertida se utiliza como carácter de escape en este tipo de archivo.

Los cambios realizados en este archivo surtirán efecto poco después de guardarlo.

Solo se puede cambiar la configuración que se muestra a continuación en [!DNL catalog-service.conf]. Si no hay una configuración concreta, puede agregarla en cualquier parte del archivo. Solo puede haber una instancia de cada configuración.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
