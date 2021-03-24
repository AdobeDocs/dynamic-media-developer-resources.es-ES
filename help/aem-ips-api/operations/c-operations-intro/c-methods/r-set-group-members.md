---
description: Establece la pertenencia a un grupo de usuarios que pertenecen a una empresa específica.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---


# setGroupMembers{#setgroupmembers}

Establece la pertenencia a un grupo de usuarios que pertenecen a una empresa específica.

La operación genera un error de autenticación si no tiene privilegios para realizar esta operación. Esto también ocurre si alguno de los usuarios de la matriz de administración de usuarios no pertenece a la empresa especificada en el control de la empresa.

## Tipos de usuarios autorizados {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-6a18562fc8e942af94be10bbb8c51151}

**Entrada (setGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`groupHandle`*` | `xsd:string` | Sí | Identificador de grupo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sí | Matriz de controladores para usuarios cuya pertenencia a un grupo desee establecer. |

**Salida (setGroupMembesReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9c528c3f44a141ce9eaddf634f26c487}

Este ejemplo de código establece la pertenencia a un grupo para un único usuario.

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
