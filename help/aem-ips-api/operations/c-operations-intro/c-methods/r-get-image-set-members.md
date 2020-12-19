---
description: Obtiene una matriz de miembros que están en un conjunto de imágenes.
seo-description: Obtiene una matriz de miembros que están en un conjunto de imágenes.
seo-title: getImageSetMembers
solution: Experience Manager
title: getImageSetMembers
topic: Scene7 Image Production System API
uuid: b19c9fec-df92-42e1-9228-42cdf196fdfc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 15%

---


# getImageSetMembers{#getimagesetmembers}

Obtiene una matriz de miembros que están en un conjunto de imágenes.

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
>Requiere acceso de lectura a la imagen y al recurso de conjunto de miembros.

## Parámetros {#section-a67ba98095574533980997c83ceaa316}

**Entrada (getImageSetMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que contiene el conjunto de imágenes. |
| ` *`assetHandle`*` | `xsd:string` | Sí | El control de recurso del conjunto de imágenes. |

**Salida (getImageSetMembersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`miembroArray`*` | `types:ImageSetMemberArray` | No | Matriz de miembros del conjunto de imágenes. |

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

