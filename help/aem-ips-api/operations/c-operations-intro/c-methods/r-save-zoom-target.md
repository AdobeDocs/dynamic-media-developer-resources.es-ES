---
description: Cree o edite un destino de zoom.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 20%

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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con el destino de zoom que desea guardar. |
| `*`assetHandle`*` | `xsd:string` | Sí | Control del destino de zoom. |
| `*`zoomTargetHandle`*` | `xsd:string` | No | Edita o crea un destino de zoom. |
| `*`name`*` | `xsd:string` | Sí | Nombre del destino de zoom. |
| `*`xPosition`*` | `xsd:int` | Sí | Ubicación en píxeles a la izquierda. |
| `*`yPosition`*` | `xsd:int` | Sí | Ubicación en píxeles superior. |
| `*`width`*` | `xsd:int` | Sí | Zoom de la anchura de destino. |
| `*`height`*` | `xsd:int` | Sí | Zoom de la altura de destino. |
| `*`Datos de usuario`*` | `xsd:string` | Sí | Para obtener información específica del cliente. Puede contener cualquier tipo de datos. |

**Salida (saveZoomTargetReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | Sí | Gestione el objetivo de zoom recién creado. |

## Ejemplos {#section-509c472c316549cdb228d7e1cfa8400a}

Este ejemplo de código guarda un objetivo de zoom. La respuesta devuelve el controlador de destino de zoom.

**Solicitar**

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

