---
description: Elemento de cadena de sustitución. Opcional en elementos <rule>.
seo-description: Elemento de cadena de sustitución. Opcional en elementos <rule>.
seo-title: sustitución
solution: Experience Manager
title: sustitución
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e5730559-0512-4416-927d-a7faf9180741
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# sustitución{#substitution}

Elemento de cadena de sustitución. Opcional en elementos `<rule>`.

## Atributos {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Ninguno.

## Datos {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Cadena de sustitución.

## Descripción {#section-4a64a93f5e1a4d04a2db19166578bf76}

Define una cadena de reemplazo para la cadena o subcadena coincidente en la ruta o consulta.

Si la expresión de patrón incluye subexpresiones (delimitadas con paréntesis), la primera subcadena coincidente se sustituye por la cadena de sustitución. Si la expresión de patrón no incluye subexpresiones, se sustituye toda la cadena coincidente.

Si `<expression>` está vacío o ausente, la cadena de sustitución se anexa a la ruta o consulta.

Si `<substitution>` está vacío, se elimina la cadena o subcadena coincidente. Si no se especifica `<substitution>`, la ruta o la cadena de consulta no se modifica.

>[!NOTE]
>
>Todas las coincidencias de la cadena de entrada se sustituyen cuando `replace="all"` se especifica en el elemento `<rule>` al que pertenece este elemento `<substitution>`. De forma predeterminada, solo la primera coincidencia se sustituye por la cadena de sustitución.

## Nota {#section-cedf2adabaaf441c9f598fb0ea180246}

La cadena de sustitución no debe contener caracteres literales &lt; y &amp;. Estos caracteres reservados se pueden codificar con `&` y `<`, respectivamente, o toda la cadena se puede incluir en una sección CDATA XML:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
