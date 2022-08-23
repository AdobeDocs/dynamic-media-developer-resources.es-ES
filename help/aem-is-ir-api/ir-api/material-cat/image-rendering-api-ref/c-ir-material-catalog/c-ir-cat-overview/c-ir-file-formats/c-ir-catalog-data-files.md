---
title: Archivos de datos del catálogo
description: Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Archivos de datos del catálogo{#catalog-data-files}

Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto `.ini`).

Los archivos de datos del catálogo se pueden mantener fácilmente utilizando aplicaciones que admitan archivos de datos de texto delimitados por tabuladores, como Microsoft® Excel y Access.

Básicamente una tabla bidimensional, un archivo de datos de catálogo consta de un registro de encabezado que identifica las columnas de datos y cualquier número de registros de datos (filas). Los campos de los registros de datos y encabezados se separan con una sola `<TAB>` caracteres. Los registros están separados por una sola `<CR>` (Código ASCII `0xD`), un solo `<LF>` (Código ASCII `0xA`) o a `<CR><LF>` par.

El registro de encabezado debe contener los nombres exactos de cada campo de datos. Los campos vacíos no están permitidos en la fila de encabezado. Los nombres de los campos de datos no distinguen entre mayúsculas y minúsculas. Todos los nombres de campo deben ser únicos.

No hay espacios en blanco que no sean `<TAB>` los separadores de campo están permitidos en el encabezado y en los registros de datos.

En los registros de datos, dos adyacentes `<TAB>` los caracteres indican un campo vacío. Los campos vacíos heredan los valores predeterminados de los atributos de catálogo o de los valores predeterminados del servidor.

Los campos de datos no deben contener `<CR>`, `<LF>`o `<TAB>` , a menos que el valor de los datos sea de tipo texto y esté entre comillas simples o dobles. No codifique HTTP los campos de datos.

Si no se indica lo contrario, los valores de varios datos del mismo campo se separan con comas (&#39;,&#39;).

Columnas cuyos nombres empiezan por &#39;.&#39; se ignoran; esto permite almacenar datos en catálogos de materiales que no son de interés para el procesamiento de imágenes. Las columnas con nombres de encabezado desconocidos se ignoran y se escribe una advertencia en el archivo de registro.

Los nombres de campo pueden constar de cualquier combinación de letras ASCII, números y &quot;-&quot; y &quot;_&quot;.

Se pueden utilizar una o más columnas como claves de índice. Si la misma clave se produce más de una vez en el mismo archivo de datos, prevalecerá la instancia posterior.
