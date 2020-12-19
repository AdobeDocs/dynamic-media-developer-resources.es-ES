---
description: Datos de velocidad de bits múltiple.
seo-description: Datos de velocidad de bits múltiple.
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# mbrSet{#mbrset}

Datos de velocidad de bits múltiple.

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

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

Devuelve un texto o una respuesta xml que contiene una lista de direcciones URL (y las tasas de bits correspondientes) que corresponden a entradas de vídeo válidas en el conjunto de vídeos asociado con la identificación de ruta de red.

El requisito previo de que una entrada de vídeo válida contenga un valor para `catalog::VideoBitRate` ahora se ha relajado. La entrada puede contener un valor para `catalog::VideoBitRate`*o* `catalog::AudioBitRate`*o* `catalog::TotalStreamBitRate`. Solo es necesario definir uno de estos parámetros para que la entrada de vídeo sea válida. Tenga en cuenta que los requisitos para `catalog::Path` y una extensión de archivo de vídeo válida no han cambiado.

Las respuestas están destinadas al consumo de los servidores de flujo de Apple y Flash y, por lo tanto, se ajustan estructuralmente a estas especificaciones. Las direcciones URL se generan utilizando prefijos `attribute::HttpAppleStreamingContext` y `attribute::HttpFlashStreamingContext`.

Las respuestas m3u8 solo contienen archivos mp4 si hay alguno presente en el conjunto de vídeos. Si no hay archivos mp4, estas respuestas solo contienen archivos f4v. Si no hay archivos mp4 ni f4v, la respuesta está vacía.

Las respuestas de f4m solo contienen archivos f4v si hay alguno presente en el conjunto de vídeos. Si no hay archivos f4v, estas respuestas solo contienen archivos mp4. Si no hay archivos f4v ni mp4, la respuesta estará vacía.

Las velocidades de bits que aparecen en las respuestas f4m/m3u8 corresponden a los valores en `catalog::TotalStreamBitRate` (convertidos a unidades adecuadas). Si no se define `catalog::TotalStreamBitRate`, se utiliza la suma de `catalog::VideoBitRate` y `catalog::AudioBitRate`.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::NonImgExpiration`.
