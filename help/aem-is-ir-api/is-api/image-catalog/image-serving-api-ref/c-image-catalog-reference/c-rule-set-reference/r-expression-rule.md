---
description: Elemento de patrón de expresión normal. Opcional en elementos <rule>.
seo-description: Elemento de patrón de expresión normal. Opcional en elementos <rule>.
seo-title: expresión
solution: Experience Manager
title: expresión
topic: Scene7 Image Serving - Image Rendering API
uuid: f2036015-a2c7-4392-86f6-4cdf3152839a
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# expresión{#expression}

Elemento de patrón de expresión normal. Opcional en elementos `<rule>`.

## Atributos {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Ninguno.

## Datos {#section-e2601008d71243109af1a8c55b58416d}

Cadena de patrón de expresión regular.

## Descripción {#section-759bfb738ddb45dba1f0807aba8c1113}

El elemento `<expression>` puede estar vacío o contener una cadena de búsqueda simple o un patrón de expresión regular. El patrón se aplica a toda la cadena de solicitud.

Siempre se produce una coincidencia cuando `<expression>` está vacío o no se ha especificado; esto equivale a especificar `<expression>.*</expression>`.

La implementación se basa en el paquete Java [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), que proporciona una sintaxis de expresión regular similar a la de Perl.

## Notas {#section-10b472a902674893b49ca49a7052c366}

La cadena de expresión no debe contener caracteres literales &lt; y &amp;. Estos caracteres reservados se pueden codificar con `&` y `<`, respectivamente, o toda la cadena se puede incluir en una sección XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Todos los caracteres entre las etiquetas `<expression>` y `</expression>` se pasan al analizador de expresiones normal, incluidos los caracteres fuera de la sección opcional `CDATA`. Se debe tener cuidado para evitar espacios en blanco adicionales.

## Véase también {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
