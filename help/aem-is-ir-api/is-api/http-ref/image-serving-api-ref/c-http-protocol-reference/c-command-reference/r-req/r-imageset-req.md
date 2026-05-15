---
description: Datos del conjunto de imágenes del catálogo de imágenes. Devuelve los datos del conjunto de imágenes para la entrada de catálogo de imágenes especificada en la ruta URL.
solution: Experience Manager
title: conjunto de imágenes
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
TQID: 'https://experienceleague.adobe.com/1PbZjs--lk7GcyXU1F-AJ-vWcgwVX9JFivvbnTGrWKQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# conjunto de imágenes{#imageset}

Datos del conjunto de imágenes del catálogo de imágenes. Devuelve los datos del conjunto de imágenes para la entrada de catálogo de imágenes especificada en la ruta URL.

`req=imageset[,text|javascript|{xml[, *`codificación`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificación</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador único de la solicitud. </p></td> 
 </tr> 
</table>

El contenido de `catalog::ImageSet` se devuelve sin más modificaciones (excepto la localización de cadenas, si corresponde), seguida de un terminador de una sola línea (CR/LF). Si la ruta URL no se resuelve en una entrada de catálogo válida, la respuesta consiste únicamente en un terminador de una sola línea.

Se omiten otros comandos de la cadena de solicitud. La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::NonImgExpiration`.

Las solicitudes compatibles con el formato de respuesta JSONP le permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
