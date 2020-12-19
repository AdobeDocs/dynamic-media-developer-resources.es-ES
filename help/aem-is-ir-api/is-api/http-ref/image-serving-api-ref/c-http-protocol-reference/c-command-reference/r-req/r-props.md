---
description: Propiedades de datos de respuesta. Evalúa la solicitud actual como si fuera una solicitud de imagen (req=img), pero en lugar de devolver la imagen, el servidor devuelve las propiedades seleccionadas de la imagen de respuesta.
seo-description: Propiedades de datos de respuesta. Evalúa la solicitud actual como si fuera una solicitud de imagen (req=img), pero en lugar de devolver la imagen, el servidor devuelve las propiedades seleccionadas de la imagen de respuesta.
seo-title: props
solution: Experience Manager
title: props
topic: Scene7 Image Serving - Image Rendering API
uuid: b9325654-81d6-4f00-bf0a-36650bea6b8d
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 8%

---


# props{#props}

Propiedades de datos de respuesta. Evalúa la solicitud actual como si fuera una solicitud de imagen (req=img), pero en lugar de devolver la imagen, el servidor devuelve las propiedades seleccionadas de la imagen de respuesta.

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId  </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificador de solicitud único. </p> </td> 
 </tr> 
</table>

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.

Consulte [Propiedades](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) para obtener una descripción de la sintaxis de respuesta y el tipo MIME de respuesta. La respuesta HTTP se puede almacenar en caché con un TTL basado en `attribute::NonImgExpiration`.

Se devuelven las siguientes propiedades para las solicitudes /is/image:

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> Propiedad</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descripción</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> Color de fondo (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p> Responder la altura de la imagen en píxeles </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> True si el perfil ICC está incrustado en la imagen de respuesta. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> Nombre o descripción del perfil asociado a la imagen de respuesta. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length  </span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p> Tamaño de respuesta en píxeles que no incluye el encabezado HTTP; 0 si el servidor no ha almacenado previamente en caché los datos de la imagen de respuesta. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 1 si la imagen de respuesta incluye un canal alfa, 0 en caso contrario. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> El tipo de imagen de respuesta puede ser <span class="codeph"> CMYK </span>, <span class="codeph"> RGB </span> o <span class="codeph"> BW </span> (para imágenes en escala de grises). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 si la imagen de respuesta incrusta algún trazado, 0 en caso contrario. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> Resolución de impresión (ppp) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p> Calidad JPEG. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> Tipo de MIME para la imagen de respuesta. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p> Responder la anchura de la imagen en píxeles. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed  </span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 si la imagen de respuesta incrusta datos xmp, 0 en caso contrario. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version  </span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> Identificador de versión de imagen. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version  </span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> Identificador de versión de metadatos. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

Se devuelven las siguientes propiedades para solicitudes `/is/content`:

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> Propiedad</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descripción</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ruta </span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p>Ruta de archivo parcialmente resuelta. (Consulte <span class="codeph"> static::Path </span>.) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> length </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> Tamaño del archivo de objeto en bytes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> vencimiento </span> </p> </td> 
   <td> <p> doble </p> </td> 
   <td> <p> <span class="codeph"> static::Expiration  </span> o el tiempo de vida predeterminado </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified  </span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> Fecha y hora de modificación (desde <span class="codeph"> static::TimeStamp </span> o el archivo de objeto) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType  </span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> <span class="codeph"> static::UserType  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

