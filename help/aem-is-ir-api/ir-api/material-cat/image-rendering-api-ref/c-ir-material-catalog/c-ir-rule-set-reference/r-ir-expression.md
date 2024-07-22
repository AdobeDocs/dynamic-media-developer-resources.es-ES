---
description: Elemento de patrón de expresión regular. Opcional en elementos <rule>.
solution: Experience Manager
title: expresión
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 5%

---

# expresión{#expression}

Elemento de patrón de expresión regular. Opcional en `<rule>` elementos.

## Atributos {#section-fd0574eee1f9423cbb2ed709c0906800}

Ninguno.

## Datos {#section-4cd740c511a1432da0955e9acfbcf96f}

Cadena de patrón de expresión regular.

## Descripción {#section-3245c8a531bb455d8398449f6ea63b37}

El elemento `<expression>` puede estar vacío o contener una cadena de búsqueda simple o un patrón de expresión regular. El patrón se aplica a toda la cadena de solicitud.

Siempre hay una coincidencia cuando `<expression>` está vacío o no se ha especificado; esto equivale a especificar `<expression>.*</expression>`.

La implementación se basa en el paquete Java [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), que proporciona una sintaxis de expresión regular similar a la de Perl.

## Nota {#section-6b41a900b0ce4a9590e5861e3c81599c}

La cadena de expresión no debe contener caracteres &lt; y &amp; literales. Estos caracteres reservados se pueden codificar con `&` y `<`, respectivamente, o toda la cadena se puede incluir en una sección XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Todos los caracteres entre las etiquetas `<expression>` y `</expression>` se pasan al analizador de expresiones regulares, incluidos los caracteres que no están en la sección `CDATA` opcional. Se debe tener cuidado de evitar espacios en blanco adicionales.

## Véase también {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
