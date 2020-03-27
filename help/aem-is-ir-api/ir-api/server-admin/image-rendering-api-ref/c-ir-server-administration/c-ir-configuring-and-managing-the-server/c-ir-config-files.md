---
description: Los ajustes de configuración del procesamiento de imágenes se almacenan en el archivo de configuración de Platform Server.
seo-description: Los ajustes de configuración del procesamiento de imágenes se almacenan en el archivo de configuración de Platform Server.
seo-title: Archivos de configuración
solution: Experience Manager
title: Archivos de configuración
topic: Scene7 Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Archivos de configuración{#configuration-files}

Los ajustes de configuración del procesamiento de imágenes se almacenan en el archivo de configuración de Platform Server.

El archivo de configuración del servidor de plataformas se encuentra en [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Este archivo es un archivo de propiedades de JAVA. Se debe tener cuidado de seguir las convenciones apropiadas, de lo contrario el Servidor de plataformas podría no tener inicios. Se debe utilizar una barra invertida de doble (\\) o una sola barra diagonal inversa (/) en lugar de una barra invertida simple (\) en las rutas de archivos de Windows, ya que la barra invertida se utiliza como carácter de escape en este tipo de archivo. El archivo contiene propiedades no documentadas, que son para uso interno del servidor y no deben modificarse.

Consulte la Referencia [](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) de configuración para obtener una lista de todos los ajustes de configuración de procesamiento de imágenes.
