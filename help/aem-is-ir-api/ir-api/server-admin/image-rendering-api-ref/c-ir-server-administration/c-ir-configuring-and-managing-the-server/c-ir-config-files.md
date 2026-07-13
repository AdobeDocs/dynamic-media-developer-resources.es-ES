---
description: Las opciones de configuración del procesamiento de imágenes se almacenan en el archivo de configuración  [!DNL Platform Server] Image Rendering.
solution: Experience Manager
title: Archivos de configuración
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
TQID: 'https://experienceleague.adobe.com/KTBXtuSOstPMi7bPQg70jyUVCqcXlLiLPiFFhyp9iFg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# Archivos de configuración{#configuration-files}

Las opciones de configuración del procesamiento de imágenes se almacenan en el archivo de configuración [!DNL Platform Server].

El archivo de configuración del servidor de la plataforma se encuentra en [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Este archivo es un archivo de propiedades JAVA. Se debe tener cuidado de seguir las convenciones apropiadas; de lo contrario, [!DNL Platform Server] podría no iniciarse. Se debe usar una barra invertida doble (`\\`) o una sola barra diagonal (/) en lugar de una barra invertida simple (\) en las rutas de acceso de archivos de Windows, ya que la barra invertida se usa como carácter de escape en este tipo de archivo. El archivo contiene propiedades no documentadas, que son para uso interno del servidor y no deben modificarse.

Consulte la [Referencia de ajustes de configuración](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) para obtener una lista de todos los ajustes de configuración de procesamiento de imágenes.

