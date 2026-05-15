---
description: Permitir el acceso directo a los recursos basados en rutas.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
TQID: 'https://experienceleague.adobe.com/h2bcjdutPEZID471oI-MWfxG4trg87bIeyAxvoMyKEA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Permitir el acceso directo a los recursos basados en rutas.

Cuando se define este atributo, se permite o restringe el acceso basado en rutas para los tipos de objeto especificados, dependiendo de si se utiliza la palabra clave `include` o `exclude`.

>[!NOTE]
>
>Si no se especifica el atributo `AllowDirectAccess`, el valor predeterminado es `exclude`.

* `include` permite el acceso para los tipos de objeto especificados y restringe el acceso para todos los demás.
* `exclude` restringe el acceso para los tipos de objeto especificados y permite el acceso para todos los demás.

Si no se especifica ni `include` ni `exclude`, se asume `include`.

Se pueden controlar los siguientes tipos:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Ejemplos {#section-4c3765ebaa4245a799b454fc196f9237}

* Permitir acceso directo solo para los tipos de objeto `IS` y `STATIC`

  `AllowDirectAccess=include:IS,STATIC`

* Permitir acceso directo a todos los tipos de objetos excepto `IS` y `STATIC` `AllowDirectAccess=exclude:IS,STATIC`

* Permitir acceso directo a *no* tipos de objetos (es decir, no incluir ninguno)

  `AllowDirectAccess=include:`

* Permitir acceso directo a *todos* los tipos de objetos (es decir, no excluir ninguno)

  `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (si `include`/ `exclude` no está presente, se supone que `include`)

  `AllowDirectAccess=IS,STATIC`

  Tenga en cuenta que es el valor predeterminado que se utiliza si el atributo `AllowDirectAccess` no se especifica para esta compañía.

* Incluir ninguno, equivalente a `include:` (si `include`/ `exclude` no está presente, se supone que `include`)

  `AllowDirectAccess=`
