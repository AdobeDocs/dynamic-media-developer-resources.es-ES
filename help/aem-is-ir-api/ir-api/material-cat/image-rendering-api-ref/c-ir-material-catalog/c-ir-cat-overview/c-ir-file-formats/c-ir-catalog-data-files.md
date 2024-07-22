---
title: Archivos de datos de catálogo
description: Los archivos de datos de catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Archivos de datos de catálogo{#catalog-data-files}

Los archivos de datos de catálogo pueden tener cualquier nombre y sufijo de archivo (excepto `.ini`).

Los archivos de datos de catálogo se pueden mantener fácilmente mediante aplicaciones que admiten archivos de datos de texto delimitados por tabuladores, como Microsoft® Excel y Access.

Básicamente una tabla bidimensional, un archivo de datos de catálogo consta de un registro de encabezado que identifica las columnas de datos y cualquier número de registros de datos (filas). Los campos del encabezado y de los registros de datos están separados por `<TAB>` caracteres. Los registros están separados por un único `<CR>` (código ASCII `0xD`), un único `<LF>` (código ASCII `0xA`) o un par `<CR><LF>`.

El registro de encabezado debe contener los nombres exactos para cada campo de datos. No se permiten campos vacíos en la fila del encabezado. Los nombres de los campos de datos no distinguen entre mayúsculas y minúsculas. Todos los nombres de campo deben ser únicos.

No se permite ningún espacio en blanco que no sean los separadores de campo `<TAB>` en el encabezado y en los registros de datos.

En los registros de datos, dos caracteres `<TAB>` adyacentes indican un campo vacío. Los campos vacíos heredan los valores predeterminados de los atributos de catálogo o de los valores predeterminados del servidor.

Los campos de datos no deben contener los caracteres `<CR>`, `<LF>` o `<TAB>`, a menos que el valor de datos sea de tipo texto y esté entre comillas simples o dobles. No codifique los campos de datos mediante HTTP.

Si hay varios valores de datos en el mismo campo, se separan con comas (&quot;,&quot;), a menos que se indique lo contrario.

Columnas cuyos nombres empiezan por &#39;.&#39; no se tienen en cuenta, lo que permite almacenar datos en catálogos de materiales que no interesan a Image Rendering. Las columnas con nombres de encabezado desconocidos se omiten y se escribe una advertencia en el archivo de registro.

Los nombres de campo pueden constar de cualquier combinación de letras ASCII, números y &quot;-&quot; y &quot;_&quot;.

Se pueden utilizar una o más columnas como claves de índice. Si la misma clave se produce más de una vez en el mismo archivo de datos, prevalecerá la instancia posterior.
