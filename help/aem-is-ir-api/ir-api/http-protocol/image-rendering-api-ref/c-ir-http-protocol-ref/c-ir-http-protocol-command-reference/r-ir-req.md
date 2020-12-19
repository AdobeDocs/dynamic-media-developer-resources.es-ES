---
description: Tipo de solicitud. Especifica el tipo de datos solicitados.
seo-description: Tipo de solicitud. Especifica el tipo de datos solicitados.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dd13338-3457-477f-96e7-3ace7266d0ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# req{#req}

Tipo de solicitud. Especifica el tipo de datos solicitados.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> debug  </span> </p> </td> 
  <td class="stentry"> <p>Ejecutar comandos en modo de depuración. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> contenido </span> </p> </td> 
  <td class="stentry"> <p>Devuelve información sobre los objetos de la viñeta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>Ejecute comandos y devuelva la imagen representada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops  </span> </p> </td> 
  <td class="stentry"> <p>Propiedades de retorno de la viñeta especificada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> mapa </span> </p> </td> 
  <td class="stentry"> <p>Devuelve datos de mapa de imagen incrustados en la viñeta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> objeto </span> </p> </td> 
  <td class="stentry"> <p>Ejecute comandos y devuelva la imagen procesada enmascarada a la selección de objetos actual. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>Ejecute comandos y devuelva propiedades de la imagen de respuesta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> userdata  </span> </p> </td> 
  <td class="stentry"> <p>Devuelve el contenido de la viñeta <span class="codeph">::UserData </span>. </p> </td> 
 </tr> 
</table>

A menos que se indique lo contrario en las descripciones detalladas, el servidor devuelve respuestas de texto con tipo MIME &lt;text/plain>.

`debug`

Ejecuta los comandos especificados y devuelve la imagen representada. Si se produce un error, se devuelve la información de error y depuración en lugar de la imagen de error ( `attribute::ErrorImagePath`).

`contents`

Devuelve una representación XML de la jerarquía de objetos en la viñeta, incluidos los atributos de objeto seleccionados. Se omiten otros comandos de la solicitud.

`img`

Ejecuta los comandos especificados y devuelve la imagen representada. El formato de datos de respuesta y el tipo de respuesta están determinados por `fmt=`.

`imageprops`

