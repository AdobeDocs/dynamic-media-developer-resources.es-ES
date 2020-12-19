---
description: Elimina una carpeta.
seo-description: Elimina una carpeta.
seo-title: deleteFolder
solution: Experience Manager
title: deleteFolder
topic: Scene7 Image Production System API
uuid: 76af65fb-86ef-43e2-bfec-3682acf0afe6
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 11%

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía a la que pertenece la carpeta. |
| ` *`folderHandle`*` | `xsd:string` | Sí | Identificador de la carpeta que se va a eliminar. |

**Salida (deleteFolderParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9d4617b322e8442d80e59be0f8714841}

Este código de muestra elimina una carpeta de la raíz de la compañía. Requiere un identificador de carpeta, que debe obtener de otra operación.

**Solicitar**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Ninguno.
