---
description: Elimina un proyecto de una empresa. Los vínculos entre los recursos y el proyecto se rompen, pero los recursos no se eliminan de IPS.
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 8%

---


# deleteProject{#deleteproject}

Elimina un proyecto de una empresa. Los vínculos entre los recursos y el proyecto se rompen, pero los recursos no se eliminan de IPS.

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
| `*`companyName`*` | `xsd:string` | Sí | Nombre de la empresa asociada al proyecto. |
| `*`projectHandle`*` | `xsd:string` | Sí | El identificador del proyecto que se va a eliminar. |

**Salida (deleteProjectReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-e38507f1f7ec41b9a625f47390490254}

Este ejemplo de código utiliza el identificador de la empresa y el identificador del proyecto como campos en deleteProjectParam enviados al servidor de servicios web IPS para eliminar el proyecto.

**Solicitar**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Respuesta**

Ninguno.
