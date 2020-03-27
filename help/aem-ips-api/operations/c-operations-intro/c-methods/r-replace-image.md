---
description: Reemplaza los datos de imagen de un recurso de imagen.
seo-description: Reemplaza los datos de imagen de un recurso de imagen.
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
topic: Scene7 Image Production System API
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyName`*` | `xsd:string` | Sí | Identificador de la compañía con la imagen que desea reemplazar. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador del recurso que desea reemplazar. |
| ` *`urlModifier`*` | `xsd:string` | Sí | Comandos del servidor de imágenes que generan nuevos datos de imagen. |

**Salida (replaceImageReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Sí | Administre el nuevo recurso. |

## Ejemplos {#section-cebb93576bde4cb98cb27356ca66783b}

Este ejemplo de código reemplaza una imagen y aplica un `urlModifier` comando que especifica que el servidor de imágenes no realizará ninguna acción al reemplazarla.

**Solicitar**

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

