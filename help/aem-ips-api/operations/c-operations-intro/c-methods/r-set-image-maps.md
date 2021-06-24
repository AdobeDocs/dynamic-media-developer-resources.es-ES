---
description: Define el mapa de imagen de un recurso.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 10%

---

# setImageMaps{#setimagemaps}

Define el mapa de imagen de un recurso.

Ya debe haber creado los mapas de imágenes. Los mapas de imágenes se aplican en orden de recuperación desde la matriz. Esto significa que el segundo mapa de imagen superpone el primero, el tercero superpone el segundo, etc.

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
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`assetHandle`*` | `xsd:string` | Sí | Identificador de recurso. |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | Sí | Matriz de mapas de imágenes predefinidos. |

**Salida (setImageMapsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | Sí | Matriz con controladores de mapa de imagen aplicados al recurso. |

## Ejemplos {#section-fe2e35662a6a4ee29cf250c9fd180371}

Este ejemplo de código establece 2 mapas de imagen para un recurso de imagen. El código especifica el tipo de forma, la región y la acción que se realizan cuando se invocan los mapas de imagen. La respuesta contiene una matriz con identificadores para los mapas de imágenes.

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
