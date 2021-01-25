---
description: Crea una imagen con capas que puede tener varias capas de texto e imagen.
seo-description: Crea una imagen con capas que puede tener varias capas de texto e imagen.
seo-title: createTemplate
solution: Experience Manager
title: createTemplate
topic: Dynamic Media Image Production System API
uuid: c54bd47c-13e1-4b0d-a24c-9829b0a6d5bf
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 10%

---


# createTemplate{#createtemplate}

Crea una imagen con capas que puede tener varias capas de texto e imagen.

El parámetro `urlModifier` especifica los comandos de protocolo del servidor de imágenes almacenados en el catálogo del servidor de imágenes aplicado antes de cualquier comando proporcionado por el usuario en la dirección URL. El parámetro `urlPostApplyModifier` especifica los comandos de protocolo aplicados después de cualquier comando de URL, lo que anulará cualquier configuración proporcionada por el usuario en conflicto.

## Tipos de usuarios autorizados {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Entrada (createTemplateParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Compañía a la que pertenece la plantilla. |
| `*`folderHandle`*` | `xsd:string` | Sí | El identificador de carpeta que representa la carpeta en la que reside la plantilla. |
| `*`name`*` | `xsd:string` | Sí | Nombre de la plantilla. |
| `*`type`*` | `xsd:string` | Sí | Tipo de plantilla. |
| `*`urlModifier`*` | `xsd:string` | Sí | Especifica los comandos del servidor de imágenes almacenados en el catálogo IS que se aplican antes de cualquier comando proporcionado por el usuario en la dirección URL. |
| `*`urlPostApplyModifier`*` | `xsd:string` | No | Especifica los comandos de protocolo aplicados después de cualquier comando de URL, lo que anulará cualquier configuración proporcionada por el usuario en conflicto. |

**Salida (createTemplateParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sí | Identificador de la plantilla. |

## Ejemplos {#section-09adb4d2f0c944af875c4463a461f55d}

Este ejemplo de código crea una plantilla en una carpeta especificada por un identificador, con el nombre `APIcreateTemplate`, `urlModifier` y `urlPostApplyModifier`. La respuesta devuelve el identificador a la plantilla recién creada.

**Solicitar**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**Respuesta**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```

