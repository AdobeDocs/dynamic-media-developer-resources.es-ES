---
title: req
description: Tipo de solicitud. Especifica el tipo de datos solicitados.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 4%

---

# req{#req}

Tipo de solicitud. Especifica el tipo de datos solicitados.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> depurar </span> </p> </td> 
  <td class="stentry"> <p>Ejecute comandos en modo de depuración. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> contenido </span> </p> </td> 
  <td class="stentry"> <p>Devuelve información sobre los objetos de la viñeta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>Ejecute comandos y devuelva la imagen procesada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>Devuelve las propiedades de la viñeta especificada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> mapa </span> </p> </td> 
  <td class="stentry"> <p>Devuelve datos de mapa de imagen incrustados en la viñeta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> objeto </span> </p> </td> 
  <td class="stentry"> <p>Ejecute comandos y devuelva la imagen procesada enmascarada a la selección de objeto actual. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>Ejecute comandos y devuelva propiedades de la imagen de respuesta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> userdata </span> </p> </td> 
  <td class="stentry"> <p>Devuelve el contenido de <span class="codeph"> viñeta::UserData </span>. </p> </td> 
 </tr> 
</table>

A menos que se indique lo contrario en las descripciones detalladas, el servidor devuelve respuestas de texto con tipo MIME &lt;text plain=&quot;&quot;>.

`debug`

Ejecuta los comandos especificados y devuelve la imagen procesada. Si se produce un error, se devuelve información de error y de depuración en lugar de la imagen de error ( `attribute::ErrorImagePath`).

`contents`

Devuelve una representación XML de la jerarquía de objetos de la viñeta, incluidos los atributos de objetos seleccionados. Otros comandos de la solicitud se ignoran.

`img`

Ejecuta los comandos especificados y devuelve la imagen procesada. El formato de datos de respuesta y el tipo de respuesta están determinados por `fmt=`.

`imageprops`

