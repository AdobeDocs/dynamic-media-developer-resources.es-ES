---
description: Vacía recursos de la papelera IPS.
seo-description: Vacía recursos de la papelera IPS.
seo-title: emptyAssetsFromTrash
solution: Experience Manager
title: emptyAssetsFromTrash
topic: Scene7 Image Production System API
uuid: de11a7b0-cd4b-4717-8596-d39afbcf7e9c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

Vacía recursos de la papelera IPS.

Los recursos viven en la basura hasta que se vacían manualmente o hasta que se agotan. Si se vacian manualmente, viven en la papelera hasta el siguiente trabajo de limpieza (normalmente por la noche) cuando finalmente se purgan del sistema. Si pierden el tiempo de la basura, los recursos se limpian como parte de la misma actividad de limpieza. El tiempo de espera se puede configurar (el valor predeterminado es de 7 días).

## Tipos de usuarios autorizados {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* ``

## Parámetros {#section-8e1fb0ee3aae453581e99ef76e298569}

**Entrada (emptyAssetsFromTrashParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía propietaria de los recursos. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Sí | Matriz de controladores que representan los elementos que se van a vaciar de la papelera. |

**Salida (emptyAssetsFromTrashParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`successCount`*` | `xsd:Int` | Sí | Número de recursos vaciados correctamente de la papelera. |
| ` *`warningCount`*` | `xsd:Int` | Sí | Número de advertencias generadas cuando la operación intentó vaciar recursos de la papelera. |
| ` *`errorCount`*` | `xsd:Int` | Sí | Número de errores generados cuando la operación intentó vaciar recursos de la papelera. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados a los recursos que generaron advertencias cuando la operación intentó vaciarlos de la papelera. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados a los recursos que generaron errores cuando la operación intentó vaciarlos de la papelera. |

## Ejemplos {#section-6154a873b6c342bf92e2036280cafdcf}

Este ejemplo de código utiliza el identificador de la compañía y una matriz de control de recursos que contiene los identificadores de los recursos que se van a vaciar de la papelera.

**Solicitar**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Respuesta**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```

