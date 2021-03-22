---
description: Elimina usuarios de una matriz de grupos.
seo-description: Elimina usuarios de una matriz de grupos.
seo-title: removeGroupMembership
solution: Experience Manager
title: removeGroupMembership
uuid: 553d91a3-73d6-4323-9436-a3ba13260a6c
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 9%

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
