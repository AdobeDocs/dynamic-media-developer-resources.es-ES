---
description: Quita los usuarios de compañía de un grupo específico.
seo-description: Quita los usuarios de compañía de un grupo específico.
seo-title: removeGroupMembers
solution: Experience Manager
title: removeGroupMembers
topic: Scene7 Image Production System API
uuid: dd0ea335-bbd0-43b1-830b-77f32dc39b12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# removeGroupMembers{#removegroupmembers}

Quita los usuarios de compañía de un grupo específico.

**Diferencias entre comandos de eliminación**

* `removeGroupMembers`:: Quita varios usuarios de un grupo.
* `removeGroupMembership`:: Quita un usuario individual de una matriz de grupos.

## Tipos de usuarios autorizados {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-b5596614a3be4ce5962455884e4636af}

**Entrada (removeGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con los usuarios con los que desea trabajar. |
| ` *`groupHandle`*` | `xsd:string` | Sí | Identificador de grupo. |
| ` *`userHandleArray`*` | `types:HandleArray` | Sí | Matriz de identificadores para usuarios cuyas pertenencias a grupos desee eliminar. |

**Salida (removeGroupMembersParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9eedac852cea46ec80de6a6928bf97ac}

Este ejemplo de código elimina a un usuario de la compañía especificada. Elimine varios usuarios de un grupo con la matriz de control de usuario.

**Solicitar**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**Respuesta**

Ninguno.
