---
description: Cambia el nombre de un recurso.
solution: Experience Manager
title: enameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 6%

---

# enameAsset{#renameasset}

Cambia el nombre de un recurso.

>[!NOTE]
>
>El parámetro `renameFiles` ha quedado obsoleto para versiones anteriores y se ha eliminado de `renameAsset`. La ruta del archivo virtual se cambia para que coincida con el nuevo nombre del recurso (conservando la extensión del archivo), mientras que las rutas de archivo físicas no se ven afectadas. Los clientes de API deben quitar las referencias a este parámetro al actualizar a la nueva versión de la API.

## Tipos de usuarios autorizados {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura al recurso.

## Parámetros {#section-ef95a994106841e0ab346dd4cf672258}

**Entrada (RenameAssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía a la que pertenece el recurso. |
| assetHandle | `xsd:string` | Sí | El identificador del recurso cuyo nombre desea cambiar. |
| newName | `xsd:string` | Sí | Nuevo nombre del recurso. |
| validateName | `xsd:boolean` | Sí | Si `validateName` es `true` y el tipo de recurso requiere un identificador de IPS único, se comprueba la exclusividad global del nuevo nombre y `renameAsset` genera un error si no es único. |

**Salida (RenameAssetReturn)**

La API de IPS no devuelve una respuesta para esta operación. Consulte la descripción del elemento `<ns1:validateName>` para obtener advertencias sobre este elemento.

## Ejemplos {#section-a0ddffd62bec42e09069f22ceb486f8a}

Este ejemplo de código cambia el nombre de un recurso

**Solicitud**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**Respuesta**

Ninguno.
