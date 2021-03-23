---
description: Condición de búsqueda de campos del sistema para la operación searchAssets.
seo-description: Condición de búsqueda de campos del sistema para la operación searchAssets.
seo-title: SystemFieldCondition
solution: Experience Manager
title: SystemFieldCondition
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

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

