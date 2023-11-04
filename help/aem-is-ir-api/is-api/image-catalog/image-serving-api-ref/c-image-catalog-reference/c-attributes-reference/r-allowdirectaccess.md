---
description: Permitir el acceso directo a los recursos basados en rutas.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Permitir el acceso directo a los recursos basados en rutas.

Cuando se define este atributo, se permite o restringe el acceso basado en rutas para los tipos de objeto especificados, dependiendo de si la variable `include` o `exclude` se utiliza la palabra clave.

>[!NOTE]
>
>Si la variable `AllowDirectAccess` no se ha especificado el atributo, el valor predeterminado es `exclude`.

* `include` permite el acceso para los tipos de objeto especificados y restringe el acceso para todos los demás.
* `exclude` restringe el acceso para los tipos de objeto especificados y permite el acceso para todos los demás.

Si ninguno `include` ni `exclude` se ha especificado, `include` se asume.

Se pueden controlar los siguientes tipos:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Ejemplos {#section-4c3765ebaa4245a799b454fc196f9237}

* Permitir acceso directo solo para `IS` y `STATIC` tipos de objeto

  `AllowDirectAccess=include:IS,STATIC`

* Permitir acceso directo a todos los tipos de objetos excepto `IS` y `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Permitir acceso directo para *no* tipos de objeto (es decir, no incluir ninguno)

  `AllowDirectAccess=include:`

* Permitir acceso directo para *todo* tipos de objeto (es decir, no excluir ninguno)

  `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (if `include`/ `exclude` no está presente, `include` se supone)

  `AllowDirectAccess=IS,STATIC`

  Tenga en cuenta que es el valor predeterminado que se utiliza si `AllowDirectAccess` no se ha especificado el atributo para esta empresa.

* Incluir ninguno, equivalente a `include:` (if `include`/ `exclude` no está presente, `include` se supone)

  `AllowDirectAccess=`
