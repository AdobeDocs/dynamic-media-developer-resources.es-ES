---
description: Permita el acceso directo a los recursos basados en rutas.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

Permita el acceso directo a los recursos basados en rutas.

Cuando se define este atributo, el acceso basado en rutas está permitido o restringido para los tipos de objeto especificados, dependiendo de si se utilizan las palabras clave `include` o `exclude`.

>[!NOTE]
>
>Si no se especifica el atributo `AllowDirectAccess`, el valor predeterminado es `exclude`.

* `include` permite el acceso para los tipos de objeto especificados y restringe el acceso para todos los demás.
* `exclude` restringe el acceso para los tipos de objeto especificados y permite el acceso para todos los demás.

Si no se especifica `include` ni `exclude`, se asume `include`.

Se pueden controlar los siguientes tipos:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Ejemplos {#section-4c3765ebaa4245a799b454fc196f9237}

* Permitir acceso directo solo para tipos de objetos `IS` y `STATIC`

   `AllowDirectAccess=include:IS,STATIC`

* Permitir acceso directo para todos los tipos de objetos excepto `IS` y `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Permitir acceso directo para tipos de objetos *no* (es decir, no incluir ninguno)

   `AllowDirectAccess=include:`

* Permitir acceso directo para *todos los tipos de objetos* (es decir, excluir ninguno)

   `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (si `include`/ `exclude` no está presente, se asume `include`)

   `AllowDirectAccess=IS,STATIC`

   Tenga en cuenta que es el valor predeterminado que se usa si el atributo `AllowDirectAccess` no se especifica para esta empresa.

* Incluir ninguno, equivalente a `include:` (si `include`/ `exclude` no está presente, se asume `include`)

   `AllowDirectAccess=`

