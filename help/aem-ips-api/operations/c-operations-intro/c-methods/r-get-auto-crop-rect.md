---
description: Devuelve una región recortada para una imagen en función de su color de fondo o transparencia.
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
TQID: 'https://experienceleague.adobe.com/cDQ-P-vZGfOyPASRMfemIKnphk5GavTU85m4vJq83bc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 152
ht-degree: 13%

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
>Especifique autoColorCropOptions o autoTransparentCropOptions al llamar a este método.

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía con el recurso con el que desea trabajar. |
| assetHandle | `xsd:string` | Sí | El identificador del recurso con el que desea trabajar. |
| autoColorCropOptions | `types:AutoColorCropOptions` | No | Calcular rectángulo de recorte en función del color. Consulte [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | No | Calcular rectángulo de recorte en función de la transparencia. Consulte [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Salida (getAutoCropRectReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| xOffset | `xsd:int` | Sí | Coordenada inicial en píxeles izquierdos de la región de recorte calculada. |
| Desplazamiento | `xsd:int` | Sí | Coordenada del píxel superior inicial de la región de recorte calculada. |
| ancho | `xsd:int` | Sí | Ancho de la región de recorte calculada (en píxeles). |
| altura | `xsd:int` | Sí | Altura de la región de recorte calculada (en píxeles). |

## Ejemplos {#section-ba65bd66086d491cad1cea535954ee1f}

**Solicitud**

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
