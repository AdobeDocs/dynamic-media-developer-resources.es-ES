---
description: Elimina un proyecto de una compañía. Los vínculos entre los recursos y el proyecto están dañados, pero los recursos no se eliminan de IPS.
seo-description: Elimina un proyecto de una compañía. Los vínculos entre los recursos y el proyecto están dañados, pero los recursos no se eliminan de IPS.
seo-title: deleteProject
solution: Experience Manager
title: deleteProject
topic: Scene7 Image Production System API
uuid: 0915066f-2106-4cbc-a68a-f149810c24f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# deleteProject{#deleteproject}

Elimina un proyecto de una compañía. Los vínculos entre los recursos y el proyecto están dañados, pero los recursos no se eliminan de IPS.

Sintaxis

## Tipos de usuarios autorizados {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-00d1e00dd5014513a52b4e6b4f61de62}

**Entrada (deleteProjectParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Sí | Nombre de la compañía asociada al proyecto. |
| ` *`projectHandle`*` | `xsd:string` | Sí | Identificador del proyecto que se va a eliminar. |

**Salida (deleteProjectReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-e38507f1f7ec41b9a625f47390490254}

Este ejemplo de código utiliza el identificador de compañía y el identificador de proyecto como campos en deleteProjectParam enviados al servidor de servicios Web IPS para eliminar el proyecto.

**Solicitar**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Respuesta**

Ninguno.
