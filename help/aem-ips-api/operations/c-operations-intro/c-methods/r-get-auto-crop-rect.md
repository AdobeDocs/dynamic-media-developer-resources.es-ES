---
description: Devuelve una región recortada para una imagen en función de su color de fondo o transparencia.
seo-description: Devuelve una región recortada para una imagen en función de su color de fondo o transparencia.
seo-title: getAutoCropRect
solution: Experience Manager
title: getAutoCropRect
topic: Scene7 Image Production System API
uuid: bb00d89a-5fc4-476f-aa47-3cf69ef99afe
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# getAutoCropRect{#getautocroprect}

Devuelve una región recortada para una imagen en función de su color de fondo o transparencia.

Sintaxis

## Tipos de usuarios autorizados {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**Entrada (getAutoCropRectParam)**

>[!NOTE]
>
>Especifique ` *`autoColorCropOptions`*` o ` *`autoTransparentCropOptions`*` al llamar a este método.

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con el recurso con el que desea trabajar. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador del recurso con el que se desea trabajar. |
| ` *`autoColorCropOptions`*` | `types:AutoColorCropOptions` | No | Calcular rectángulo de recorte basado en color. Consulte [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| ` *`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | No | Calcular rectángulo de recorte en función de la transparencia. Consulte [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Salida (getAutoCropRectReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`xOffset`*` | `xsd:int` | Sí | Coordenada inicial de píxeles izquierda de la región de recorte calculada. |
| ` *`yOffset`*` | `xsd:int` | Sí | Coordenada de píxeles superior inicial de la región de recorte calculada. |
| ` *`width`*` | `xsd:int` | Sí | Anchura de la región de recorte calculada (en píxeles). |
| ` *`height`*` | `xsd:int` | Sí | Altura de la región de recorte calculada (en píxeles). |

## Ejemplos {#section-ba65bd66086d491cad1cea535954ee1f}

**Solicitar**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**Respuesta**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

