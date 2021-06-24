---
description: Utilizado por MetadataField/type, saveMetadataFieldParam/fieldType y createMetadataField/fieldType.
solution: Experience Manager
title: Tipos de campos de metadatos
feature: Dynamic Media Classic,SDK/API,Metadatos
role: Developer,Administrator
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
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
