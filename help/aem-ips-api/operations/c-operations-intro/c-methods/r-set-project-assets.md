---
description: Asigne o actualice recursos en un proyecto.
seo-description: Asigne o actualice recursos en un proyecto.
seo-title: setProjectAssets
solution: Experience Manager
title: setProjectAssets
uuid: 98d18948-d387-4890-9c27-e8ab60cded1d
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 17%

---


# setProjectAssets{#setprojectassets}

Asigne o actualice recursos en un proyecto.

Sintaxis

## Tipos de usuarios autorizados {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Entrada (setProjectAssetsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`projectHandle`*` | `xsd:string` | Sí | Identificador del proyecto. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sí | Matriz de controladores de recursos que desea asociar al proyecto. |

**Salida (setProjectAssetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sí | El número de recursos agregados correctamente. |

## Ejemplos {#section-33c1a909c3dc4aa98da474c23a036596}

Este ejemplo de código asigna un recurso a un proyecto. La solicitud devuelve un recuento de éxito de uno.

**Solicitar**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Respuesta**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

