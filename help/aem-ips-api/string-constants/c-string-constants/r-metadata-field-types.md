---
description: Lo utilizan MetadataField/type, saveMetadataFieldParam/fieldType y createMetadataField/fieldType.
solution: Experience Manager
title: Tipos de campos de metadatos
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
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
