---
description: Establece los comandos de protocolo de servicio de imágenes o procesamiento de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.
seo-description: Establece los comandos de protocolo de servicio de imágenes o procesamiento de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
topic: Scene7 Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUrlModifier{#seturlmodifier}

Establece los comandos de protocolo de servicio de imágenes o procesamiento de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.

Para el servicio de imágenes, los comandos del `urlModifier` parámetro se publican en el campo de catálogo Modificador y se aplican antes de cualquier comando especificado en la dirección URL de la solicitud. Los comandos de `urlPostApplyModifier` se publicarán en el campo del `PostModifier` catálogo y anularán todos los comandos de la dirección URL de la solicitud o en `urlModifier`. En Procesamiento de imágenes, los comandos de `urlModifier` y `urlPostApplyModifier` se concatenan y publican en el campo de catálogo Modificador.

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de Compañía. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador de recurso. |
| ` *`urlModifier`*` | `xsd:string` | No | Comandos de protocolo de servicio de imágenes o procesamiento de imágenes que se aplicarán antes de solicitar o `urlPostApplyModifier` comandos. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | No | Comandos de protocolo de servicio de imágenes o procesamiento de imágenes para aplicar después `urlModifier` y solicitar comandos. |

**Output (setUrlModifierReturn)**

La API de IPS no devuelve una respuesta para esta operación.

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
