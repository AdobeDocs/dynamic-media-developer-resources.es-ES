---
description: Establece la pertenencia a grupos de un usuario.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 13%

---

# setGroupMembership{#setgroupmembership}

Establece la pertenencia a grupos de un usuario.

Sintaxis

## Tipos de usuarios autorizados {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Entrada (setGroupMembershipParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userHandle | `xsd:string` | No | El identificador del usuario cuya pertenencia al grupo desea establecer. |
| companyHandle | `xsd:string` | No | Manejo de la compañía. |
| groupHandleArray | `types:HandleArray` | Sí | Matriz de identificadores de grupos a los que pertenece el usuario. |

**Salida (setGroupMembershipReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-67b86d259df24938896fe19061845811}

Este ejemplo de código convierte al usuario en miembro de un grupo. Agregue un usuario a varios grupos con la matriz de identificadores de grupo.

**Solicitar**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Respuesta**

Ninguno.
