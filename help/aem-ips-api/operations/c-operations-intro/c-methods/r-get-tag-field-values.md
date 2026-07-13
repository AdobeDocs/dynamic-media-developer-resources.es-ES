---
description: Obtiene todos los valores de diccionario de etiquetas definidos para uno o varios campos de etiqueta.
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 12836783-4f9d-41d3-9b42-6e25238d7ed5
TQID: 'https://experienceleague.adobe.com/b7chzlIT9c4eWbl-MEVgdmvpymwnOieDHgm3a-lMnH4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 16%

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
| companyHandle | `xsd:string` | Sí | El identificador de la compañía que contiene el campo de etiqueta. |
| fieldHandleArray | `types:HandleArray` | Sí | Una matriz de identificadores de campo para etiquetar los valores que desee devolver. |

**Salida (getTagFieldValuesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| fieldArray | `types:TagFieldValuesArray` | Sí | Una matriz de los valores de etiqueta del diccionario para cada campo solicitado. |

## Ejemplos {#section-4492742614e44bb191a7d397dc1a1407}

**Solicitud**

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