Devuelve las propiedades seleccionadas del archivo de viñeta o de la entrada de catálogo especificada en la ruta URL. Consulte [Propiedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) para obtener una descripción de la sintaxis de respuesta y el tipo MIME de respuesta. Se omiten otros comandos de la solicitud. Se devuelven las siguientes propiedades:

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
   <td colname="col1"> <p> <span class="codeph"> image.expiration  </span> </p> </td> 
   <td colname="col2"> <p>Doble </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo::Caducidad  </span> o el tiempo de vida predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td colname="col2"> <p>Entero </p> </td> 
   <td colname="col3"> <p>Altura de resolución completa en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td colname="col2"> <p>Cadena </p> </td> 
   <td colname="col3"> <p>nombre/descripción del perfil asociado a esta viñeta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.EmbeddedIccProfile  </span> </p> </td> 
   <td colname="col2"> <p>Sí/No </p> </td> 
   <td colname="col3"> <p>1 si el perfil asociado está incrustado en la viñeta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.Embedded PhotoshopPaths  </span> </p> </td> 
   <td colname="col2"> <p>Sí/No </p> </td> 
   <td colname="col3"> <p>1 si la viñeta incrusta datos de ruta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier  </span> </p> </td> 
   <td colname="col2"> <p>Cadena </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo::Modificador  </span> o vacío si no es una entrada de catálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Tipo de píxel de la imagen de respuesta; puede ser 'CMYK', 'RGB' o 'BW' (para imágenes en escala de grises). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolución de impresión predeterminada en ppp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp  </span> </p> </td> 
   <td colname="col2"> <p>Cadena </p> </td> 
   <td colname="col3"> <p>Fecha y hora de modificación (desde <span class="codeph"> catálogo::TimeStamp </span> o el archivo de viñeta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td colname="col2"> <p>Entero </p> </td> 
   <td colname="col3"> <p>Ancho de resolución completo en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name  </span> </p> </td> 
   <td colname="col2"> <p>Cadena </p> </td> 
   <td colname="col3"> <p>Nombre de viñeta (cadena de nombre del objeto de viñeta raíz). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolución máxima del objeto en <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unidades de resolución del material </a> (normalmente píxeles/pulgada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolución media de objeto en <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unidades de resolución de material </a> (normalmente píxeles/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> resolución de material </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolución mínima del objeto en <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unidades de resolución del material </a> (normalmente píxeles/pulgada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version  </span> </p> </td> 
   <td colname="col2"> <p>Entero </p> </td> 
   <td colname="col3"> <p>Número de versión del archivo de viñeta. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Devuelve los datos del mapa de imagen incluidos en la viñeta. De forma predeterminada, se devuelven los datos del mapa para todos los grupos externos. Los datos del mapa de todos los grupos más internos se pueden obtener con

`req=map&groupLevel=-1`

Los datos del mapa no se escalan a `wid=` o `hei=` ni se modifican de otro modo. El tipo MIME de respuesta es `<text/xml>`.

Los datos de respuesta constan de un elemento `<map>` que contiene un conjunto de elementos `<area>`, similar a la etiqueta HTML `<AREA>`.

Cada elemento `<area>` incluye los atributos estándar `type=` y `coord=`, así como un atributo `name=` que especifica el nombre del grupo de viñeta o la ruta de nombre. Si las máscaras del grupo de objetos correspondiente tienen regiones discontinuas, estarán presentes varios elementos `<area>` con el mismo nombre.

Además de los atributos predeterminados, las viñetas pueden definir atributos adicionales si se crean. Estos atributos personalizados se definen como atributos de grupo de objetos. Los nombres de los atributos personalizados deben comenzar por `map`. que se incluirá en los elementos `<area>`. Por ejemplo, si los atributos de grupo incluyen `map.href=http://www.scene7.com`, el elemento `<area>` correspondiente incluirá `href="http://www.scene7.com"`.

Se devuelve un documento XML con un elemento vacío `<map>` si la viñeta no incluye datos de asignación.

`object`

Ejecuta los comandos especificados y devuelve la imagen procesada enmascarada por la selección de objetos residuales (el grupo u objeto seleccionado con el último comando `sel=` o `obj=` de la solicitud). Normalmente se utiliza junto con un formato de imagen que admite alfa (consulte [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Si se utiliza un formato de imagen que no admite alfa, las áreas fuera de la máscara son de color negro.

`props`

Ejecuta los comandos especificados y devuelve propiedades de viñeta y propiedades de grupo u objeto, en lugar de la imagen representada. Consulte [Propiedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) para obtener una descripción de la sintaxis de respuesta y el tipo MIME de respuesta. La selección predeterminada se aplica a menos que también se especifique `obj=` o `sel=` (consulte [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

En la respuesta se pueden incluir las siguientes propiedades:

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
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> Responda al color de fondo de la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p>Entero </p> </td> 
   <td> <p> Responder la altura de la imagen en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> Sí/No </p> </td> 
   <td> <p>True si el perfil ICC se incrustará en la imagen de respuesta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> Nombre de método abreviado del perfil asociado con la imagen de respuesta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> Sí/No </p> </td> 
   <td> <p> True si la imagen de respuesta incluye alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> Sí/No </p> </td> 
   <td> <p> True si la imagen de respuesta incluye datos de ruta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> El tipo de imagen de respuesta puede ser 'CMYK', 'RGB' o 'BW' (para imágenes en escala de grises) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> Resolución de impresión (ppp) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p>Entero, booleano </p> </td> 
   <td> <p> Calidad JPEG y indicador de croma (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> Tipo de MIME para la imagen de respuesta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Responder la anchura de la imagen en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select.attributes  </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> Cadena de atributos para la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selected.count  </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Número de objetos de la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select.ident  </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Sangrar el valor de la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select  <span class="codeph"> Selection.attributes  </span>ion.name  </span> </p> </td> 
   <td> <p> Cadena </p> </td> 
   <td> <p> Ruta de acceso con nombre completo de la selección de objetos actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selección.superposición  </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> número de objetos de superposición en la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select.renderable  </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p>Número de objetos procesables en la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select.texturable  </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Número de objetos texturables de la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select.visible  </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Estado actual de mostrar u ocultar la selección actual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select.zorder  </span> </p> </td> 
   <td> <p> Entero </p> </td> 
   <td> <p> Valor de orden Z del primer objeto de superposición en la selección actual. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Devuelve el contenido de `vignette::UserData`. El servidor reemplazará todas las ocurrencias de `'??'` en `vignette::UserData` por terminadores de línea ( `<cr><lf>`). La respuesta tiene el formato de datos de texto con el tipo MIME de respuesta definido como &lt;text/plain>.

Si el objeto especificado en la ruta de URL no se resuelve en una entrada de mapa de viñetas válida o si `vignette::UserData` está vacío, la respuesta sólo contendrá un terminador de líneas ( `CR/LF`).

Los demás comandos de la cadena de solicitud se omiten.

## Propiedades {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Solicitar. Puede ocurrir en cualquier parte de la cadena de solicitud.

## Predeterminado {#section-00c593cbf1af4364b6b78812e6b93c64}

Si la dirección URL no incluye una ruta de imagen o modificadores, entonces:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

De lo contrario, `req=img`

## Véase también {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) ,  [atributo::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0),  [viñeta::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85),  [Propiedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
