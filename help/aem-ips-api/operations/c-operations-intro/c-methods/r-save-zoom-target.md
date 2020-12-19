---
description: Cree o edite un destinatario de zoom.
seo-description: Cree o edite un destinatario de zoom.
seo-title: saveZoomTarget
solution: Experience Manager
title: saveZoomTarget
topic: Scene7 Image Production System API
uuid: 197f7a2a-39ea-41cc-8e3a-76f9fe1b37d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 20%

---


# saveZoomTarget{#savezoomtarget}

Cree o edite un destinatario de zoom.

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con el destinatario de zoom que desea guardar. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Control del destinatario de zoom. |
| ` *`zoomTargetHandle`*` | `xsd:string` | No | Edita o crea un destinatario de zoom. |
| ` *`name`*` | `xsd:string` | Sí | Nombre del destinatario de zoom. |
| ` *`xPosition`*` | `xsd:int` | Sí | Ubicación del píxel izquierdo. |
| ` *`yPosition`*` | `xsd:int` | Sí | Ubicación en píxeles superior. |
| ` *`width`*` | `xsd:int` | Sí | Zoom de anchura de destinatario. |
| ` *`height`*` | `xsd:int` | Sí | Altura del destinatario de zoom. |
| ` *`Datos de usuario`*` | `xsd:string` | Sí | Para obtener información específica del cliente. Puede contener cualquier tipo de datos. |

**Salida (saveZoomTargetReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`zoomTargetHandle`*` | `xsd:string` | Sí | Controlar el destinatario de zoom recién creado. |

## Ejemplos {#section-509c472c316549cdb228d7e1cfa8400a}

Este ejemplo de código guarda un destinatario de zoom. La respuesta devuelve el control de destinatario de zoom.

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

