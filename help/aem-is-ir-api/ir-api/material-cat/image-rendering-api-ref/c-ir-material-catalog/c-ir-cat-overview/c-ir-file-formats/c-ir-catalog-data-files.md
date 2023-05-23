---
title: Archivos de datos de catálogo
description: Los archivos de datos de catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Archivos de datos de catálogo{#catalog-data-files}

Los archivos de datos de catálogo pueden tener cualquier nombre y sufijo de archivo (excepto `.ini`).

Los archivos de datos de catálogo se pueden mantener fácilmente mediante aplicaciones que admiten archivos de datos de texto delimitados por tabuladores, como Microsoft® Excel y Access.

Básicamente una tabla bidimensional, un archivo de datos de catálogo consta de un registro de encabezado que identifica las columnas de datos y cualquier número de registros de datos (filas). Los campos del encabezado y los registros de datos están separados por una sola etiqueta `<TAB>` caracteres. Los registros están separados por un único `<CR>` (código ASCII `0xD`), un solo `<LF>` (código ASCII `0xA`), o un `<CR><LF>` par.

El registro de encabezado debe contener los nombres exactos para cada campo de datos. No se permiten campos vacíos en la fila del encabezado. Los nombres de los campos de datos no distinguen entre mayúsculas y minúsculas. Todos los nombres de campo deben ser únicos.

No hay más espacios en blanco que el `<TAB>` se permiten separadores de campos en los registros de datos y encabezados.

En los registros de datos, dos adyacentes `<TAB>` Los caracteres indican un campo vacío. Los campos vacíos heredan los valores predeterminados de los atributos de catálogo o de los valores predeterminados del servidor.

Los campos de datos no deben contener `<CR>`, `<LF>`, o `<TAB>` caracteres, a menos que el valor de los datos sea de tipo texto y esté entre comillas simples o dobles. No codifique los campos de datos mediante HTTP.

Si hay varios valores de datos en el mismo campo, se separan con comas (&quot;,&quot;), a menos que se indique lo contrario.

Columnas cuyos nombres empiezan por &#39;.&#39; no se tienen en cuenta, lo que permite almacenar datos en catálogos de materiales que no interesan a Image Rendering. Las columnas con nombres de encabezado desconocidos se omiten y se escribe una advertencia en el archivo de registro.

Los nombres de campo pueden constar de cualquier combinación de letras ASCII, números y &quot;-&quot; y &quot;_&quot;.

Se pueden utilizar una o más columnas como claves de índice. Si la misma clave se produce más de una vez en el mismo archivo de datos, prevalecerá la instancia posterior.
