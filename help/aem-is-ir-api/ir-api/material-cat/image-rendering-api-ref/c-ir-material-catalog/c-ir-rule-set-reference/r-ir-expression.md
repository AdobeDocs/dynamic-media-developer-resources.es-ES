---
description: Elemento de patrón de expresión regular. Opcional en elementos <rule>.
seo-description: Elemento de patrón de expresión regular. Opcional en elementos <rule>.
seo-title: expresión
solution: Experience Manager
title: expresión
topic: Scene7 Image Serving - Image Rendering API
uuid: e7ef3769-0090-42d6-8021-1c213f1ee391
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 4%

---


# expresión{#expression}

Elemento de patrón de expresión regular. Opcional en elementos `<rule>`.

## Atributos {#section-fd0574eee1f9423cbb2ed709c0906800}

Ninguno.

## Datos {#section-4cd740c511a1432da0955e9acfbcf96f}

Cadena de patrón de expresión regular.

## Descripción {#section-3245c8a531bb455d8398449f6ea63b37}

El elemento `<expression>` puede estar vacío o contener una cadena de búsqueda simple o un patrón de expresión regular. El patrón se aplica a toda la cadena de solicitud.

Siempre se produce una coincidencia cuando `<expression>` está vacío o no se ha especificado; esto equivale a especificar `<expression>.*</expression>`.

La implementación se basa en el paquete Java [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), que proporciona una sintaxis de expresión regular similar a la de Perl.

## Nota {#section-6b41a900b0ce4a9590e5861e3c81599c}

La cadena de expresión no debe contener caracteres literales &lt; y &amp;. Estos caracteres reservados se pueden codificar con `&` y `<`, respectivamente, o toda la cadena se puede incluir en una sección XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Todos los caracteres entre las etiquetas `<expression>` y `</expression>` se pasan al analizador de expresiones normal, incluidos los caracteres fuera de la sección opcional `CDATA`. Se debe tener cuidado para evitar espacios en blanco adicionales.

## Véase también {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
