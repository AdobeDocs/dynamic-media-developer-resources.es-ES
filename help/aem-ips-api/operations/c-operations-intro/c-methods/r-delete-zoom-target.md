---
description: Elimina un destino de zoom.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 13%

---

# deleteZoomTarget{#deletezoomtarget}

Elimina un destino de zoom.

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
| companyHandle | `xsd:string` | Sí | El identificador de la empresa a la que pertenece el destino de zoom. |
| zoomTargetHandle | `xsd:string` | Sí | El controlador para el destino de zoom que se va a eliminar. |

**Salida (deleteZoomTargetParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplo {#section-a35857a5ca884357a879f7ba6cf985fe}

Este ejemplo de código elimina un objetivo de zoom de una empresa.

**Solicitar**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Respuesta**

Ninguno.
