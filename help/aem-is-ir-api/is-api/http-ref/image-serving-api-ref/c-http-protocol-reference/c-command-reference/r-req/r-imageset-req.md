---
description: Datos del conjunto de imágenes del catálogo de imágenes. Devuelve los datos del conjunto de imágenes para la entrada del catálogo de imágenes especificada en la ruta de URL.
seo-description: Datos del conjunto de imágenes del catálogo de imágenes. Devuelve los datos del conjunto de imágenes para la entrada del catálogo de imágenes especificada en la ruta de URL.
seo-title: imageset
solution: Experience Manager
title: imageset
topic: Scene7 Image Serving - Image Rendering API
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# imageset{#imageset}

Datos del conjunto de imágenes del catálogo de imágenes. Devuelve los datos del conjunto de imágenes para la entrada del catálogo de imágenes especificada en la ruta de URL.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificación</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador de solicitud único. </p></td> 
 </tr> 
</table>

El contenido de `catalog::ImageSet` se devuelve sin más modificaciones (excepto localización de cadena, si procede), seguido de un terminador de una sola línea (CR/LF). Si la ruta de URL no se resuelve en una entrada de catálogo válida, la respuesta consiste únicamente en un terminador de línea único.

Se omiten otros comandos de la cadena de solicitud. The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del `req=` parámetro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
