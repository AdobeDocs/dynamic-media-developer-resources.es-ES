---
description: Los ajustes de configuración de procesamiento de imágenes se almacenan en el archivo de configuración de Platform Server.
seo-description: Los ajustes de configuración de procesamiento de imágenes se almacenan en el archivo de configuración de Platform Server.
seo-title: Archivos de configuración
solution: Experience Manager
title: Archivos de configuración
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# Archivos de configuración{#configuration-files}

Los ajustes de configuración de procesamiento de imágenes se almacenan en el archivo de configuración de Platform Server.

El archivo de configuración del servidor de plataforma se encuentra en [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Este archivo es un archivo de propiedades de JAVA. Se debe tener cuidado de seguir las convenciones adecuadas; de lo contrario, es posible que Platform Server no se inicie. Se debe utilizar una barra invertida doble (`\\`) o una sola barra diagonal (/) en lugar de una barra invertida simple (\) en las rutas de archivos de Windows, ya que la barra invertida se utiliza como carácter de escape en este tipo de archivo. El archivo contiene propiedades no documentadas, que son para uso interno del servidor y no deben modificarse.

Consulte la [Referencia de configuración](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) para obtener una lista de todos los ajustes de configuración de procesamiento de imágenes.
