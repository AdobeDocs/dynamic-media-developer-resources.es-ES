---
description: Elimina un mapa de imagen.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 12%

---


# deleteImageMap{#deleteimagemap}

Elimina un mapa de imagen.

Sintaxis

## Tipos de usuarios autorizados {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura al recurso.

## Parámetros {#section-28de12bab79045a5977c68855e37ae3d}

**Entrada (deleteImageMapParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene el mapa de imagen que se va a eliminar. |
| `*`imageMapHandle`*` | `xsd:string` | Sí | El identificador del mapa de imagen que se va a eliminar. |

**Salida (deleteImageMapParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Este ejemplo de código elimina un mapa de imagen de una empresa. Debe obtener el identificador del mapa de imagen de otra operación.

**Solicitar**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Respuesta**

Ninguno
