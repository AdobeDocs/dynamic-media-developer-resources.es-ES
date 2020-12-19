---
description: Elemento de cadena de sustitución. Opcional en elementos <rule>.
seo-description: Elemento de cadena de sustitución. Opcional en elementos <rule>.
seo-title: sustitución
solution: Experience Manager
title: sustitución
topic: Scene7 Image Serving - Image Rendering API
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---


# sustitución{#substitution}

Elemento de cadena de sustitución. Opcional en elementos `<rule>`.

## Atributos {#section-d955eefc53eb4274861270669c01f9ca}

Ninguno.

## Datos {#section-a2688866ed6d41279a8478886e511ae3}

Cadena de sustitución.

## Descripción {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Define una cadena de reemplazo para la cadena o subcadena coincidente en la ruta o consulta.

Si la expresión de patrón incluye subexpresiones (delimitadas con paréntesis), la primera subcadena coincidente se sustituye por la cadena de sustitución. Si la expresión de patrón no incluye subexpresiones, se sustituye toda la cadena coincidente.

Si `<expression>` está vacío o ausente, la cadena de sustitución se anexa a la ruta o consulta.

Si `<substitution>` está vacío, se elimina la cadena o subcadena coincidente. Si no se especifica `<substitution>`, la ruta o la cadena de consulta no se modifica.

## Nota {#section-90fe89bb17a04804b7ff3c93df082892}

La cadena de sustitución no debe contener caracteres literales &lt; y &amp;. Estos caracteres reservados se pueden codificar con `&` y `<`, respectivamente, o toda la cadena se puede incluir en una sección XML `CDATA`:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
