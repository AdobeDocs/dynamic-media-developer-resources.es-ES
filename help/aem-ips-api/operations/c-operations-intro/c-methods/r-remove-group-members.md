---
description: Quita a los usuarios de la empresa de un grupo específico.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 9%

---


# removeGroupMembers{#removegroupmembers}

Quita a los usuarios de la empresa de un grupo específico.

**Diferencias entre los comandos Quitar**

* `removeGroupMembers`: Quita varios usuarios de un grupo.
* `removeGroupMembership`: Quita un usuario individual de una matriz de grupos.

## Tipos de usuarios autorizados {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-b5596614a3be4ce5962455884e4636af}

**Entrada (removeGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con los usuarios con los que desea trabajar. |
| `*`groupHandle`*` | `xsd:string` | Sí | Identificador de grupo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sí | Matriz de controladores para usuarios cuyas pertenencias de grupo desee eliminar. |

**Salida (removeGroupMembersParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9eedac852cea46ec80de6a6928bf97ac}

Este ejemplo de código elimina a un usuario de la empresa especificada. Elimine varios usuarios de un grupo con la matriz de control de usuario.

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
