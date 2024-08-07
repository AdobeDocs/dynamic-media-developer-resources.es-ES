---
description: Elimina una carpeta.
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 10%

---

# deleteFolder{#deletefolder}

Elimina una carpeta.

Sintaxis

## Tipos de usuarios autorizados {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y eliminación a la carpeta y a todos sus elementos secundarios.

## Parámetros {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Entrada (deleteFolderParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía a la que pertenece la carpeta. |
| folderHandle | `xsd:string` | Sí | El identificador de la carpeta que se va a eliminar. |

**Salida (deleteFolderParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9d4617b322e8442d80e59be0f8714841}

Este código de ejemplo elimina una carpeta de la raíz de la compañía. Requiere un identificador de carpeta, que debe obtener de otra operación.

**Solicitud**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Ninguno.
