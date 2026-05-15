---
title: emptyAssetsFromTrash
description: Vacía los recursos de la papelera IPS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
TQID: 'https://experienceleague.adobe.com/y-TOHfExSc5RL9-j0f-pU6uKXWuSKSrn9SG7w0e5jPg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 6%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

Vacía los recursos de la papelera IPS.

Assets vive en la papelera hasta que se vacía manualmente o hasta que se agota el tiempo de espera de la papelera. Si se vacían manualmente, se almacenan en la papelera hasta el siguiente trabajo de limpieza (normalmente todas las noches) cuando finalmente se eliminan del sistema. Si se agota el tiempo de espera de la papelera, los recursos se limpian como parte de esa misma actividad de limpieza. El tiempo de espera es configurable (el valor predeterminado es de 7 días).

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
| companyHandle | xsd:string | Sí | El identificador de la compañía propietaria de los recursos. |
| assetHandleArray | tipos:HandleArray | Sí | Matriz de identificadores que representan los elementos que se van a eliminar de la papelera. |

**Salida (emptyAssetsFromTrashParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | xsd:Int | Sí | Número de recursos que se han eliminado correctamente de la papelera. |
| warningCount | xsd:Int | Sí | El número de advertencias generadas cuando la operación intentó vaciar recursos de la papelera. |
| errorCount | xsd:Int | Sí | El número de errores generados cuando la operación intentó vaciar recursos de la papelera. |
| warningDetailArray | tipos:AssetOperationFaultArray | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó vaciarlos de la papelera. |
| errorDetailArray | tipos:AssetOperationFaultArray | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó vaciarlos de la papelera. |

## Ejemplos {#section-6154a873b6c342bf92e2036280cafdcf}

Este ejemplo de código utiliza el identificador de la empresa y una matriz de identificadores de recursos que contiene los identificadores de los recursos que se van a eliminar de la papelera.

**Solicitud**

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
