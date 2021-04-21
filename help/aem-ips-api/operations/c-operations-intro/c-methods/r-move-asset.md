---
description: Mueve un recurso a una carpeta específica.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

---


# moveAsset{#moveasset}

Mueve un recurso a una carpeta específica.

Sintaxis

## Tipos de usuarios autorizados {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-dd0bbdf293aa4563af70a91f97c861f1}

**Entrada (moveAssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Gestionar a la empresa. |
| `*`assetHandle`*` | `xsd:string` | Sí | Gestione el recurso que desee mover. |
| `*`folderHandle`*` | `xsd:string` | Sí | Gestionar en la carpeta de destino. |

**Salida (moveAssetReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-78333769f4f14e2886fdf06433c9d2ad}

Este ejemplo de código mueve un recurso a una carpeta.

**Solicitar**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Respuesta**

Ninguno.
