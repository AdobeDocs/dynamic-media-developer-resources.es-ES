---
description: Elemento de cadena de sustitución. Opcional en <rule> elementos.
solution: Experience Manager
title: sustitución
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---

# sustitución{#substitution}

Elemento de cadena de sustitución. Opcional en `<rule>` elementos.

## Atributos {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Ninguno.

## Datos {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Cadena de sustitución.

## Descripción {#section-4a64a93f5e1a4d04a2db19166578bf76}

Define una cadena de reemplazo para la cadena o subcadena coincidente de la ruta de acceso o consulta.

Si la expresión de patrón incluye subexpresiones (delimitadas por paréntesis), la primera subcadena coincidente se reemplaza por la cadena de sustitución. Si la expresión de patrón no incluye subexpresiones, se sustituye toda la cadena coincidente.

If `<expression>` está vacía o ausente, la cadena de sustitución se anexa a la ruta o consulta.

If `<substitution>` está vacío, se elimina la cadena o subcadena coincidente. If `<substitution>` no se ha especificado, no se ha modificado la ruta de acceso o la cadena de consulta.

>[!NOTE]
>
>Todas las coincidencias de la cadena de entrada se sustituyen cuando `replace="all"` se especifica en la `<rule>`,elemento al que se aplica `<substitution>` el elemento pertenece. De forma predeterminada, solo la primera coincidencia se reemplaza con la cadena de sustitución.

## Nota {#section-cedf2adabaaf441c9f598fb0ea180246}

La cadena de sustitución no debe contener los caracteres literales &lt; y &amp;. Estos caracteres reservados se pueden codificar con `&` y `<`, respectivamente, o toda la cadena se puede incluir en una sección CDATA XML:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
