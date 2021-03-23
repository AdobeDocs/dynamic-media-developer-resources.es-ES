---
description: Elimina un proyecto de una empresa. Los vínculos entre los recursos y el proyecto se rompen, pero los recursos no se eliminan de IPS.
seo-description: Elimina un proyecto de una empresa. Los vínculos entre los recursos y el proyecto se rompen, pero los recursos no se eliminan de IPS.
seo-title: deleteProject
solution: Experience Manager
title: deleteProject
uuid: 0915066f-2106-4cbc-a68a-f149810c24f8
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 7%

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
