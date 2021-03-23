---
description: Obtiene una matriz de miembros que se encuentran en un conjunto de imágenes.
seo-description: Obtiene una matriz de miembros que se encuentran en un conjunto de imágenes.
seo-title: getImageSetMembers
solution: Experience Manager
title: getImageSetMembers
uuid: b19c9fec-df92-42e1-9228-42cdf196fdfc
feature: Dynamic Media Classic,SDK/API,Conjuntos de imágenes
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 13%

---


# getImageSetMembers{#getimagesetmembers}

Obtiene una matriz de miembros que se encuentran en un conjunto de imágenes.

Sintaxis

## Tipos de usuarios autorizados {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Requiere acceso de lectura a la imagen y al recurso del conjunto de miembros.

## Parámetros {#section-a67ba98095574533980997c83ceaa316}

**Entrada (getImageSetMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene el conjunto de imágenes. |
| `*`assetHandle`*` | `xsd:string` | Sí | El controlador de recurso del conjunto de imágenes. |

**Salida (getImageSetMembersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`memberArray`*` | `types:ImageSetMemberArray` | No | Matriz de miembros del conjunto de imágenes. |

## Ejemplos {#section-888a9a78033346f39b171229de93dfa0}

Este ejemplo de código devuelve miembros específicos del conjunto de imágenes. La respuesta devuelve una matriz vacía.

**Solicitar**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**Respuesta**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```

