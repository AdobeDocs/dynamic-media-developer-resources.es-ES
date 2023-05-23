---
description: Quita usuarios de una matriz de grupos.
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 10%

---

# removeGroupMembership{#removegroupmembership}

Quita usuarios de una matriz de grupos.

**Diferencias entre los comandos Quitar**

* `removeGroupMembers`: elimina varios usuarios de un grupo.
* `removeGroupMembership`: quita un usuario individual de una matriz de grupos.

## Tipos de usuarios autorizados {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Entrada (removeGroupMembershipParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userHandle | `xsd:string` | No | El identificador de la compañía cuya pertenencia al grupo desea eliminar. |
| groupHandleArray | `types:HandleArray` | Sí | Matriz de identificadores de los grupos de los que desea quitar la compañía. |

**Salida (removeGroupMembershipReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-f8d4181170a243efb9faf5824ae96197}

Este ejemplo de código quita un usuario de un grupo.

**Solicitar**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**Respuesta**

Ninguno.
