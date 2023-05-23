---
description: Establece los comandos del protocolo de servicio o procesamiento de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

Establece los comandos del protocolo de servicio o procesamiento de imágenes para el recurso especificado. Estos comandos modifican la representación del recurso sin destruirlo.

Para el servicio de imágenes, los comandos del `urlModifier` Los parámetros de se publican en el campo Modifier catalog y se aplican antes de cualquier comando especificado en la URL de la solicitud. Comandos en `urlPostApplyModifier` se publican en el `PostModifier` catálogo y omita cualquier comando de la dirección URL de la solicitud o del `urlModifier`. Para el procesamiento de imágenes, los comandos de `urlModifier` y `urlPostApplyModifier` se concatenan y publican en el campo Modifier catalog.

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
| urlModifier | `xsd:string` | No | Comandos del protocolo de servicio o procesamiento de imágenes que se aplicarán antes de la solicitud o `urlPostApplyModifier` comandos. |
| urlPostApplyModifier | `xsd:string` | No | Comandos de protocolo de servicio o procesamiento de imágenes para aplicar después de `urlModifier` y solicitar comandos. |

**Salida (setUrlModifierReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Solicitar**

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
