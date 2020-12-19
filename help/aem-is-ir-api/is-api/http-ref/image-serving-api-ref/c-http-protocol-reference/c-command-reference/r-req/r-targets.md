---
description: Zoom destinatarios datos del catálogo de imágenes. Devuelve datos de destinatario de zoom para la entrada de catálogo de imágenes especificada en la ruta de URL.
seo-description: Zoom destinatarios datos del catálogo de imágenes. Devuelve datos de destinatario de zoom para la entrada de catálogo de imágenes especificada en la ruta de URL.
seo-title: objetivo
solution: Experience Manager
title: objetivo
topic: Scene7 Image Serving - Image Rendering API
uuid: e20dcd2c-913a-4153-97c7-dfb190763e39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# objetivo{#targets}

Zoom destinatarios datos del catálogo de imágenes. Devuelve datos de destinatario de zoom para la entrada de catálogo de imágenes especificada en la ruta de URL.

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificación</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador de solicitud único. </p></td> 
 </tr> 
</table>

Se devuelve el contenido de `catalog::Targets`. Cuando se solicita el formato &#39;texto&#39;, todas las instancias de `??` en `catalog::Targets` se reemplazan por caracteres de fin de línea y se anexa al final un único terminador de línea ( `CR/LF`). Si la ruta de URL no se resuelve en una entrada de catálogo válida, la respuesta consiste únicamente en un terminador de línea único. Se aplica el formato adecuado cuando se solicita el formato &#39;xml&#39; o &#39;json&#39;.

Se omiten otros comandos de la cadena de solicitud.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
