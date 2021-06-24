---
description: Los ajustes de configuración de procesamiento de imágenes se almacenan en el archivo de configuración de Platform Server.
solution: Experience Manager
title: Archivos de configuración
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Archivos de configuración{#configuration-files}

Los ajustes de configuración de procesamiento de imágenes se almacenan en el archivo de configuración de Platform Server.

El archivo de configuración del servidor de plataforma se encuentra en [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Este archivo es un archivo de propiedades de JAVA. Se debe tener cuidado de seguir las convenciones adecuadas; de lo contrario, es posible que Platform Server no se inicie. Se debe utilizar una barra invertida doble (`\\`) o una sola barra diagonal (/) en lugar de una barra invertida simple (\) en las rutas de archivos de Windows, ya que la barra invertida se utiliza como carácter de escape en este tipo de archivo. El archivo contiene propiedades no documentadas, que son para uso interno del servidor y no deben modificarse.

Consulte la [Referencia de configuración](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) para obtener una lista de todos los ajustes de configuración de procesamiento de imágenes.
