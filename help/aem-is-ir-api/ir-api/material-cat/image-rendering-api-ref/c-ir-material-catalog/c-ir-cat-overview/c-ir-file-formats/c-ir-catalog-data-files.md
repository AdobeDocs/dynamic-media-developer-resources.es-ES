---
description: Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini).
solution: Experience Manager
title: Archivos de datos del catálogo
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# Archivos de datos del catálogo{#catalog-data-files}

Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini).

Los archivos de datos del catálogo se pueden mantener fácilmente mediante aplicaciones que admitan archivos de datos de texto delimitados por tabuladores, como Microsoft Excel y Access.

Básicamente una tabla bidimensional, un archivo de datos de catálogo consta de un registro de encabezado que identifica las columnas de datos y cualquier número de registros de datos (filas). Los campos del encabezado y los registros de datos se separan con caracteres `<TAB>` únicos. Los registros están separados por un único `<CR>` (código ASCII 0xD), un único `<LF>` (código ASCII 0xA) o un par `<CR><LF>`.

El registro de encabezado debe contener los nombres exactos de cada campo de datos. Los campos vacíos no están permitidos en la fila de encabezado. Los nombres de los campos de datos no distinguen entre mayúsculas y minúsculas. Todos los nombres de campo deben ser únicos.

En el encabezado y los registros de datos no se permiten espacios en blanco que no sean los separadores de campo `<TAB>`.

En los registros de datos, dos caracteres `<TAB>` adyacentes indican un campo vacío. Los campos vacíos heredarán los valores predeterminados de los atributos de catálogo o de los valores predeterminados del servidor.

Los campos de datos no deben contener caracteres `<CR>`, `<LF>` ni `<TAB>`, a menos que el valor de datos sea de tipo texto y esté entre comillas simples o dobles. Los campos de datos no deben tener codificación HTTP.

Si no se indica lo contrario, los valores de varios datos del mismo campo se separan con comas (&#39;,&#39;).

Columnas cuyos nombres empiezan por &#39;.&#39; se ignoran; esto permite almacenar datos en catálogos de materiales que no son de interés para el procesamiento de imágenes. Las columnas con nombres de encabezado desconocidos se ignoran y se escribe una advertencia en el archivo de registro.

Los nombres de campo pueden consistir en cualquier combinación de letras ASCII, números, así como &quot;-&quot; y &quot;_&quot;.

Se pueden utilizar una o más columnas como claves de índice. Si la misma clave se produce más de una vez en el mismo archivo de datos, prevalecerá la instancia posterior.
