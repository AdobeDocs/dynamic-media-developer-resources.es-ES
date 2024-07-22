---
title: sustitución
description: Elemento de cadena de sustitución. Opcional en elementos <rule>.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---

# sustitución{#substitution}

Elemento de cadena de sustitución. Opcional en `<rule>` elementos.

## Atributos {#section-d955eefc53eb4274861270669c01f9ca}

Ninguno.

## Datos {#section-a2688866ed6d41279a8478886e511ae3}

Cadena de sustitución.

## Descripción {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Define una cadena de reemplazo para la cadena o subcadena coincidente de la ruta de acceso o consulta.

Si la expresión de patrón incluye subexpresiones (delimitadas por paréntesis), la primera subcadena coincidente se reemplaza por la cadena de sustitución. Si la expresión de patrón no incluye subexpresiones, se sustituye toda la cadena coincidente.

Si `<expression>` está vacío o ausente, la cadena de sustitución se anexa a la ruta de acceso o consulta.

Si `<substitution>` está vacío, se quita la cadena o subcadena coincidente. Si no se especifica `<substitution>`, no se modifica la ruta de acceso o la cadena de consulta.

## Nota {#section-90fe89bb17a04804b7ff3c93df082892}

La cadena de sustitución no debe contener los caracteres literales &lt; y &amp;. Estos caracteres reservados se pueden codificar con `&` y `<`, respectivamente, o toda la cadena se puede incluir en una sección XML `CDATA`:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
