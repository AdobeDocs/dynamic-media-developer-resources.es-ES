---
description: Datos de usuario del catálogo de imágenes. Devuelve los datos de usuario de la entrada de catálogo de imágenes especificada en la ruta de URL.
seo-description: Datos de usuario del catálogo de imágenes. Devuelve los datos de usuario de la entrada de catálogo de imágenes especificada en la ruta de URL.
seo-title: userdata
solution: Experience Manager
title: userdata
topic: Scene7 Image Serving - Image Rendering API
uuid: 7a34adad-f1b6-45a7-94fe-1407845710e5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# userdata{#userdata}

Datos de usuario del catálogo de imágenes. Devuelve los datos de usuario de la entrada de catálogo de imágenes especificada en la ruta de URL.

`req=userdata[,text|{xml[, *`codificación`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codificación</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Se devuelve el contenido de `catalog::UserData` . Cuando se especifica el formato &#39;texto&#39;, todas las instancias de `??` in `catalog::UserData`se sustituyen por caracteres de fin de línea y se añade al final un único terminador de línea (CR/LF). Si la ruta de URL no se resuelve en una entrada de catálogo válida, la respuesta consiste únicamente en un terminador de línea único. Se aplica el formato adecuado cuando se solicita el formato &#39;xml&#39; o &#39;json&#39;.

Se omiten otros comandos de la cadena de solicitud.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

>[!NOTE]
>
>El carácter de dos puntos no está permitido en los nombres de claves de propiedad userdata.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del `req=` parámetro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
