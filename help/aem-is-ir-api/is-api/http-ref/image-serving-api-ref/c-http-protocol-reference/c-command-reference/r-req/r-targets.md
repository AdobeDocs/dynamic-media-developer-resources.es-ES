---
description: Destinos de zoom datos del catálogo de imágenes. Devuelve los datos de destino de zoom para la entrada de catálogo de imágenes especificada en la ruta URL.
solution: Experience Manager
title: objetivo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# objetivo{#targets}

Destinos de zoom datos del catálogo de imágenes. Devuelve los datos de destino de zoom para la entrada de catálogo de imágenes especificada en la ruta URL.

`req=targets[,text|{xml[, *`codificación`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificación</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador único de la solicitud. </p></td> 
 </tr> 
</table>

El contenido de `catalog::Targets` se devuelven. Cuando se solicita el formato &quot;texto&quot;, todas las instancias de `??` in `catalog::Targets` se sustituyen por terminadores de línea y un terminador de línea única ( `CR/LF`) se anexa al final. Si la ruta URL no se resuelve en una entrada de catálogo válida, la respuesta consiste únicamente en un terminador de una sola línea. Se aplica el formato adecuado cuando se solicita el formato &quot;xml&quot; o &quot;json&quot;.

Se omiten otros comandos de la cadena de solicitud.

La respuesta HTTP se puede almacenar en caché con el TTL en función de `catalog::Expiration`.

Las solicitudes compatibles con el formato de respuesta JSONP permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida de `req=` parámetro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
