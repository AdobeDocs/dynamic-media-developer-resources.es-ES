---
description: Los archivos de datos de catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini). Se pueden mantener fácilmente mediante aplicaciones que admiten archivos de datos de texto delimitados por tabuladores, como Microsoft Excel y Access.
solution: Experience Manager
title: Archivos de datos de catálogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
TQID: 'https://experienceleague.adobe.com/h4-MIosWMEWhmbAYbpS9xm22nDzEPO6APGEezCA1B-Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 0%

---

# Archivos de datos de catálogo{#catalog-data-files}

Los archivos de datos de catálogo pueden tener cualquier nombre y sufijo de archivo (excepto .ini). Se pueden mantener fácilmente mediante aplicaciones que admiten archivos de datos de texto delimitados por tabuladores, como Microsoft Excel y Access.

Básicamente una tabla bidimensional, un archivo de datos de catálogo consta de un registro de encabezado que identifica las columnas de datos y cualquier número de registros de datos (filas). Los campos del encabezado y de los registros de datos están separados por `<TAB>` caracteres. Los registros están separados por un único `<CR>` (código ASCII `0xD`), un único `<LF>` (código ASCII `0xA`) o un par `<CR><LF>`.

El registro de encabezado debe contener los nombres exactos para cada campo de datos. No se permiten campos vacíos en la fila del encabezado. Los nombres de los campos de datos no distinguen entre mayúsculas y minúsculas. Todos los nombres de campo deben ser únicos.

Los caracteres de espacio no se pueden usar como separadores de campo. No se permiten espacios en el registro de encabezado. En los registros de datos, cualquier espacio al principio o al final de un campo de datos se considera parte de ese campo de datos.

En los registros de datos, dos caracteres `<TAB>` adyacentes indican un campo vacío. Los campos vacíos pueden heredar los valores predeterminados de los atributos de catálogo o de los valores predeterminados del servidor.

Los campos de datos se pueden incluir opcionalmente entre comillas dobles. No deben contener los caracteres `<CR>`, `<LF>` o `<TAB>`, a menos que el valor de los datos sea de tipo texto y esté entre comillas dobles. Los campos de datos no deben tener codificación HTTP.

A menos que se indique lo contrario, los valores de datos múltiples del mismo campo se separan con comas.

Columnas cuyos nombres empiezan por &quot;.&quot; se ignoran. Esto permite almacenar los datos en catálogos de imágenes, lo que no interesa al servicio de imágenes. Las columnas con nombres de encabezado desconocidos se omiten y se escribe una advertencia en el archivo de registro.

Los nombres de campo pueden consistir en cualquier combinación de letras ASCII, números, así como &quot;-&quot; y &quot;_&quot;.

Se pueden usar una o más columnas como claves de índice. Si la misma clave se produce más de una vez en el mismo archivo de datos, prevalecerá la instancia posterior.
