---
description: Crea una imagen con capas que puede tener varias capas de texto e imagen.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 11%

---

# createTemplate{#createtemplate}

Crea una imagen con capas que puede tener varias capas de texto e imagen.

El `urlModifier` especifica los comandos de protocolo del servidor de imágenes almacenados en el catálogo del servidor de imágenes aplicado antes de cualquier comando proporcionado por el usuario en la dirección URL. El `urlPostApplyModifier` especifica los comandos de protocolo aplicados después de los comandos de URL, que anulan cualquier configuración proporcionada por el usuario que esté en conflicto.

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
| companyHandle | `xsd:string` | Sí | Compañía a la que pertenece la plantilla. |
| folderHandle | `xsd:string` | Sí | Identificador de carpeta que representa la carpeta en la que reside la plantilla. |
| nombre | `xsd:string` | Sí | Nombre de plantilla. |
| tipo | `xsd:string` | Sí | Tipo de plantilla. |
| urlModifier | `xsd:string` | Sí | Especifica los comandos del servidor de imágenes almacenados en el catálogo de IS que se aplican antes de cualquier comando proporcionado por el usuario en la dirección URL. |
| urlPostApplyModifier | `xsd:string` | No | Especifica los comandos de protocolo aplicados después de los comandos de dirección URL, lo que anula cualquier configuración proporcionada por el usuario que esté en conflicto. |

**Salida (createTemplateParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| assetHandle | `xsd:string` | Sí | El identificador de la plantilla. |

## Ejemplos {#section-09adb4d2f0c944af875c4463a461f55d}

Este ejemplo de código crea una plantilla en una carpeta especificada por un identificador, con un nombre de `APIcreateTemplate`, a `urlModifier`, y a `urlPostApplyModifier`. La respuesta devuelve el identificador a la plantilla recién creada.

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
