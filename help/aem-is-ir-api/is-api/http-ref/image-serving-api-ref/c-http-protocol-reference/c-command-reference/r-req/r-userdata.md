---
description: Datos de usuario del catálogo de imágenes. Devuelve los datos de usuario de la entrada de catálogo de imágenes especificada en la ruta de URL.
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
TQID: 'https://experienceleague.adobe.com/cLVsaN--jydZTkV6GA92jN1PO8VOFAEZxhSg7F2S9dk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

---

# userdata{#userdata}

Datos de usuario del catálogo de imágenes. Devuelve los datos de usuario de la entrada de catálogo de imágenes especificada en la ruta de URL.

`req=userdata[,text|{xml[, *`codificación`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codificación</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Se devuelve el contenido de `catalog::UserData`. Cuando se especifica el formato &#39;text&#39;, todas las instancias de `??` en `catalog::UserData`se reemplazan por terminadores de línea y se anexa un terminador de una sola línea (CR/LF) al final. Si la ruta URL no se resuelve en una entrada de catálogo válida, la respuesta consiste únicamente en un terminador de una sola línea. Se aplica el formato adecuado cuando se solicita el formato &quot;xml&quot; o &quot;json&quot;.

Se omiten otros comandos de la cadena de solicitud.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.

>[!NOTE]
>
>No se permite el carácter de dos puntos en los nombres de clave de propiedad userdata.

Las solicitudes compatibles con el formato de respuesta JSONP le permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
