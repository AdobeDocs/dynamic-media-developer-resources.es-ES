---
description: Elimina una carpeta.
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
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
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa a la que pertenece la carpeta. |
| `*`folderHandle`*` | `xsd:string` | Sí | El identificador de la carpeta que se va a eliminar. |

**Salida (deleteFolderParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9d4617b322e8442d80e59be0f8714841}

Este código de ejemplo elimina una carpeta de la raíz de la empresa. Requiere un identificador de carpeta, que debe obtener de otra operación.

**Solicitar**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Ninguno.
