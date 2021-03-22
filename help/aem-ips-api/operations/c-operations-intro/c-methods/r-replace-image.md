---
description: Reemplaza los datos de imagen de un recurso de imagen.
seo-description: Reemplaza los datos de imagen de un recurso de imagen.
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
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
| `*`companyName`*` | `xsd:string` | Sí | El identificador de la empresa con la imagen que desea reemplazar. |
| `*`assetHandle`*` | `xsd:string` | Sí | El identificador del recurso que desea reemplazar. |
| `*`urlModifier`*` | `xsd:string` | Sí | Comandos del servidor de imágenes que generan nuevos datos de imagen. |

**Salida (replaceImageReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sí | Gestionar en el nuevo recurso. |

## Ejemplos {#section-cebb93576bde4cb98cb27356ca66783b}

Este ejemplo de código reemplaza una imagen y aplica un `urlModifier` con un comando que especifica que el servidor de imágenes no realizará ninguna acción tras el reemplazo.

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

