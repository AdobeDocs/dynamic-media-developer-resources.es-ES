---
description: Datos de velocidad de bits múltiple.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# mbrSet{#mbrset}

Datos de velocidad de bits múltiple.

`req=mbrSet[,text|xml[, *`codificación`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificación</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

Devuelve una respuesta de texto o xml que contiene una lista de direcciones URL (y las tasas de bits correspondientes) que corresponden a entradas de vídeo válidas en el conjunto de vídeos asociado con el ID de ruta de acceso de red.

Se ha relajado el requisito anterior de que una entrada de vídeo válida contenga un valor para `catalog::VideoBitRate`. La entrada puede contener un valor para `catalog::VideoBitRate`*o* `catalog::AudioBitRate`*o* `catalog::TotalStreamBitRate`. Solo es necesario definir una de ellas para que la entrada de vídeo sea válida. Tenga en cuenta que los requisitos de `catalog::Path` y una extensión de archivo de vídeo válida no han cambiado.

Las respuestas están pensadas para el consumo por parte de los servidores de flujo continuo Apple y Flash y, por lo tanto, cumplen estructuralmente esas especificaciones. Las direcciones URL se generan utilizando los prefijos `attribute::HttpAppleStreamingContext` y `attribute::HttpFlashStreamingContext`.

Las respuestas m3u8 solo contienen archivos mp4 si hay alguno presente en el conjunto de vídeos. Si no hay archivos mp4, estas respuestas solo contienen archivos f4v. Si no hay archivos mp4 ni f4v, la respuesta está vacía.

Las respuestas de f4m solo contienen archivos f4v si hay alguno presente en el conjunto de vídeos. Si no hay archivos f4v, estas respuestas solo contienen archivos mp4. Si no hay archivos f4v ni archivos mp4, la respuesta está vacía.

Las tasas de bits que aparecen en las respuestas de f4m/m3u8 corresponden a los valores de `catalog::TotalStreamBitRate` (convertidos en unidades adecuadas). Si `catalog::TotalStreamBitRate` no está definido, se usa la suma de `catalog::VideoBitRate` y `catalog::AudioBitRate`.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::NonImgExpiration`.
