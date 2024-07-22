---
description: Devuelve información sobre la estructura de una empresa (número de archivos, etc.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 11%

---

# getDiskUsage{#getdiskusage}

Devuelve información sobre la estructura de una empresa (número de archivos, etc.).

## Tipos de usuarios autorizados {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Entrada (getDiskUsageParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía cuyo uso de disco desea obtener. |

**Salida (getDiskUsageReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| diskUsageArray | `types:DiskUsageArray` | Sí | Matriz de usuarios del disco de la empresa. |

## Ejemplos {#section-cb16a97badc94076ad5da277db5ed16a}

El nombre de esta solicitud es engañoso. En lugar de devolver simplemente un valor escalar que refleje cuánto espacio en disco está utilizando una empresa, también obtiene otra información sobre la estructura de una empresa.

**Solicitud**

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
