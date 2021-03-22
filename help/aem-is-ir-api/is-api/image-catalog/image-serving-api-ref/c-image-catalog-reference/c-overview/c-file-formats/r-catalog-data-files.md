---
description: Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini). Se pueden mantener fácilmente mediante aplicaciones que admitan archivos de datos de texto delimitados por tabuladores, como Microsoft Excel y Access.
seo-description: Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini). Se pueden mantener fácilmente mediante aplicaciones que admitan archivos de datos de texto delimitados por tabuladores, como Microsoft Excel y Access.
seo-title: Archivos de datos del catálogo
solution: Experience Manager
title: Archivos de datos del catálogo
uuid: 0f66e2fe-5b8a-43d3-bf2e-8dd79da6a581
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---


# Archivos de datos del catálogo{#catalog-data-files}

Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini). Se pueden mantener fácilmente mediante aplicaciones que admitan archivos de datos de texto delimitados por tabuladores, como Microsoft Excel y Access.

Básicamente una tabla bidimensional, un archivo de datos de catálogo consta de un registro de encabezado que identifica las columnas de datos y cualquier cantidad de registros de datos (filas). Los campos del encabezado y los registros de datos se separan con caracteres `<TAB>` únicos. Los registros están separados por un único `<CR>` (código ASCII `0xD`), un único `<LF>` (código ASCII `0xA`) o un par `<CR><LF>`.

El registro de encabezado debe contener los nombres exactos de cada campo de datos. Los campos vacíos no están permitidos en la fila de encabezado. Los nombres de los campos de datos no distinguen entre mayúsculas y minúsculas. Todos los nombres de campo deben ser únicos.

Los caracteres de espacio no se pueden usar como separadores de campo. No se permiten espacios en el registro de encabezado. En los registros de datos, cualquier espacio al principio o al final de un campo de datos se considera parte de ese campo de datos.

En los registros de datos, dos caracteres `<TAB>` adyacentes indican un campo vacío. Los campos vacíos pueden heredar valores predeterminados de los atributos de catálogo o de los valores predeterminados del servidor.

Los campos de datos se pueden incluir de forma opcional entre comillas dobles. No deben contener caracteres `<CR>`, `<LF>` ni `<TAB>`, a menos que el valor de los datos sea de tipo texto y esté entre comillas dobles. Los campos de datos no deben tener codificación HTTP.

Los valores de datos múltiples del mismo campo se separan con comas, a menos que se indique lo contrario.

Columnas cuyos nombres empiezan por &quot;.&quot; se ignoran. Esto permite almacenar datos en catálogos de imágenes, lo que no interesa al servicio de imágenes. Las columnas con nombres de encabezado desconocidos se ignoran y se escribe una advertencia en el archivo de registro.

Los nombres de campo pueden consistir en cualquier combinación de letras ASCII, números, así como &quot;-&quot; y &quot;_&quot;.

Se pueden utilizar una o más columnas como claves de índice. Si la misma clave se produce más de una vez en el mismo archivo de datos, prevalecerá la instancia posterior.
