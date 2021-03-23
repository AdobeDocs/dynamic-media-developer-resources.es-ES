---
description: Datos del conjunto de imágenes del catálogo de imágenes. Devuelve los datos del conjunto de imágenes para la entrada del catálogo de imágenes especificada en la ruta URL.
seo-description: Datos del conjunto de imágenes del catálogo de imágenes. Devuelve los datos del conjunto de imágenes para la entrada del catálogo de imágenes especificada en la ruta URL.
seo-title: imageset
solution: Experience Manager
title: imageset
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
feature: Dynamic Media Classic,SDK/API,Conjuntos de imágenes
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# imageset{#imageset}

Datos del conjunto de imágenes del catálogo de imágenes. Devuelve los datos del conjunto de imágenes para la entrada del catálogo de imágenes especificada en la ruta URL.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificación</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador de solicitud única. </p></td> 
 </tr> 
</table>

El contenido de `catalog::ImageSet` se devuelve sin más modificaciones (excepto la localización de cadenas, si corresponde), seguido de un terminador de una sola línea (CR/LF). Si la ruta URL no se resuelve en una entrada de catálogo válida, la respuesta consiste únicamente en un terminador de línea único.

Se omiten otros comandos de la cadena de solicitud. La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::NonImgExpiration`.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
