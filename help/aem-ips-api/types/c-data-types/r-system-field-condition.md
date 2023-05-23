---
description: Condición de búsqueda de campo del sistema para la operación searchAssets.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 6%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Condición de búsqueda de campo del sistema para la operación searchAssets.

Para comparaciones unarias, pase exactamente un valor ( `boolVal`, `longVal`, `doubleVal`, o `dateVal`) según el tipo de campo del sistema. Para los intervalos de búsqueda, pase `min<Type>` y `max<Type>` parámetros y pasar un `op` valor de `Between` o `NotBetween`.

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
