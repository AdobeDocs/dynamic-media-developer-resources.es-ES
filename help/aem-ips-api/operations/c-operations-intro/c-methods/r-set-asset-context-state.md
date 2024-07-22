---
description: Establezca o actualice el estado de publicación para uno o varios recursos. Puede establecer estados de publicación independientes para cada contexto de publicación en una empresa.
solution: Experience Manager
title: setAssetsContextState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 28d0a67b-3e36-43fc-800d-17c841dca3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 10%

---

# setAssetsContextState{#setassetscontextstate}

Establezca o actualice el estado de publicación para uno o varios recursos. Puede establecer estados de publicación independientes para cada contexto de publicación en una empresa.

## Tipos de usuarios autorizados {#section-815eb031f85143278c1560c18c5e3431}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura para devolver el recurso.

## Parámetros {#section-009b9006de8e4c16ad657c47f28ace9f}

**Entrada (setAssetsContextStateParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Gestionar en la empresa. |
| assetsContextHandle | `types:AssetsContextStateUpdateArray` | Sí | Una matriz de recursos y sus nuevos estados de publicación. |

**Salida (setAssetsContextStateReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | `xsd:int` | Sí | El número de recursos cambiados correctamente. |
| warningCount | `xsd:int` | Sí | El número de advertencias generadas cuando la operación intentó modificar recursos. |
| errorCount | `xsd:int` | Sí | El número de errores generados cuando la operación intentó modificar recursos. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Matriz de errores generados por los recursos cuando la operación intentó modificarlos. |

## Ejemplos {#section-283a073f3cb14bcda5abed863c538aa4}

Este ejemplo de código establece el estado de publicación de un recurso mediante `NotMarkedForPublish`.

**Solicitud**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**Respuesta**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```
