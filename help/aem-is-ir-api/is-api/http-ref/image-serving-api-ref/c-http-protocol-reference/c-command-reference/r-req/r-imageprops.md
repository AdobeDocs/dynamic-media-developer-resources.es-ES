---
description: Propiedades de la imagen de origen. Devuelve las propiedades seleccionadas del archivo de imagen o de la entrada de catálogo especificada en la ruta de URL.
seo-description: Propiedades de la imagen de origen. Devuelve las propiedades seleccionadas del archivo de imagen o de la entrada de catálogo especificada en la ruta de URL.
seo-title: imageprops
solution: Experience Manager
title: imageprops
topic: Scene7 Image Serving - Image Rendering API
uuid: e9bf2780-a520-4fb1-ab4c-40bb799e36a4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# imageprops{#imageprops}

Propiedades de la imagen de origen. Devuelve las propiedades seleccionadas del archivo de imagen o de la entrada de catálogo especificada en la ruta de URL.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificador de solicitud único. </p></td> 
 </tr> 
</table>

The HTTP response is cacheable with the TTL based on `attribute::NonImgExpiration`.

Se omiten otros comandos de la cadena de solicitud.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del `req=` parámetro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.

Se devuelven las siguientes propiedades:

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> Propiedad</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descripción</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Anclaje</span> o punto de ancla predeterminado </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> doble </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Caducidad</span> o el tiempo de vida predeterminado </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p>Altura de la imagen en resolución completa en píxeles </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> Nombre o descripción del perfil asociado a esta imagen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> imagen. EmbeddedIccProfile</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 si el perfil asociado está incrustado en la imagen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.Embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 si la imagen incluye datos de ruta de Photoshop </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> imagen. EmbeddedXmpData</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 si la imagen incluye datos XMP </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 para ninguna máscara, 1 para alfa premultiplicado, 2 para alfa no premultiplicado y 3 para una imagen de máscara independiente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Modificador</span> o vacío si no es una entrada de catálogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> imagen. photoshopPathNames</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> lista separada por comas de los nombres de todas las rutas de Photoshop asociadas con esta imagen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> Tipo de imagen, puede ser 'CMYK', 'RGB' o 'BW' (para imágenes de escala de grises) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> <span class="codeph"> atributo::PostModifier</span> o vacío si no es una entrada de catálogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> resolución de impresión predeterminada en píxeles/pulgada </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Resolución</span> o resolución de objeto predeterminada </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p>Fecha y hora de modificación (desde <span class="codeph"> catálogo::TimeStamp</span> o el archivo de imagen) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> catálogo::ThumbRes</span> o la resolución de miniatura predeterminada </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catálogo::ThumbType</span> o el tipo de miniatura predeterminado </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p> Ancho de imagen de resolución completa en píxeles </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translateId</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> ID del catálogo en el que se resuelve el <span class="varname"> objeto</span> especificado en la ruta de acceso (consulte Traducción <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"></a>de ID de objeto). </p> </td> 
  </tr> 
 </tbody> 
</table>

