---
description: Utilizado por MetadataField/type, saveMetadataFieldParam/fieldType y createMetadataField/fieldType.
seo-description: Utilizado por MetadataField/type, saveMetadataFieldParam/fieldType y createMetadataField/fieldType.
seo-title: Tipos de campos de metadatos
solution: Experience Manager
title: Tipos de campos de metadatos
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
feature: Dynamic Media Classic,SDK/API,Metadatos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 1%

---


# Tipos de campos de metadatos{#metadata-field-types}

Utilizado por MetadataField/type, saveMetadataFieldParam/fieldType y createMetadataField/fieldType.

Sintaxis

## Valores {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Un caso especial de  [!DNL `SingleFixedTag`] con un diccionario no modificable inicializado a los valores  [!DNL `True`] y  [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Cero o más valores de cadena de un diccionario cerrado. Solo los usuarios administradores pueden modificar el diccionario.
* [!DNL `MultiTag`]: Cero o más valores de cadena.
* [!DNL `SingleFixedTag`]: Un valor de cadena individual de un diccionario cerrado. Si se llama a `setAssetMetadata` o `batchSetAssetMetadata` con un valor que no está en el diccionario, se devuelve un error. Solo los usuarios administradores pueden modificar el diccionario.

* [!DNL `SingleTag`]: Cualquier valor de cadena individual.
* [!DNL `String`]

