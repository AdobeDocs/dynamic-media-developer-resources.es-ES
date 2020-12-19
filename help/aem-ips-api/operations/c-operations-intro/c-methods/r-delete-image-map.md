---
description: Elimina un mapa de imagen.
seo-description: Elimina un mapa de imagen.
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
topic: Scene7 Image Production System API
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que contiene el mapa de imagen que se va a eliminar. |
| ` *`imageMapHandle`*` | `xsd:string` | Sí | Identificador del mapa de imagen que se va a eliminar. |

**Salida (deleteImageMapParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Este ejemplo de código elimina un mapa de imagen de una compañía. Debe obtener el controlador de mapa de imagen de otra operación.

**Solicitar**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Respuesta**

Ninguno
