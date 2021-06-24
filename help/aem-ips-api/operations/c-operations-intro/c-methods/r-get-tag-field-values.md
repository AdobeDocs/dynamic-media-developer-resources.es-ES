---
description: Obtiene todos los valores de diccionario de etiquetas definidos para uno o varios campos de etiqueta.
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 12836783-4f9d-41d3-9b42-6e25238d7ed5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 17%

---

# getTagFieldValues{#gettagfieldvalues}

Obtiene todos los valores de diccionario de etiquetas definidos para uno o varios campos de etiqueta.

Sintaxis

## Tipos de usuarios autorizados {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-9ad806e7736e4d51ae42cad185050cf9}

**Entrada (getTagFieldValuesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene el campo de etiqueta. |
| `*`fieldHandleArray`*` | `types:HandleArray` | Sí | Matriz de identificadores de campo para etiquetar valores que desea que se devuelvan. |

**Salida (getTagFieldValuesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`fieldArray`*` | `types:TagFieldValuesArray` | Sí | Matriz de los valores de etiqueta del diccionario para cada campo solicitado. |

## Ejemplos {#section-4492742614e44bb191a7d397dc1a1407}

**Solicitar**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**Respuesta**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```
