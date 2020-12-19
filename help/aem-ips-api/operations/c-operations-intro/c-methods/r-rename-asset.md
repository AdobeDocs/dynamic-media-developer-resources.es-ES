---
description: Cambia el nombre de un recurso.
seo-description: Cambia el nombre de un recurso.
seo-title: changeAsset
solution: Experience Manager
title: changeAsset
topic: Scene7 Image Production System API
uuid: f285d7e4-00df-4d90-a05a-71747a4c54cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 7%

---


# RenameAsset{#renameasset}

Cambia el nombre de un recurso.

>[!NOTE]
>
>El parámetro `renameFiles` ha quedado obsoleto para versiones anteriores y se ha eliminado de `renameAsset`. La ruta de acceso del archivo virtual se cambia para que coincida con el nuevo nombre del recurso (conservando la extensión del archivo), mientras que las rutas de acceso del archivo físico no se ven afectadas. Los clientes de API deben eliminar las referencias a este parámetro al actualizar a la nueva versión de API.

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

**Entrada (cambiar el nombre de AssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía a la que pertenece el recurso. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador del recurso cuyo nombre desea cambiar. |
| ` *`newName`*` | `xsd:string` | Sí | Nombre nuevo del recurso. |
| ` *`validateName`*` | `xsd:boolean` | Sí | Si `validateName` es `true` y el tipo de recurso requiere un ID IPS único, se comprueba la unicidad global del nuevo nombre y `renameAsset` genera un error si no es único. |

**Output (RenameAssetReturn)**

La API de IPS no devuelve una respuesta para esta operación. Consulte la descripción del elemento `<ns1:validateName>` para obtener más información sobre este elemento.

## Ejemplos {#section-a0ddffd62bec42e09069f22ceb486f8a}

Este ejemplo de código cambia el nombre de un recurso

**Solicitar**

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
