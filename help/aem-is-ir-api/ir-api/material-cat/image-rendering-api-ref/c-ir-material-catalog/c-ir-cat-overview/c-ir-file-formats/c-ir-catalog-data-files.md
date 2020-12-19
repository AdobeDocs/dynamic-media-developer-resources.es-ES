---
description: Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini).
seo-description: Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini).
seo-title: Archivos de datos del catálogo
solution: Experience Manager
title: Archivos de datos del catálogo
topic: Scene7 Image Serving - Image Rendering API
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Archivos de datos del catálogo{#catalog-data-files}

Los archivos de datos del catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini).

Los archivos de datos del catálogo se pueden mantener fácilmente mediante aplicaciones que admiten archivos de datos de texto delimitados por tabuladores, como Microsoft Excel y Access.

Básicamente una tabla bidimensional, un archivo de datos de catálogo consiste en un registro de encabezado que identifica las columnas de datos y cualquier número de registros de datos (filas). Los campos tanto en el encabezado como en los registros de datos están separados por `<TAB>` caracteres únicos. Los registros están separados por un solo `<CR>` (código ASCII 0xD), un único `<LF>` (código ASCII 0xA) o un par `<CR><LF>`.

El registro de encabezado debe contener los nombres exactos de cada campo de datos. Los campos vacíos no están permitidos en la fila de encabezado. Los nombres de los campos de datos no distinguen entre mayúsculas y minúsculas. Todos los nombres de campo deben ser únicos.

No se permite ningún espacio en blanco distinto de los separadores de campo `<TAB>` en los registros de datos y encabezados.

En los registros de datos, dos caracteres `<TAB>` adyacentes indican un campo vacío. Los campos vacíos heredarán los valores predeterminados de los atributos del catálogo o de los valores predeterminados del servidor.

Los campos de datos no deben contener caracteres `<CR>`, `<LF>` ni `<TAB>`, a menos que el valor de datos sea de tipo texto y esté entre comillas simples o dobles. Los campos de datos no deben tener codificación HTTP.

Los valores de datos múltiples del mismo campo se separan con comas (&#39;,&#39;), a menos que se indique lo contrario.

Columnas cuyos nombres inicio con &#39;.&#39; se ignoran; esto permite almacenar datos en catálogos de materiales que no interesan al procesamiento de imágenes. Las columnas con nombres de encabezado desconocidos se omiten y se escribe una advertencia en el archivo de registro.

Los nombres de campo pueden constar de cualquier combinación de letras ASCII, números, así como &quot;-&quot; y &quot;_&quot;.

Se pueden utilizar una o más columnas como claves de índice. Si la misma clave se produce más de una vez en el mismo archivo de datos, prevalecerá la instancia posterior.
