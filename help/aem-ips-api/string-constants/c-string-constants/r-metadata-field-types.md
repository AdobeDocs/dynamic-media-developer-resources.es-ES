---
description: Lo utilizan MetadataField/type, saveMetadataFieldParam/fieldType y createMetadataField/fieldType.
solution: Experience Manager
title: Tipos de campos de metadatos
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
TQID: 'https://experienceleague.adobe.com/XFRmGmRc9iE5xmW0P2KfDzc-X-3TTrNYWkzNieSodQc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 2%

---

# Tipos de campos de metadatos{#metadata-field-types}

Lo utilizan MetadataField/type, saveMetadataFieldParam/fieldType y createMetadataField/fieldType.

Sintaxis

## Valores {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: caso especial de [!DNL `SingleFixedTag`] con un diccionario no modificable inicializado en los valores [!DNL `True`] y [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: cero o más valores de cadena de un diccionario cerrado. Solo los usuarios administradores pueden modificar el diccionario.
* [!DNL `MultiTag`]: cero o más valores de cadena.
* [!DNL `SingleFixedTag`]: un solo valor de cadena de un diccionario cerrado. Si se llama a `setAssetMetadata` o `batchSetAssetMetadata` con un valor que no está en el diccionario, se devuelve un error. Solo los usuarios administradores pueden modificar el diccionario.

* [!DNL `SingleTag`]: cualquier valor de cadena individual.
* [!DNL `String`]

