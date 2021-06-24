---
description: Establece los comandos del protocolo de servicio de imágenes o de renderización de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

Establece los comandos del protocolo de servicio de imágenes o de renderización de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.

Para Image Serving, los comandos del parámetro `urlModifier` se publican en el campo de catálogo de modificadores y se aplican antes de cualquier comando especificado en la dirección URL de la solicitud. Los comandos de `urlPostApplyModifier` se publicarán en el campo del catálogo `PostModifier` y anularán todos los comandos de la dirección URL de la solicitud o de `urlModifier`. Para el procesamiento de imágenes, los comandos de `urlModifier` y `urlPostApplyModifier` se concatenan y publican en el campo de catálogo Modificador.

## Tipos de usuarios autorizados {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Entrada (setUrlModifierParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`assetHandle`*` | `xsd:string` | Sí | Identificador de recurso. |
| `*`urlModifier`*` | `xsd:string` | No | Comandos de protocolo Image Serving o Image Rendering para aplicar antes de los comandos request o `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | No | Los comandos de protocolo de servicio de imágenes o renderización de imágenes se aplican después de los comandos `urlModifier` y request. |

**Salida (setUrlModifierReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Solicitar**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**Respuesta**

Ninguno.
