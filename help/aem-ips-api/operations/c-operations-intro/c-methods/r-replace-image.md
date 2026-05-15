---
description: Reemplaza los datos de imagen de un recurso de imagen.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
TQID: 'https://experienceleague.adobe.com/11bWPLId2s4gOVhiIFr93Ca4D-7SJ0PYHFmiSKtStjk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 14%

---

# replaceImage{#replaceimage}

Reemplaza los datos de imagen de un recurso de imagen.

Sintaxis

## Tipos de usuarios autorizados {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Entrada (replaceImageParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyName | `xsd:string` | Sí | El identificador de la compañía con la imagen que desea reemplazar. |
| assetHandle | `xsd:string` | Sí | El identificador del recurso que desea reemplazar. |
| urlModifier | `xsd:string` | Sí | Comandos del servidor de imágenes que generan nuevos datos de imagen. |

**Salida (replaceImageReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| assetHandle | `xsd:string` | Sí | Administrar en el nuevo recurso. |

## Ejemplos {#section-cebb93576bde4cb98cb27356ca66783b}

Este ejemplo de código reemplaza una imagen y aplica un `urlModifier` con un comando que especifica que el servidor de imágenes no realizará ninguna acción al reemplazar.

**Solicitud**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**Respuesta**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```
