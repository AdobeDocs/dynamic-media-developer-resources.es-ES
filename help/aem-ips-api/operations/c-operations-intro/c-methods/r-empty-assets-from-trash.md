---
title: emptyAssetsFromTrash
description: Vacía recursos de la papelera IPS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 8%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

Vacía recursos de la papelera IPS.

Los activos viven en la basura hasta que se vacían manualmente o hasta que salen de la basura. Si se vacian manualmente, viven en la Papelera hasta el siguiente trabajo de limpieza (normalmente por la noche) cuando finalmente se depuran del sistema. Si se agota el tiempo de espera de la papelera, los recursos se limpian como parte de la misma actividad de limpieza. El tiempo de espera es configurable (el valor predeterminado es de 7 días).

## Tipos de usuarios autorizados {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-8e1fb0ee3aae453581e99ef76e298569}

**Entrada (emptyAssetsFromTrashParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | xsd:string | Sí | El identificador de la empresa propietaria de los activos. |
| assetHandleArray | tipos:HandleArray | Sí | Matriz de controladores que representan los elementos que se van a vaciar de la papelera. |

**Salida (emptyAssetsFromTrashParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | xsd:Int | Sí | El número de recursos vaciados correctamente de la basura. |
| warningCount | xsd:Int | Sí | Número de advertencias generadas cuando la operación intentó vaciar recursos de la papelera. |
| errorCount | xsd:Int | Sí | Número de errores generados cuando la operación intentó vaciar recursos de la papelera. |
| warningDetailArray | tipos:AssetOperationFaultArray | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó vaciarlos de la papelera. |
| errorDetailArray | tipos:AssetOperationFaultArray | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó vaciarlos de la papelera. |

## Ejemplos {#section-6154a873b6c342bf92e2036280cafdcf}

Este ejemplo de código utiliza el identificador de la empresa y una matriz de control de recursos que contiene los identificadores de los recursos que se van a vaciar de la papelera.

**Solicitar**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Respuesta**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
