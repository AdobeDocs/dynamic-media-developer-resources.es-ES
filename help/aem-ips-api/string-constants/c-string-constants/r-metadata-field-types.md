---
description: Utilizado por MetadataField/type, saveMetadataFieldParam/fieldType y createMetadataField/fieldType.
seo-description: Utilizado por MetadataField/type, saveMetadataFieldParam/fieldType y createMetadataField/fieldType.
seo-title: Tipos de campos de metadatos
solution: Experience Manager
title: Tipos de campos de metadatos
topic: Scene7 Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# Tipos de campos de metadatos{#metadata-field-types}

Utilizado por MetadataField/type, saveMetadataFieldParam/fieldType y createMetadataField/fieldType.

Sintaxis

## Valores {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:: Un caso especial de [!DNL `SingleFixedTag`] con un diccionario no modificable inicializado con los valores [!DNL `True`] y [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:: Cero o más valores de cadena de un diccionario cerrado. Solo los usuarios administradores pueden modificar el diccionario.
* [!DNL `MultiTag`]:: Cero o más valores de cadena.
* [!DNL `SingleFixedTag`]:: Un valor de cadena único de un diccionario cerrado. Si se llama `setAssetMetadata` o `batchSetAssetMetadata` se llama con un valor que no está en el diccionario, se mostrará un error. Solo los usuarios administradores pueden modificar el diccionario.

* [!DNL `SingleTag`]:: Cualquier valor de cadena individual.
* [!DNL `String`]

