---
description: Elimina usuarios de una matriz de grupos.
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---


# removeGroupMembership{#removegroupmembership}

Elimina usuarios de una matriz de grupos.

**Diferencias entre los comandos Quitar**

* `removeGroupMembers`: Quita varios usuarios de un grupo.
* `removeGroupMembership`: Quita un usuario individual de una matriz de grupos.

## Tipos de usuarios autorizados {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Entrada (removeGroupMembershipParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | No | El identificador de la empresa cuya pertenencia a grupo desea eliminar. |
| `*`groupHandleArray`*` | `types:HandleArray` | Sí | Matriz de identificadores a grupos de los que desea eliminar la empresa. |

**Salida (removeGroupMembershipReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-f8d4181170a243efb9faf5824ae96197}

Este ejemplo de código elimina a un usuario de un grupo.

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
