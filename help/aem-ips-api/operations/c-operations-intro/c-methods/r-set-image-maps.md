---
description: Define el mapa de imagen de un recurso.
seo-description: Define el mapa de imagen de un recurso.
seo-title: setImageMaps
solution: Experience Manager
title: setImageMaps
topic: Scene7 Image Production System API
uuid: 1dd7e032-34b4-464d-8ec6-7ad282d12891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# setImageMaps{#setimagemaps}

Define el mapa de imagen de un recurso.

Debe haber creado ya los mapas de imagen. Los mapas de imagen se aplican en orden de recuperación desde la matriz. Esto significa que el segundo mapa de imagen se superpone al primero, al tercero, al segundo, etc.

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de compañía. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador de recurso. |
| ` *`imageMapArray`*` | `types:ImageMapDefinitionArray` | Sí | Matriz de mapas de imagen predefinidos. |

**Salida (setImageMapsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`imageMapHandleArray`*` | `types:HandleArray` | Sí | Matriz con controles de mapa de imagen aplicados al recurso. |

## Ejemplos {#section-fe2e35662a6a4ee29cf250c9fd180371}

Este ejemplo de código establece 2 mapas de imagen para un recurso de imagen. El código especifica el tipo de forma, la región y la acción que se realiza cuando se invocan los mapas de imagen. La respuesta contiene una matriz con controladores para los mapas de imagen.

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

