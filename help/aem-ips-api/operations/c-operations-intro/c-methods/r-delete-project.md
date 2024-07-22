---
description: Elimina un proyecto de una compañía. Los vínculos entre los recursos y el proyecto están rotos, pero los recursos no se eliminan de IPS.
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---

# deleteProject{#deleteproject}

Elimina un proyecto de una compañía. Los vínculos entre los recursos y el proyecto están rotos, pero los recursos no se eliminan de IPS.

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
| companyName | `xsd:string` | Sí | El nombre de la empresa asociada con el proyecto. |
| projectHandle | `xsd:string` | Sí | El identificador del proyecto que se va a eliminar. |

**Salida (deleteProjectReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-e38507f1f7ec41b9a625f47390490254}

En este ejemplo de código se utiliza el identificador de la compañía y el identificador del proyecto como campos del parámetro deleteProjectParam enviado al servidor de servicios Web IPS para eliminar el proyecto.

**Solicitud**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Respuesta**

Ninguno.
