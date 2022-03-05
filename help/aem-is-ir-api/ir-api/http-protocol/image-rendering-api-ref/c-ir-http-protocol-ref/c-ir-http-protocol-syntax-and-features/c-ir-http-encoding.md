---
title: Codificación HTTP de renderización de imágenes
description: Los valores de comando deben tener codificación http utilizando secuencias de escape %xx, de modo que las cadenas de valor no incluyan los caracteres reservados '=', '&' y '%'.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# Codificación HTTP de renderización de imágenes{#image-rendering-http-encoding}

Los valores de comando deben tener codificación http utilizando secuencias de escape %xx, de modo que las cadenas de valor no incluyan los caracteres reservados &#39;=&#39;, &#39;&amp;&#39; y &#39;%&#39;.

De lo contrario, se aplican reglas de codificación HTTP estándar. La especificación HTTP requiere la codificación de caracteres no seguros como &#39; (espacio), &#39;&quot;(comillas dobles), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; y &#39;>&#39;, así como de cualquier carácter de control, como `<return>` y `<tab>`.

**Precaución:** Las llaves { } utilizadas como delimitadores de anidación de solicitudes no deben codificarse. Algunos clientes de correo electrónico codifican desafortunadamente las llaves en la solicitud HTTP incrustada. Si este problema es un problema, la renderización de imágenes permite el uso de paréntesis ( ) en lugar de llaves.

## Ejemplo {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

El fragmento de solicitud anterior debe codificarse de la siguiente manera:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Véase también {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Especificación HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
