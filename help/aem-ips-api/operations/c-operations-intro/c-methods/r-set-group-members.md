---
description: Establece la pertenencia a grupos de usuarios que pertenecen a una compañía específica.
seo-description: Establece la pertenencia a grupos de usuarios que pertenecen a una compañía específica.
seo-title: setGroupMembers
solution: Experience Manager
title: setGroupMembers
topic: Scene7 Image Production System API
uuid: fe6585ef-a4b3-4b3c-95d0-624017650497
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 8%

---


# setGroupMembers{#setgroupmembers}

Establece la pertenencia a grupos de usuarios que pertenecen a una compañía específica.

La operación genera un error de autenticación si no tiene privilegios para realizar esta operación. Esto también es cierto si alguno de los usuarios de la matriz de control de usuario no pertenece a la compañía especificada en el controlador de compañía.

## Tipos de usuarios autorizados {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-6a18562fc8e942af94be10bbb8c51151}

**Entrada (setGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de compañía. |
| ` *`groupHandle`*` | `xsd:string` | Sí | Identificador de grupo. |
| ` *`userHandleArray`*` | `types:HandleArray` | Sí | Matriz de identificadores para usuarios cuya pertenencia a grupos desea establecer. |

**Salida (setGroupMembesReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9c528c3f44a141ce9eaddf634f26c487}

Este ejemplo de código establece la pertenencia a grupos para un solo usuario.

**Solicitar**

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
