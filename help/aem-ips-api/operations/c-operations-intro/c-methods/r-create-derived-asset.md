---
description: Crea un nuevo recurso derivado de un recurso de imagen de origen principal existente.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

Crea un nuevo recurso derivado de un recurso de imagen de origen principal existente.

Sintaxis

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Los recursos derivados especifican comandos de protocolo del servidor de imágenes que modifican la representación de la imagen del propietario. El tipo derivado `AdjustedView` ayuda a aplicar modificaciones simples a una sola imagen (por ejemplo, especificando un rectángulo de recorte), mientras que `LayerView` ayuda a crear una vista de varias capas que puede incluir texto o imágenes adicionales.

A diferencia de una copia de imagen (consulte [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), una imagen derivada está vinculada a su imagen de propietario. Los cambios en la imagen de propietario modifican los recursos derivados asociados. Al eliminar la imagen de propietario, se eliminan todas las imágenes derivadas asociadas.

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
| companyHandle | `xsd:string` | Sí | El identificador de la compañía que contiene el recurso del que se deriva el nuevo recurso. |
| ownerHandle | `xsd:string` | Sí | El identificador del recurso de imagen principal del que se deriva la nueva imagen. |
| folderHandle | `xsd:string` | Sí | El identificador de la carpeta en la que se crea el nuevo recurso derivado. |
| nombre | `xsd:string` | Sí | Nombre del recurso derivado. |
| tipo | `xsd:string` | Sí | El tipo de recurso del nuevo recurso derivado: `AdjustedView` o `LayerView`. |
| urlModifier | `xsd:string` | No | Los comandos del protocolo de servicio de imágenes o de procesamiento de imágenes se aplicaron *antes de* la solicitud de `urlPostApplyModifier` comandos. |
| urlPostApplyModifier | `xsd:string` | No | Los comandos del protocolo de servicio de imágenes o de procesamiento de imágenes se aplicaron *después de* a la solicitud o a los comandos de `urlPostApplyModifier`. |

**Salida (createDerivedAssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| assetHandle | `xsd:string` | Sí | El identificador del recurso derivado. |

## Ejemplos {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

El código de ejemplo crea un recurso derivado con una vista ajustada y `urlModifier` y `urlPostApplyModifier` con valores arbitrarios. La respuesta devuelve el identificador al recurso recién derivado.

**Solicitud**

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
