---
description: Condición de búsqueda de campo del sistema para la operación searchAssets.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
TQID: 'https://experienceleague.adobe.com/dCZl4pLGuG5hHpEq04W-qv8mRWcFiA7PvmzcO7Un-sM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 6%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Condición de búsqueda de campo del sistema para la operación searchAssets.

Para comparaciones unarias, pase exactamente un valor ( `boolVal`, `longVal`, `doubleVal` o `dateVal`) según el tipo de campo del sistema. Para los intervalos de búsqueda, pase los parámetros `min<Type>` y `max<Type>` y pase un valor `op` de `Between` o `NotBetween`.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| campo | `xsd:string` | Selección de los campos del sistema de búsqueda de recursos. |
| op | `xsd:string` | Opción de operadores de comparación de cadenas. |
| valor | `xsd:string` | Valor con el que probar. |
| boolVal | `xsd:boolean` | Valor de comparación booleano. |
| longVal | `xsd:long` | Valor de comparación largo. |
| minLong | `xsd:long` | Límite inferior de largo alcance. |
| maxLong | `xsd:long` | Límite superior de largo alcance. |
| doubleVal | `xsd:double` | Valor de comparación doble. |
| minDouble | `xsd:double` | Límite inferior de rango doble. |
| maxDouble | `xsd:double` | Límite superior de rango doble. |
| dateVal | `xsd:dateTime` | Valor de comparación de fecha. |
| minDate | `xsd:dateTime` | Intervalo de fecha mínimo. |
| maxDate | `xsd:dateTime` | Intervalo de fecha máximo. |

## Ejemplo {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```
