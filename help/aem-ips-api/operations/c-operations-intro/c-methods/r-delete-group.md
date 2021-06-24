---
description: Elimina un grupo.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que pertenece al grupo que desea eliminar. |
| `*`groupHandle`*` | `xsd:string` | Sí | El identificador del grupo que desea eliminar. |

**Salida (deleteGroupParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Este código de ejemplo elimina un grupo de una empresa. Requiere un identificador de grupo, que debe obtener de otra operación.

**Solicitar**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Respuesta**

Ninguno.
