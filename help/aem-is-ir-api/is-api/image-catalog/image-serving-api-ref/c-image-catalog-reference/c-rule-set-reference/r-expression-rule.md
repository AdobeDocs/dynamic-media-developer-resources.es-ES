---
description: Elemento de patrón de expresión regular. Opcional en <rule> elementos.
solution: Experience Manager
title: expresión
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 4%

---

# expresión{#expression}

Elemento de patrón de expresión regular. Opcional en `<rule>` elementos.

## Atributos {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Ninguno.

## Datos {#section-e2601008d71243109af1a8c55b58416d}

Cadena de patrón de expresión regular.

## Descripción {#section-759bfb738ddb45dba1f0807aba8c1113}

El `<expression>` puede estar vacío o contener una cadena de búsqueda simple o un patrón de expresión regular. El patrón se aplica a toda la cadena de solicitud.

Las coincidencias siempre se producen cuando `<expression>` está vacío o no se ha especificado; equivale a especificar `<expression>.*</expression>`.

La implementación se basa en el paquete Java [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), que proporciona una sintaxis de expresión regular similar a la de Perl.

## Notas {#section-10b472a902674893b49ca49a7052c366}

La cadena de expresión no debe contener caracteres &lt; y &amp; literales. Estos caracteres reservados se pueden codificar con `&` y `<`, respectivamente, o toda la cadena se puede incluir en un XML `CDATA` sección:

`<expression><![CDATA[&fmt=custom]]></expression>`

Todos los caracteres entre `<expression>` y `</expression>` las etiquetas se pasan al analizador de expresiones regulares, incluidos los caracteres no incluidos en el `CDATA` sección. Se debe tener cuidado de evitar espacios en blanco adicionales.

## Véase también {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
