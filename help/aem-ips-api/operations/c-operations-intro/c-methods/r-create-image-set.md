---
description: Crea un conjunto de imágenes.
seo-description: Crea un conjunto de imágenes.
seo-title: createImageSet
solution: Experience Manager
title: createImageSet
uuid: 688f3954-bc8f-4687-8d66-e064561cd4a0
feature: Dynamic Media Classic,SDK/API,Conjuntos de imágenes
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 14%

---


# createImageSet{#createimageset}

Crea un conjunto de imágenes.

Sintaxis

## Tipos de usuarios autorizados {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura a la carpeta de destino.

## Parámetros {#section-03d22ba7d290477e91c25ca1d4439200}

**Entrada (createImageSetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa a la que pertenece el conjunto de imágenes. |
| `*`folderHandle`*` | `xsd:string` | Sí | El identificador de la carpeta. |
| `*`name`*` | `xsd:string` | Sí | Nombre del conjunto de imágenes. |
| `*`type`*` | `xsd:string` | Sí | Tipo de conjunto de imágenes. |
| `*`thumbAssetHandle`*` | `xsd:string` | No | Control del recurso que actúa como la miniatura del nuevo conjunto de imágenes. Si no se especifica, IPS intenta utilizar el primer recurso de imagen al que hace referencia el conjunto. |

**Salida**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sí | El identificador del nuevo conjunto de imágenes. |

## Ejemplos {#section-385fe3b0af8044b0a2451336ec137fc5}

Este ejemplo de código crea un conjunto de imágenes especificado por empresa, carpeta, nombre y tipo. La respuesta es un gestor de recursos del conjunto de imágenes recién creado.

**Solicitar**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**Respuesta**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```

