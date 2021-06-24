---
description: Zoom dirige los datos del catálogo de imágenes. Devuelve datos de destino de zoom para la entrada de catálogo de imágenes especificada en la ruta URL.
solution: Experience Manager
title: objetivo
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---

# objetivo{#targets}

Zoom dirige los datos del catálogo de imágenes. Devuelve datos de destino de zoom para la entrada de catálogo de imágenes especificada en la ruta URL.

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador de solicitud única. </p></td> 
 </tr> 
</table>

Se devuelve el contenido de `catalog::Targets`. Cuando se solicita el formato &quot;texto&quot;, todas las instancias de `??` en `catalog::Targets` se sustituyen por caracteres de fin de línea y se añade al final un solo terminador de línea ( `CR/LF`). Si la ruta URL no se resuelve en una entrada de catálogo válida, la respuesta consiste únicamente en un terminador de línea único. Se aplica el formato adecuado cuando se solicita el formato &quot;xml&quot; o &quot;json&quot;.

Se omiten otros comandos de la cadena de solicitud.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
