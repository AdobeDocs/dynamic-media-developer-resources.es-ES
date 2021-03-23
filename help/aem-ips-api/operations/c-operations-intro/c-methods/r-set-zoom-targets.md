---
description: Establece el destino de zoom asociado a una imagen de recurso. Sobrescribe los destinos de zoom existentes.
seo-description: Establece el destino de zoom asociado a una imagen de recurso. Sobrescribe los destinos de zoom existentes.
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 11%

---


# setZoomTargets{#setzoomtargets}

Establece el destino de zoom asociado a una imagen de recurso. Sobrescribe los destinos de zoom existentes.

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
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`assetHandle`*` | `xsd:string` | Sí | Recurso con el destino de zoom que desea establecer. |
| `*`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Sí | Matriz de definiciones de destino de zoom. |

**Salida (setZoomTargetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`zoomTargetHandleArray`*` | `types:HandleArray` | Sí | Conjunto de controles de los destinos de zoom creados por esta operación. |

## Ejemplos {#section-a2f14c7a1499443e96d099ea8a76c182}

Este ejemplo de código define una matriz de destinos de zoom por nombre, posición (ejes x e y), ancho, alto y asigna la matriz a un recurso. La respuesta contiene controladores para los destinos de zoom recién creados.

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

