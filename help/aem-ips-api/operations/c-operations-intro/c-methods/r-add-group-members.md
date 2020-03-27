---
description: Añade usuarios de una compañía específica a un grupo específico.
seo-description: Añade usuarios de una compañía específica a un grupo específico.
seo-title: addGroupMembers
solution: Experience Manager
title: addGroupMembers
topic: Scene7 Image Production System API
uuid: 382d36a8-7c93-48e6-a54b-425c5e6414fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sí | El identificador de la compañía. |
| ` *`groupHandle`*` | `xsd:string` | Sí | El identificador del grupo. |
| ` *`userHandleArray`*` | `types:HandleArray` | Sí | Matriz de identificadores para los usuarios que desea agregar a un grupo. |

**Salida (addGroupMembersParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-8f168b528aef4c4fa8c3d41f7686842f}

En este ejemplo se utiliza ` *`addGroupMembersParam`*` para agregar un usuario a una sola compañía. La API de IPS no devuelve una respuesta para esta operación.

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
