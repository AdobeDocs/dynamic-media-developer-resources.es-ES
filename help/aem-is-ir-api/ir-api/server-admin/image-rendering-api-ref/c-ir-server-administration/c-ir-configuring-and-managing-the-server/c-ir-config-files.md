---
description: Las opciones de configuración de Image Rendering se almacenan en la variable [!DNL Platform Server] archivo de configuración.
solution: Experience Manager
title: Archivos de configuración
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Archivos de configuración{#configuration-files}

Las opciones de configuración de Image Rendering se almacenan en la variable [!DNL Platform Server] archivo de configuración.

El archivo de configuración del servidor de plataforma se encuentra en [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Este archivo es un archivo de propiedades JAVA. Se debe tener cuidado de seguir las convenciones apropiadas; de lo contrario, la [!DNL Platform Server] podría fallar al iniciar. Una doble barra invertida (`\\`) o una sola barra diagonal (/) debe utilizarse en lugar de una simple barra invertida (\) en las rutas de archivo de Windows, porque la barra invertida se utiliza como carácter de escape en este tipo de archivo. El archivo contiene propiedades no documentadas, que son para uso interno del servidor y no deben modificarse.

Consulte la [Referencia de ajustes de configuración](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) para obtener una lista de todos los ajustes de configuración de procesamiento de imágenes.
