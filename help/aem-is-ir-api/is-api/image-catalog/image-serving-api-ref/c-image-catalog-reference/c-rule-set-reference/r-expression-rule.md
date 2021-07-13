---
description: Elemento de patrón de expresión regular. Opcional en elementos <rule> .
solution: Experience Manager
title: expresión
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 4%

---

# expresión{#expression}

Elemento de patrón de expresión regular. Opcional en elementos `<rule>`.

## Atributos {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Ninguno.

## Datos {#section-e2601008d71243109af1a8c55b58416d}

Cadena de patrón de expresión regular.

## Descripción {#section-759bfb738ddb45dba1f0807aba8c1113}

El elemento `<expression>` puede estar vacío o contener una cadena de búsqueda simple o un patrón de expresión regular. El patrón se aplica a toda la cadena de solicitud.

Siempre se produce una coincidencia cuando `<expression>` está vacío o no se ha especificado; esto equivale a especificar `<expression>.*</expression>`.

La implementación se basa en el paquete Java [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), que proporciona una sintaxis de expresión regular similar a la de Perl.

## Notas {#section-10b472a902674893b49ca49a7052c366}

La cadena de expresión no debe contener caracteres literales &lt; y &amp;. Estos caracteres reservados se pueden codificar con `&` y `<` respectivamente, o toda la cadena se puede incluir en una sección XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Todos los caracteres entre las etiquetas `<expression>` y `</expression>` se pasan al analizador de expresiones regulares, incluidos los caracteres que están fuera de la sección opcional `CDATA`. Se debe tener cuidado para evitar espacios en blanco adicionales.

## Véase también {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
