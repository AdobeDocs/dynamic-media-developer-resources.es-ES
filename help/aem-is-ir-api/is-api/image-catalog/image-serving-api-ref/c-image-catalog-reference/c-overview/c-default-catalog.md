---
description: El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo para todos los catálogos de imágenes.
solution: Experience Manager
title: Catálogo predeterminado
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
TQID: 'https://experienceleague.adobe.com/qbfEwBJ-eQmCbBR0MJQhP7x3ZEd30nfLJHWjBVoXIjc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 0%

---

# Catálogo predeterminado{#default-catalog}

El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo para todos los catálogos de imágenes.

Si no se encuentra un atributo concreto en un catálogo de imágenes específico, el servidor utiliza el valor correspondiente del catálogo predeterminado en su lugar. Del mismo modo, el catálogo predeterminado se puede utilizar para proporcionar valores predeterminados para registros de datos de catálogo específicos (imágenes, definiciones de macros, fuentes y perfiles ICC). Si no se encuentra un registro de datos concreto en un catálogo de imágenes específico, el servidor intenta encontrarlo en el catálogo predeterminado en su lugar. Esto permite que los catálogos de imágenes se rellenen escasamente y simplifica la administración de atributos y datos globales, como plantillas compartidas, macros, fuentes, etc.

Además, el catálogo predeterminado proporciona todos los atributos y registros de datos (macros, fuentes, perfiles ICC, reglas de preprocesamiento de solicitudes) cuando no hay ningún catálogo de imágenes específico involucrado en una operación.

Para el correcto funcionamiento de [!DNL Platform Server], el archivo de atributos de catálogo para el catálogo predeterminado debe llamarse [!DNL default.ini], debe existir siempre en la carpeta de catálogo y debe rellenarse completamente con todos los atributos necesarios, excluyendo `attribute::RootId` y las referencias a los distintos archivos de datos de catálogo, que son todos opcionales.

>[!NOTE]
>
>Todos los archivos de atributos de catálogo excepto [!DNL default.ini] deben contener un valor `attribute::RootId` único. `attribute::RootId` en [!DNL default.ini] debe estar vacío.
