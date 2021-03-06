---
description: Crea una imagen en capas que puede tener varias capas de texto e imágenes.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 10%

---

# createTemplate{#createtemplate}

Crea una imagen en capas que puede tener varias capas de texto e imágenes.

La variable `urlModifier` especifica los comandos de protocolo de Image Server almacenados en el catálogo de Image Server aplicados antes de cualquier comando proporcionado por el usuario en la URL. La variable `urlPostApplyModifier` especifica los comandos de protocolo aplicados después de cualquier comando URL, lo que anulará cualquier configuración conflictiva suministrada por el usuario.

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
| companyHandle | `xsd:string` | Sí | Empresa a la que pertenece la plantilla. |
| folderHandle | `xsd:string` | Sí | El controlador de carpeta que representa la carpeta donde reside la plantilla. |
| name | `xsd:string` | Sí | Nombre de la plantilla. |
| tipo | `xsd:string` | Sí | Tipo de plantilla. |
| urlModifier | `xsd:string` | Sí | Especifica los comandos del servidor de imágenes almacenados en el catálogo IS que se aplican antes de cualquier comando proporcionado por el usuario en la dirección URL. |
| urlPostApplyModifier | `xsd:string` | No | Especifica los comandos de protocolo aplicados después de cualquier comando URL, que anularán cualquier configuración conflictiva suministrada por el usuario. |

**Salida (createTemplateParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| assetHandle | `xsd:string` | Sí | El identificador de la plantilla. |

## Ejemplos {#section-09adb4d2f0c944af875c4463a461f55d}

Este ejemplo de código crea una plantilla en una carpeta especificada por un controlador, con un nombre de `APIcreateTemplate`, `urlModifier`y `urlPostApplyModifier`. La respuesta devuelve el identificador a la plantilla recién creada.

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
