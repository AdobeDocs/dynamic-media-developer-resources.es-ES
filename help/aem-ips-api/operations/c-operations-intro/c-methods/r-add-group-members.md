---
description: Agrega usuarios de una compañía específica a un grupo específico.
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 10%

---

# addGroupMembers{#addgroupmembers}

Agrega usuarios de una compañía específica a un grupo específico.

Sintaxis

## Tipos de usuarios autorizados {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-b28434dcf2ca4b4ea431136aac33913e}

**Entrada (addGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía. |
| groupHandle | `xsd:string` | Sí | El identificador del grupo. |
| userHandleArray | `types:HandleArray` | Sí | Matriz de identificadores para los usuarios que desea agregar a un grupo. |

**Salida (addGroupMembersParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-8f168b528aef4c4fa8c3d41f7686842f}

En este ejemplo se utiliza addGroupMembersParam para agregar un usuario a una sola compañía. La API de IPS no devuelve una respuesta para esta operación.

**Solicitud**

```java {.line-numbers}
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Respuesta**

Ninguno.
