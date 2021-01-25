---
description: Elimina un grupo.
seo-description: Elimina un grupo.
seo-title: deleteGroup
solution: Experience Manager
title: deleteGroup
topic: Dynamic Media Image Production System API
uuid: 04934b16-b7ef-4657-9f63-c91fcc741ca4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 13%

---


# deleteGroup{#deletegroup}

Elimina un grupo.

Sintaxis

## Tipos de usuarios autorizados {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-42775102ec724c36ae5241eea1a00b8e}

**Entrada (deleteGroupParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que pertenece al grupo que desea eliminar. |
| `*`groupHandle`*` | `xsd:string` | Sí | Identificador del grupo que desea eliminar. |

**Salida (deleteGroupParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Este código de muestra elimina un grupo de una compañía. Requiere un identificador de grupo, que debe obtener de otra operación.

**Solicitar**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Respuesta**

Ninguno.
