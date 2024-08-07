---
description: Agrega uno o más recursos a un proyecto.
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 10%

---

# addProjectAssets{#addprojectassets}

Agrega uno o más recursos a un proyecto.

Sintaxis

## Tipos de usuarios autorizados {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-20d498e971b6466298e60c8a77fc32b2}

**Entrada (addProjectAssetsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Administrar a la compañía asociada con el proyecto actual. |
| projectHandle | `xsd:string` | Sí | Administre al proyecto al que está agregando recursos. |
| projectHandleArray | `xsd:HandleArray` | Sí | Matriz de recursos que está agregando al proyecto actual. |

**Salida (addProjectAssetsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | `xsd:int` | Sí | El número de recursos añadidos correctamente. |
| warningCount | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó agregar recursos a un proyecto. |
| errorCount | `xsd:int` | Sí | Número de errores generados cuando la operación intentó agregar recursos a un proyecto. |
| warningDetailHandle | `xsd:AssetOperationFaultArray` | No | Matriz de advertencias generadas por los recursos cuando la operación intentó agregarlas a un proyecto. |
| companyHandle | `xsd:AssetOperationFaultArray` | No | Matriz de errores generados por los recursos cuando la operación intentó agregarlos a un proyecto. |

## Ejemplos {#section-bee5be2402f54cb9a3a02cc07def4135}

En este ejemplo se agrega un solo recurso (al que se hace referencia mediante su identificador) en una matriz de identificadores de recursos a un proyecto especificado en la solicitud. La operación se completó correctamente cuando la respuesta `successCount` devuelve `1`.

**Solicitud**

```java {.line-numbers}
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Respuesta**

```java {.line-numbers}
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```
