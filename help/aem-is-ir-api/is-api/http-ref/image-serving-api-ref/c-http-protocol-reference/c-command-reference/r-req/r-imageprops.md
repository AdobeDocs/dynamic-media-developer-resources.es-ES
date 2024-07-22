---
description: Propiedades de imagen de Source. Devuelve las propiedades seleccionadas del archivo de imagen o la entrada de catálogo especificada en la ruta URL.
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 4%

---

# imageprops{#imageprops}

Propiedades de imagen de Source. Devuelve las propiedades seleccionadas del archivo de imagen o la entrada de catálogo especificada en la ruta URL.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificador único de la solicitud. </p></td> 
 </tr> 
</table>

La respuesta HTTP se puede almacenar en caché con el TTL basado en `attribute::NonImgExpiration`.

Se omiten otros comandos de la cadena de solicitud.

Las solicitudes compatibles con el formato de respuesta JSONP le permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.

Se devuelven las siguientes propiedades:

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> propiedad</b> </td> 
   <td> <b> tipo</b> </td> 
   <td> <b> Descripción</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> o el punto de ancla predeterminado </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> doble </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Caducidad</span> o el tiempo de vida predeterminado </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p>Altura de imagen de resolución completa en píxeles </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> Nombre/descripción del perfil asociado a esta imagen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> imagen. embeddedIccProfile</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 si el perfil asociado está incrustado en la imagen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 si la imagen incluye datos de ruta de Photoshop </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> imagen. embeddedXmpData</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> XMP 1 si la imagen incluye datos de la </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 para máscara sin, 1 para alfa premultiplicado, 2 para alfa no premultiplicado y 3 para una imagen de máscara independiente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Modificador</span> o vacío si no es una entrada de catálogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> imagen. photoshopPathNames</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> Lista separada por comas de los nombres de todas las rutas de Photoshop asociadas con esta imagen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> El tipo de imagen puede ser 'CMYK', 'RGB' o 'BW' (para imágenes en escala de grises) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> <span class="codeph"> attribute::PostModifier</span> o vacío si no es una entrada de catálogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> resolución de impresión predeterminada en píxeles/pulgada </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Resolution</span> o la resolución de objeto predeterminada </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p>Fecha y hora de modificación (del catálogo <span class="codeph">::TimeStamp</span> o del archivo de imagen) </p> </td> 
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
   <td> <p> Anchura de la imagen de resolución completa en píxeles </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> cadena </p> </td> 
   <td> <p> Id. de catálogo al que se ha resuelto el objeto <span class="varname"> </span> especificado en la ruta de acceso (consulte Traducción de id. de objeto <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> </a>). </p> </td> 
  </tr> 
 </tbody> 
</table>
