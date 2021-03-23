---
description: Define los campos específicos de la imagen para uno o varios recursos de imagen.
seo-description: Define los campos específicos de la imagen para uno o varios recursos de imagen.
seo-title: batchSetImageFields
solution: Experience Manager
title: batchSetImageFields
uuid: e0ad7da4-cb28-4402-8b47-a600916d23b3
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 9%

---


# batchSetImageFields{#batchsetimagefields}

Define los campos específicos de la imagen para uno o varios recursos de imagen.

Sintaxis

## Tipos de usuarios autorizados {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-4969815cf67c4d11b13bb2017b3604e8}

**Entrada (batchSetImageFields)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene los recursos de imagen. |
| `*`updateArray`*` | `types:ImageFieldUpdateArray` | Sí | La matriz de actualizaciones del campo de imagen. |

**Salida (batchSetImageFields)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sí | Número de campos de imagen establecidos correctamente. |
| `*`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó establecer los campos de imagen. |
| `*`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó establecer los campos de imagen. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó aplicar las actualizaciones. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó aplicar las actualizaciones. |

## Ejemplos {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

En este ejemplo se establecen datos en los campos de dos imágenes de una matriz de actualización. En la matriz, las imágenes se especifican mediante sus controladores de recursos y contienen resolución en píxeles, coordenadas de anclaje de posición x e y y datos del usuario. La respuesta indica que los campos de ambas imágenes se configuraron correctamente.

**Solicitar**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**Respuesta**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```

