---
description: Añade usuarios de una compañía específica a un grupo específico.
solution: Experience Manager
title: addGroupMembers
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---


# addGroupMembers{#addgroupmembers}

Añade usuarios de una compañía específica a un grupo específico.

Sintaxis

## Tipos de usuarios autorizados {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-b28434dcf2ca4b4ea431136aac33913e}

**Entrada (addGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la compañía. |
| `*`groupHandle`*` | `xsd:string` | Sí | El identificador del grupo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sí | Matriz de identificadores para los usuarios que desea agregar a un grupo. |

**Salida (addGroupMembersParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-8f168b528aef4c4fa8c3d41f7686842f}

Este ejemplo utiliza `*`addGroupMembersParam`*` para agregar un usuario a una sola compañía. La API de IPS no devuelve una respuesta para esta operación.

**Solicitar**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Respuesta**

Ninguno.
