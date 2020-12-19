---
description: Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini). Pueden mantenerse fácilmente mediante aplicaciones que admiten archivos de datos de texto delimitados por tabuladores, como Microsoft Excel y Access.
seo-description: Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini). Pueden mantenerse fácilmente mediante aplicaciones que admiten archivos de datos de texto delimitados por tabuladores, como Microsoft Excel y Access.
seo-title: Archivos de datos del catálogo
solution: Experience Manager
title: Archivos de datos del catálogo
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f66e2fe-5b8a-43d3-bf2e-8dd79da6a581
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Archivos de datos del catálogo{#catalog-data-files}

Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini). Pueden mantenerse fácilmente mediante aplicaciones que admiten archivos de datos de texto delimitados por tabuladores, como Microsoft Excel y Access.

Básicamente, una tabla bidimensional, un archivo de datos de catálogo consiste en un registro de encabezado que identifica las columnas de datos y cualquier número de registros de datos (filas). Los campos tanto en el encabezado como en los registros de datos están separados por `<TAB>` caracteres únicos. Los registros están separados por un único `<CR>` (código ASCII `0xD`), un único `<LF>` (código ASCII `0xA`) o un par `<CR><LF>`.

El registro de encabezado debe contener los nombres exactos de cada campo de datos. Los campos vacíos no están permitidos en la fila de encabezado. Los nombres de los campos de datos no distinguen entre mayúsculas y minúsculas. Todos los nombres de campo deben ser únicos.

Los caracteres de espacio no se pueden usar como separadores de campo. No se permiten espacios en el registro de encabezado. En los registros de datos, cualquier espacio al principio o al final de un campo de datos se considera parte de ese campo de datos.

En los registros de datos, dos caracteres `<TAB>` adyacentes indican un campo vacío. Los campos vacíos pueden heredar valores predeterminados de los atributos del catálogo o de los valores predeterminados del servidor.

Los campos de datos se pueden incluir opcionalmente entre comillas de doble. No deben contener `<CR>`, `<LF>` ni `<TAB>` caracteres, a menos que el valor de datos sea de tipo texto y esté entre comillas de doble. Los campos de datos no deben tener codificación HTTP.

Varios valores de datos en el mismo campo se separan con comas, a menos que se indique lo contrario.

Columnas cuyos nombres inicio con &quot;.&quot; se ignoran. Esto permite almacenar datos en catálogos de imágenes, lo que no interesa al servicio de imágenes. Las columnas con nombres de encabezado desconocidos se omiten y se escribe una advertencia en el archivo de registro.

Los nombres de campo pueden constar de cualquier combinación de letras ASCII, números, así como &quot;-&quot; y &quot;_&quot;.

Se pueden utilizar una o más columnas como claves de índice. Si la misma clave se produce más de una vez en el mismo archivo de datos, prevalecerá la instancia posterior.
