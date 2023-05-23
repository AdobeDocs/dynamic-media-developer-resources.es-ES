---
description: Establece el objetivo de zoom asociado a una imagen de recurso. Sobrescribe los destinos de zoom existentes.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 14%

---

# setZoomTargets{#setzoomtargets}

Establece el objetivo de zoom asociado a una imagen de recurso. Sobrescribe los destinos de zoom existentes.

Sintaxis

## Tipos de usuarios autorizados {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-161f8c733cc4439f94a06e12119d4226}

**Entrada (setZoomTargetsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Manejo de la compañía. |
| assetHandle | `xsd:string` | Sí | Recurso con el objetivo de zoom que desea establecer. |
| zoomTargetArray | `types:ZoomTargetDefinitionArray` | Sí | Matriz de definiciones de destinos de zoom. |

**Salida (setZoomTargetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | Sí | El conjunto de controladores para los destinos de zoom creados por esta operación. |

## Ejemplos {#section-a2f14c7a1499443e96d099ea8a76c182}

Este ejemplo de código define una matriz de destinos de zoom por nombre, posición (eje x e y), anchura, altura y asigna la matriz a un recurso. La respuesta contiene controladores para los destinos de zoom recién creados.

**Solicitar**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**Respuesta**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```
