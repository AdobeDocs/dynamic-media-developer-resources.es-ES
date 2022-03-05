---
description: Crea un nuevo recurso derivado de un recurso de imagen de origen principal existente.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

Crea un nuevo recurso derivado de un recurso de imagen de origen principal existente.

Sintaxis

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Los recursos derivados especifican comandos de protocolo del servidor de imágenes que modifican la representación de la imagen del propietario. La variable `AdjustedView` el tipo derivado ayuda a aplicar modificaciones simples a una sola imagen (por ejemplo, especificando un rectángulo de recorte), mientras que la variable `LayerView` ayuda a crear una vista de varias capas que puede incluir texto o imágenes adicionales.

A diferencia de una copia de imagen (consulte [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), una imagen derivada está vinculada a su imagen de propietario. Los cambios realizados en la imagen del propietario modifican los recursos derivados asociados. Al eliminar la imagen del propietario, se eliminarán las imágenes derivadas asociadas.

## Tipos de usuarios autorizados {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-5a0dde01cff6454da3646ea805c2be1e}

**Entrada (createDerivedAssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene el recurso del que derivará el nuevo recurso. |
| `*`ownerHandle`*` | `xsd:string` | Sí | El identificador del recurso de imagen principal del que se deriva la nueva imagen. |
| `*`folderHandle`*` | `xsd:string` | Sí | El identificador de la carpeta en la que se crea el nuevo recurso derivado. |
| `*`name`*` | `xsd:string` | Sí | Nombre del recurso derivado. |
| `*`type`*` | `xsd:string` | Sí | El tipo de recurso del nuevo recurso derivado: `AdjustedView` o `LayerView`. |
| `*`urlModifier`*` | `xsd:string` | No | Comandos de protocolo de servicio o representación de imágenes aplicados *before* la solicitud o `urlPostApplyModifier` comandos. |
| `*`urlPostApplyModifier`*` | `xsd:string` | No | Comandos de protocolo de servicio o representación de imágenes aplicados *after* a la solicitud o `urlPostApplyModifier` comandos. |

**Salida (createDerivedAssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sí | El identificador del recurso derivado. |

## Ejemplos {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

El código de ejemplo crea un recurso derivado con una vista ajustada y `urlModifier` y `urlPostApplyModifier` con valores arbitrarios. La respuesta devuelve el identificador al recurso recién derivado.

**Solicitar**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**Respuesta**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```
