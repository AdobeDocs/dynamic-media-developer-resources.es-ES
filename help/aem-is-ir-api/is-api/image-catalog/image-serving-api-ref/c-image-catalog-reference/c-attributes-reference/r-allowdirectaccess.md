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
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

Permitir el acceso directo a recursos basados en rutas.

Cuando se define este atributo, se permite o restringe el acceso basado en rutas para los tipos de objeto especificados, según se utilice la palabra clave `include` o `exclude`.

>[!NOTE]
>
>Si no se especifica el atributo `AllowDirectAccess`, el valor predeterminado es `exclude`.

* `include` permite el acceso a los tipos de objeto especificados y restringe el acceso a todos los demás.
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

* Permitir acceso directo sólo para tipos de objetos `IS` y `STATIC`

   `AllowDirectAccess=include:IS,STATIC`

* Permitir acceso directo para todos los tipos de objetos excepto `IS` y `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Permitir acceso directo para tipos de objetos *no* (es decir, no incluir ninguno)

   `AllowDirectAccess=include:`

* Permitir acceso directo para tipos de objetos *todos* (es decir, no excluir ninguno)

   `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (si `include`/ `exclude` no está presente, se asume `include`)

   `AllowDirectAccess=IS,STATIC`

   Tenga en cuenta que es el valor predeterminado que se utiliza si no se especifica el atributo `AllowDirectAccess` para esta compañía.

* Incluir ninguno, equivalente a `include:` (si `include`/ `exclude` no está presente, se asume `include`)

   `AllowDirectAccess=`

