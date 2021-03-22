---
description: Defina o actualice el estado de publicación de uno o varios recursos. Puede establecer estados de publicación independientes para cada contexto de publicación en una empresa.
seo-description: Defina o actualice el estado de publicación de uno o varios recursos. Puede establecer estados de publicación independientes para cada contexto de publicación en una empresa.
seo-title: setAssetsContextState
solution: Experience Manager
title: setAssetsContextState
uuid: 4b94f9ea-3f7b-45ee-9381-6434f2bc4e31
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 9%

---


# setAssetsContextState{#setassetscontextstate}

Defina o actualice el estado de publicación de uno o varios recursos. Puede establecer estados de publicación independientes para cada contexto de publicación en una empresa.

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
| `*`companyHandle`*` | `xsd:string` | Sí | Gestionar a la empresa. |
| `*`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | Sí | Matriz de recursos y sus nuevos estados de publicación. |

**Salida (setAssetsContexStateReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sí | El número de recursos modificados correctamente. |
| `*`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó modificar recursos. |
| `*`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó modificar recursos. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de errores generados por los recursos cuando la operación intentó modificarlos. |

## Ejemplos {#section-283a073f3cb14bcda5abed863c538aa4}

Este ejemplo de código establece el estado de publicación de un recurso mediante `NotMarkedForPublish`.

**Solicitar**

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

