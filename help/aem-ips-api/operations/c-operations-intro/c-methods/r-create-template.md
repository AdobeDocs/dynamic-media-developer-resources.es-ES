---
description: Crea una imagen con capas que puede tener varias capas de texto e imagen.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
TQID: 'https://experienceleague.adobe.com/T9x2yuGOkwJ5xp6CVyREMySIy7HYL58jYI3-J2E2K6g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 9%

---

# createTemplate{#createtemplate}

Crea una imagen con capas que puede tener varias capas de texto e imagen.

El parámetro `urlModifier` especifica los comandos de protocolo del servidor de imágenes almacenados en el catálogo del servidor de imágenes aplicado antes de cualquier comando proporcionado por el usuario en la dirección URL. El parámetro `urlPostApplyModifier` especifica los comandos de protocolo aplicados después de cualquier comando de URL, lo que anula cualquier configuración proporcionada por el usuario que esté en conflicto.

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

Este ejemplo de código crea una plantilla en una carpeta especificada por un identificador, con el nombre `APIcreateTemplate`, `urlModifier` y `urlPostApplyModifier`. La respuesta devuelve el identificador a la plantilla recién creada.

**Solicitud**

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
