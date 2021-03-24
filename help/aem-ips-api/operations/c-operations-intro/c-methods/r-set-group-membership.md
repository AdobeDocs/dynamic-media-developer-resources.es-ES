---
description: Establece la pertenencia a un grupo para un usuario.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 12%

---


# setGroupMembership{#setgroupmembership}

Establece la pertenencia a un grupo para un usuario.

Sintaxis

## Tipos de usuarios autorizados {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Entrada (setGroupMembershipParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | No | El identificador del usuario cuya pertenencia a grupo desea establecer. |
| `*`companyHandle`*` | `xsd:string` | No | Identificador de la empresa. |
| `*`groupHandleArray`*` | `types:HandleArray` | Sí | Matriz de controles a grupos a los que pertenece el usuario. |

**Salida (setGroupMembershipReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-67b86d259df24938896fe19061845811}

Este ejemplo de código convierte al usuario en miembro de un grupo. Agregue un usuario a varios grupos con la matriz de gestión de grupo.

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
