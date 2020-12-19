---
description: Elimina un destinatario de zoom.
seo-description: Elimina un destinatario de zoom.
seo-title: deleteZoomTarget
solution: Experience Manager
title: deleteZoomTarget
topic: Scene7 Image Production System API
uuid: 01a9321f-89a9-4263-937b-b0b49fe2fb81
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 12%

---


# deleteZoomTarget{#deletezoomtarget}

Elimina un destinatario de zoom.

## Tipos de usuarios autorizados {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura al recurso.

## Parámetros {#section-225330a45e7a408f8375e084677d9cb1}

**Entrada (deleteZoomTargetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía a la que pertenece el destinatario de zoom. |
| ` *`zoomTargetHandle`*` | `xsd:string` | Sí | Control del destinatario de zoom que se va a eliminar. |

**Salida (deleteZoomTargetParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplo {#section-a35857a5ca884357a879f7ba6cf985fe}

Este ejemplo de código elimina un destinatario de zoom de una compañía.

**Solicitar**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Respuesta**

Ninguno.
