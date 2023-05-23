---
description: Establece el mapa de imagen de un recurso.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 11%

---

# setImageMaps{#setimagemaps}

Establece el mapa de imagen de un recurso.

Ya debe haber creado los mapas de imagen. Los mapas de imagen se aplican en orden de recuperación desde la matriz. Esto significa que el segundo mapa de imagen se superpone al primero, el tercero se superpone al segundo, etc.

## Tipos de usuarios autorizados {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-2292ec1aead947ef8741dd0653a41f42}

**Entrada (setImageMapsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Manejo de la compañía. |
| assetHandle | `xsd:string` | Sí | Controlador de recurso. |
| imageMapArray | `types:ImageMapDefinitionArray` | Sí | Matriz de mapas de imagen predefinidos. |

**Salida (setImageMapsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | Sí | Matriz con identificadores de mapa de imagen aplicados al recurso. |

## Ejemplos {#section-fe2e35662a6a4ee29cf250c9fd180371}

Este ejemplo de código establece 2 mapas de imagen para un recurso de imagen. El código especifica el tipo de forma, la región y las acciones que se realizarán cuando se invoquen los mapas de imagen. La respuesta contiene una matriz con controladores para los mapas de imagen.

**Solicitar**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```
