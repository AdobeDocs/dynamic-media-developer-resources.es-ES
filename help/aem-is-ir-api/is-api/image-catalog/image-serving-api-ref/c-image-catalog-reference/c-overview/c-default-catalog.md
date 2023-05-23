---
description: El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo para todos los catálogos de imágenes.
solution: Experience Manager
title: Catálogo predeterminado
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Catálogo predeterminado{#default-catalog}

El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo para todos los catálogos de imágenes.

Si no se encuentra un atributo concreto en un catálogo de imágenes específico, el servidor utiliza el valor correspondiente del catálogo predeterminado en su lugar. Del mismo modo, el catálogo predeterminado se puede utilizar para proporcionar valores predeterminados para registros de datos de catálogo específicos (imágenes, definiciones de macros, fuentes y perfiles ICC). Si no se encuentra un registro de datos concreto en un catálogo de imágenes específico, el servidor intenta encontrarlo en el catálogo predeterminado en su lugar. Esto permite que los catálogos de imágenes se rellenen escasamente y simplifica la administración de atributos y datos globales, como plantillas compartidas, macros, fuentes, etc.

Además, el catálogo predeterminado proporciona todos los atributos y registros de datos (macros, fuentes, perfiles ICC, reglas de preprocesamiento de solicitudes) cuando no hay ningún catálogo de imágenes específico involucrado en una operación.

Para el correcto funcionamiento del [!DNL Platform Server] el nombre del archivo de atributos de catálogo para el catálogo predeterminado debe ser [!DNL default.ini], siempre debe existir en la carpeta del catálogo y debe rellenarse completamente con todos los atributos necesarios, excluyendo `attribute::RootId` y las referencias a los distintos archivos de datos del catálogo, que son opcionales.

>[!NOTE]
>
>Todos los archivos de atributos de catálogo excepto [!DNL default.ini] debe contener un único `attribute::RootId` valor. `attribute::RootId` in [!DNL default.ini] debe estar vacío.
