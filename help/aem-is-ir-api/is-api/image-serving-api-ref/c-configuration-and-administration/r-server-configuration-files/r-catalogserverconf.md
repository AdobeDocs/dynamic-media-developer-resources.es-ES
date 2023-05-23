---
description: Contiene configuración relacionada con la administración de catálogos de imágenes.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Contiene configuración relacionada con la administración de catálogos de imágenes.

Este archivo es un archivo de propiedades JAVA. Se debe tener cuidado de seguir las convenciones apropiadas; de lo contrario, la [!DNL Platform Server] puede fallar al iniciar. Utilice una doble barra invertida &#39;\\&#39; o una sola barra diagonal &#39;/&#39; en lugar de una barra invertida &#39;\&#39; en las rutas de archivos de Windows. La barra invertida se utiliza como carácter de escape en este tipo de archivo.

Los cambios en este archivo se aplicarán poco después de que se guarde el archivo.

Solo se pueden cambiar las configuraciones enumeradas a continuación en [!DNL catalog-service.conf]. Si una configuración en particular está ausente, se puede agregar en cualquier parte del archivo. Solo puede haber una instancia de cada configuración.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
