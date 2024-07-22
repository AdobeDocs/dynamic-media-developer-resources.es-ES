---
description: Establece la pertenencia a grupos de usuarios que pertenecen a una compañía específica.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 7%

---

# setGroupMembers{#setgroupmembers}

Establece la pertenencia a grupos de usuarios que pertenecen a una compañía específica.

La operación genera un error de autenticación si no tiene privilegios para realizar esta operación. Esto también se aplica si alguno de los usuarios de la matriz de identificadores de usuario no pertenece a la compañía especificada en el identificador de la compañía,

## Tipos de usuarios autorizados {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-6a18562fc8e942af94be10bbb8c51151}

**Entrada (setGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Manejo de la compañía. |
| groupHandle | `xsd:string` | Sí | Identificador de grupo. |
| userHandleArray | `types:HandleArray` | Sí | Matriz de identificadores para los usuarios cuya pertenencia a grupo desea establecer. |

**Salida (setGroupMembesReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9c528c3f44a141ce9eaddf634f26c487}

Este ejemplo de código establece la pertenencia a grupos de un solo usuario.

**Solicitud**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**Respuesta**

Ninguno.
