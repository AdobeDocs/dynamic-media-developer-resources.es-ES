---
description: Mueve un recurso a una carpeta específica.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 14%

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
| companyHandle | `xsd:string` | Sí | Gestionar en la empresa. |
| assetHandle | `xsd:string` | Sí | Administre al recurso que desea mover. |
| folderHandle | `xsd:string` | Sí | Administrar en la carpeta de destino. |

**Salida (moveAssetReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-78333769f4f14e2886fdf06433c9d2ad}

Este ejemplo de código mueve un recurso a una carpeta.

**Solicitud**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Respuesta**

Ninguno.
