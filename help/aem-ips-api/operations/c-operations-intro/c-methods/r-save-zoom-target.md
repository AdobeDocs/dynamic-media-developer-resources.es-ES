---
description: Cree o edite un destino de zoom.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
TQID: 'https://experienceleague.adobe.com/rw-joRwkyumLI261ifPiWTeIgy4mvx-4MpgmaKcX5-E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 19%

---

# saveZoomTarget{#savezoomtarget}

Cree o edite un destino de zoom.

Sintaxis

## Tipo de usuario autorizado {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-4a23983cae4e49a098e9bbe736933996}

**Entrada (saveZoomTargetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la empresa con el destino de zoom que desea guardar. |
| assetHandle | `xsd:string` | Sí | El controlador para el destino de zoom. |
| zoomTargetHandle | `xsd:string` | No | Edita o crea un destino de zoom. |
| nombre | `xsd:string` | Sí | Nombre del destino de zoom. |
| xPosition | `xsd:int` | Sí | Ubicación del píxel izquierdo. |
| yPosition | `xsd:int` | Sí | Ubicación de píxel superior. |
| ancho | `xsd:int` | Sí | Anchura del destino de zoom. |
| altura | `xsd:int` | Sí | Altura de destino de zoom. |
| userData | `xsd:string` | Sí | Para obtener información específica del cliente. Puede contener cualquier tipo de datos. |

**Salida (saveZoomTargetReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| zoomTargetHandle | `xsd:string` | Sí | Manejar al destino de zoom recién creado. |

## Ejemplos {#section-509c472c316549cdb228d7e1cfa8400a}

Este ejemplo de código guarda un destino de zoom. La respuesta devuelve el controlador de destinos de zoom.

**Solicitud**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**Respuesta**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```

