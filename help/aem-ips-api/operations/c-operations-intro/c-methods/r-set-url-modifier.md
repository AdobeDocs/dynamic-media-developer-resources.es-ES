---
description: Establece los comandos del protocolo de servicio o procesamiento de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
TQID: 'https://experienceleague.adobe.com/dcz-gnw7NjHKN7EvsGvSRDmu4dgCUo2PPr3GjYLVoOA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 6%

---

# setUrlModifier{#seturlmodifier}

Establece los comandos del protocolo de servicio o procesamiento de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.

Para el servicio de imágenes, los comandos del parámetro `urlModifier` se publican en el campo Modifier catalog y se aplican antes de cualquier comando especificado en la URL de la solicitud. Los comandos de `urlPostApplyModifier` se publican en el campo de catálogo `PostModifier` y anulan cualquier comando de la dirección URL de la solicitud o de `urlModifier`. Para Image Rendering, los comandos de `urlModifier` y `urlPostApplyModifier` se concatenan y se publican en el campo Modifier catalog.

## Tipos de usuarios autorizados {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Entrada (setUrlModifierParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Manejo de la compañía. |
| assetHandle | `xsd:string` | Sí | Controlador de recurso. |
| urlModifier | `xsd:string` | No | Comandos de protocolo de servicio o procesamiento de imágenes que se aplicarán antes de la solicitud o de `urlPostApplyModifier` comandos. |
| urlPostApplyModifier | `xsd:string` | No | Comandos de protocolo de servicio o procesamiento de imágenes para aplicar después de `urlModifier` y solicitar comandos. |

**Salida (setUrlModifierReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Solicitud**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**Respuesta**

Ninguno.
