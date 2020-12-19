---
description: Devuelve información sobre la estructura de una compañía (número de archivos, etc.).
seo-description: Devuelve información sobre la estructura de una compañía (número de archivos, etc.).
seo-title: getDiskUsage
solution: Experience Manager
title: getDiskUsage
topic: Scene7 Image Production System API
uuid: 29190200-8f49-4689-9782-1df665dca1b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 12%

---


# getDiskUsage{#getdiskusage}

Devuelve información sobre la estructura de una compañía (número de archivos, etc.).

## Tipos de usuarios autorizados {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía cuyo uso de disco desea obtener. |

**Salida (getDiskUsageReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`diskUsageArray`*` | `types:DiskUsageArray` | Sí | Matriz de uso del disco de compañía. |

## Ejemplos {#section-cb16a97badc94076ad5da277db5ed16a}

El nombre de esta solicitud es engañoso. En lugar de devolver simplemente un valor escalar que refleja cuánto espacio de disco está utilizando una compañía, obtiene también otra información sobre la estructura de una compañía.

**Solicitar**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**Respuesta**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```

