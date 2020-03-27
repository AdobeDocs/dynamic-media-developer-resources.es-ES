---
description: Permitir el acceso directo a recursos basados en rutas.
seo-description: Permitir el acceso directo a recursos basados en rutas.
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AllowDirectAccess{#allowdirectaccess}

Permitir el acceso directo a recursos basados en rutas.

Cuando se define este atributo, se permite o restringe el acceso basado en rutas para los tipos de objeto especificados, en función de si se utiliza la palabra clave `include` o `exclude` .

>[!NOTE]
>
>Si no se especifica el `AllowDirectAccess` atributo, el valor predeterminado es `exclude`.

* `include` permite el acceso a los tipos de objeto especificados y restringe el acceso a todos los demás.
* `exclude` restringe el acceso para los tipos de objeto especificados y permite el acceso para todos los demás.

Si no `include` se especifica ni `exclude` , `include` se asume.

Se pueden controlar los siguientes tipos:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Ejemplos {#section-4c3765ebaa4245a799b454fc196f9237}

* Permitir el acceso directo solo para tipos `IS` de objetos y `STATIC` objetos

   `AllowDirectAccess=include:IS,STATIC`

* Permitir el acceso directo a todos los tipos de objetos excepto `IS` y `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Permitir acceso directo para *ningún* tipo de objeto (es decir, incluir ninguno)

   `AllowDirectAccess=include:`

* Permitir acceso directo para *todos los* tipos de objetos (es decir, excluir ninguno)

   `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (si `include`/ `exclude` no está presente, `include` se asume)

   `AllowDirectAccess=IS,STATIC`

   Tenga en cuenta que es el valor predeterminado que se utiliza si no se especifica el `AllowDirectAccess` atributo para esta compañía.

* Incluir ninguno, equivalente a `include:` (si `include`/ `exclude` no está presente, `include` se supone)

   `AllowDirectAccess=`