Devuelve las propiedades seleccionadas del archivo de viñeta o la entrada de catálogo especificada en la ruta de URL. Consulte [Propiedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) para obtener una descripción de la sintaxis de respuesta y el tipo MIME de respuesta. Otros comandos de la solicitud se ignoran. Se devuelven las siguientes propiedades:

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>Doble </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Caducidad </span> o el tiempo de vida predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>Entero </p> </td> 
   <td colname="col3"> <p>Altura de resolución completa en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>Cadena </p> </td> 
   <td colname="col3"> <p>nombre/descripción del perfil asociado con esta viñeta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>Sí/No </p> </td> 
   <td colname="col3"> <p>1 si el perfil asociado está incrustado en la viñeta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded.PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>Sí/No </p> </td> 
   <td colname="col3"> <p>1 si la viñeta incrusta los datos de ruta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>Cadena </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Modificador </span> o vacío si no es una entrada de catálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td colname="col2"> <p>Enumeración </p> </td> 
   <td colname="col3"> <p>Tipo de píxel de la imagen de respuesta; puede ser 'CMYK', 'RGB' o 'BW' (para imágenes en escala de grises). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolución de impresión predeterminada en ppp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>Cadena </p> </td> 
   <td colname="col3"> <p>Fecha y hora de modificación (desde <span class="codeph"> catalog::TimeStamp </span> o el archivo de viñeta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>Entero </p> </td> 
   <td colname="col3"> <p>Ancho de resolución completa en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> viñeta.nombre </span> </p> </td> 
   <td colname="col2"> <p>Cadena </p> </td> 
   <td colname="col3"> <p>Nombre de viñeta (cadena de nombre del objeto de viñeta raíz). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> viñeta.res </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolución máxima del objeto en <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> resolución material </a> unidades (normalmente píxeles/pulgada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> viñeta.res.avg </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolución de objeto promedio en <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> resolución material </a> unidades (normalmente píxeles/inc) <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> resolución material </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> viñeta.res.min </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolución mínima del objeto en <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> resolución material </a> unidades (normalmente píxeles/pulgada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>Entero </p> </td> 
   <td colname="col3"> <p>Número de versión del archivo de viñeta. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Devuelve los datos de mapa de imagen incluidos en la viñeta. De forma predeterminada, se devuelven los datos de asignación de todos los grupos exteriores. Los datos de asignación de todos los grupos más internos se pueden obtener con

`req=map&groupLevel=-1`

Los datos del mapa no se escalan a `wid=` o `hei=` o modificado de otro modo. El tipo MIME de respuesta es `<text/xml>`.

Los datos de respuesta constan de un `<map>` elemento que contiene un conjunto de `<area>` elementos, similares al HTML `<AREA>` etiqueta.

Cada `<area>` incluye el estándar `type=` y `coord=` atributos, y un `name=` , especificando el nombre del grupo de viñetas o la ruta de acceso del nombre. Múltiple `<area>` los elementos con el mismo nombre están presentes si las máscaras del grupo de objetos correspondiente tienen regiones discontinuas.

Además de los atributos predeterminados, las viñetas pueden definir atributos adicionales si se crean. Estos atributos personalizados se definen como atributos de grupo de objetos. Los nombres de los atributos personalizados deben comenzar por `map` que se incluirán en la `<area>` elementos. Por ejemplo, si los atributos de grupo incluyen `map.href=http://www.scene7.com`, el correspondiente `<area>` el elemento incluye `href="http://www.scene7.com"`.

Un documento XML con una etiqueta vacía `<map>` se devuelve si la viñeta no incluye datos de mapa.

`object`

Ejecuta los comandos especificados y devuelve la imagen procesada enmascarada por la selección de objeto residual (el grupo u objeto seleccionado con la última `sel=` o `obj=` en la solicitud). Normalmente se utiliza con un formato de imagen que admite alfa (consulte [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Si se utiliza un formato de imagen que no admite alfa, las áreas fuera de la máscara son de color negro.

`props`

Ejecuta los comandos especificados y devuelve propiedades de viñeta y propiedades de grupo u objeto, en lugar de la imagen procesada. Consulte [Propiedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) para obtener una descripción de la sintaxis de respuesta y el tipo MIME de respuesta. La selección predeterminada se aplica a menos que `obj=` o `sel=` también se especifica (consulte [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

En la respuesta pueden incluirse las siguientes propiedades:

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Propiedad </p> </th> 
   <th class="entry"> <p> Tipo </p> </th> 
   <th class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> Color de fondo de imagen de respuesta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>Entero </p> </td> 
   <td> <p> Altura de la imagen de respuesta en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> Sí/No </p> </td> 
   <td> <p>True si el perfil ICC está incrustado en la imagen de respuesta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> Nombre de acceso directo del perfil asociado a la imagen de respuesta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> Sí/No </p> </td> 
   <td> <p> True si la imagen de respuesta incluye alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> Sí/No </p> </td> 
   <td> <p> True si la imagen de respuesta incluye datos de ruta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> El tipo de imagen de respuesta puede ser 'CMYK', 'RGB' o 'BW' (para imágenes en escala de grises) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> Resolución de impresión (ppp) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>Entero, booleano </p> </td> 
   <td> <p> Calidad JPEG e indicador de croma (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> Tipo MIME para la imagen de respuesta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Ancho de la imagen de respuesta en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> Cadena de atributos de la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Número de objetos de la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Aplicar sangría al valor de la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> Ruta de nombre completo de la selección de objeto actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> número de objetos de superposición en la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p>Número de objetos procesables en la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Número de objetos texturables de la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Estado actual de mostrar/ocultar de la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Valor del orden Z del primer objeto de superposición de la selección actual. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Devuelve el contenido de `vignette::UserData`. El servidor reemplaza todas las apariciones de `'??'` in `vignette::UserData` con terminadores de línea ( `<cr><lf>`). La respuesta tiene el formato de datos de texto con el tipo MIME de respuesta establecido en &lt;text plain=&quot;&quot;>.

Si el objeto especificado en la ruta URL no se resuelve en una entrada de mapa de viñeta válida, o si la variable `vignette::UserData` está vacío, la respuesta solo contiene un terminador de línea ( `CR/LF`).

Los demás comandos de la cadena de solicitud se omiten.

## Propiedades {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Solicitar comando. Puede producirse en cualquier lugar de la cadena de solicitud.

## Predeterminado {#section-00c593cbf1af4364b6b78812e6b93c64}

Si la dirección URL no incluye una ruta de imagen o modificadores, haga lo siguiente:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

De lo contrario, `req=img`

## Véase también {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [viñeta::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Propiedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
