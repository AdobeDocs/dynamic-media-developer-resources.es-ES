---
description: Establece los comandos del protocolo de servicio de imágenes o de renderización de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

Establece los comandos del protocolo de servicio de imágenes o de renderización de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.

Para el servicio de imágenes, los comandos de la sección `urlModifier` se publican en el campo de catálogo Modificador y se aplican antes de cualquier comando especificado en la dirección URL de la solicitud. Comandos en `urlPostApplyModifier` se publican en el `PostModifier` campo catálogo y anular cualquier comando de la dirección URL de solicitud o de `urlModifier`. Para la renderización de imágenes, los comandos de `urlModifier` y `urlPostApplyModifier` se concatenan y publican en el campo de catálogo Modificador .

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
| `*`urlModifier`*` | `xsd:string` | No | Comandos de protocolo de servicio de imágenes o renderización de imágenes para aplicar antes de la solicitud o `urlPostApplyModifier` comandos. |
| `*`urlPostApplyModifier`*` | `xsd:string` | No | Comandos de protocolo de servicio de imágenes o renderización de imágenes que se aplican después de `urlModifier` y los comandos de solicitud. |

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
