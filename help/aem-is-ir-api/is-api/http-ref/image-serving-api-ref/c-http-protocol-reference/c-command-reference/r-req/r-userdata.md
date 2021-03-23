---
description: Datos de usuario del catálogo de imágenes. Devuelve los datos de usuario de la entrada de catálogo de imágenes especificada en la ruta url.
seo-description: Datos de usuario del catálogo de imágenes. Devuelve los datos de usuario de la entrada de catálogo de imágenes especificada en la ruta url.
seo-title: userdata
solution: Experience Manager
title: userdata
uuid: 7a34adad-f1b6-45a7-94fe-1407845710e5
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 2%

---


# userdata{#userdata}

Datos de usuario del catálogo de imágenes. Devuelve los datos de usuario de la entrada de catálogo de imágenes especificada en la ruta url.

`req=userdata[,text|{xml[, *`codificación`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codificación</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Se devuelve el contenido de `catalog::UserData`. Cuando se especifica el formato &quot;texto&quot;, todas las instancias de `??` en `catalog::UserData`se sustituyen por caracteres de fin de línea y se añade al final un terminador de línea único (CR/LF). Si la ruta URL no se resuelve en una entrada de catálogo válida, la respuesta consiste únicamente en un terminador de línea único. Se aplica el formato adecuado cuando se solicita el formato &quot;xml&quot; o &quot;json&quot;.

Se omiten otros comandos de la cadena de solicitud.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.

>[!NOTE]
>
>No se permite el carácter de dos puntos en los nombres de claves de propiedad userdata.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
