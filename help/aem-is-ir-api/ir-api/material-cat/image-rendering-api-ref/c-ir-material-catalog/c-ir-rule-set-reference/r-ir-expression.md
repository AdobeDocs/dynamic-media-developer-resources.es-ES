---
description: Elemento de patrón de expresión regular. Opcional en elementos <rule>.
solution: Experience Manager
title: expresión
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
TQID: 'https://experienceleague.adobe.com/zMAFfzeypXmMIx1aO1xmHdF-UkHJPHKp7KUgi05F94w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 4%

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
