---
description: Condición de búsqueda de campos del sistema para la operación searchAssets.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 6%

---

# SystemFieldCondition{#systemfieldcondition}

Condición de búsqueda de campos del sistema para la operación searchAssets.

Para las comparaciones unarias, pase exactamente un valor ( `boolVal`, `longVal`, `doubleVal` o `dateVal`) según el tipo de campo del sistema. Para los intervalos de búsqueda, pase los parámetros `min<Type>` y `max<Type>` y pase un valor `op` de `Between` o `NotBetween`.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`campo`*` | `xsd:string` | Selección de los campos del sistema de búsqueda de recursos. |
| `*`op`*` | `xsd:string` | Opción de operadores de comparación de cadenas. |
| `*`basado en IP`*` | `xsd:string` | Valor con el que realizar pruebas. |
| `*`boolVal`*` | `xsd:boolean` | Valor de comparación booleano. |
| `*`longVal`*` | `xsd:long` | Valor de comparación largo. |
| `*`minLong`*` | `xsd:long` | Límite inferior de rango largo. |
| `*`maxLong`*` | `xsd:long` | Límite superior de rango largo. |
| `*`doubleVal`*` | `xsd:double` | Valor de comparación doble. |
| `*`minDouble`*` | `xsd:double` | Límite inferior de rango doble. |
| `*`maxDouble`*` | `xsd:double` | Límite superior de doble rango. |
| `*`dateVal`*` | `xsd:dateTime` | Valor de comparación de fechas. |
| `*`minDate`*` | `xsd:dateTime` | Intervalo de fechas mínimo. |
| `*`maxDate`*` | `xsd:dateTime` | Intervalo de fechas máximo. |

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
