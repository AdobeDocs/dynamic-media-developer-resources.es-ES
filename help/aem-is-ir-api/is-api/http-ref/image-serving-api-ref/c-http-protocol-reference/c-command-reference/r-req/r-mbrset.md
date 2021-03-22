---
description: Datos de velocidad de bits múltiples.
seo-description: Datos de velocidad de bits múltiples.
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# mbrSet{#mbrset}

Datos de velocidad de bits múltiples.

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

Devuelve una respuesta de texto o xml que contiene una lista de direcciones URL (y las tasas de bits correspondientes) que corresponden a entradas de vídeo válidas en un conjunto de vídeos asociado con el id de ruta de acceso de red.

Se ha relajado el requisito anterior de que una entrada de vídeo válida contenga un valor para `catalog::VideoBitRate`. La entrada puede contener un valor para `catalog::VideoBitRate`*o* `catalog::AudioBitRate`*o* `catalog::TotalStreamBitRate`. Solo es necesario definir uno de estos elementos para que la entrada de vídeo sea válida. Tenga en cuenta que los requisitos para `catalog::Path` y una extensión de archivo de vídeo válida no han cambiado.

Las respuestas están destinadas al consumo de los servidores de transmisión de Apple y Flash y, por lo tanto, se ajustan estructuralmente a esas especificaciones. Las direcciones URL se generan utilizando los prefijos `attribute::HttpAppleStreamingContext` y `attribute::HttpFlashStreamingContext`.

Las respuestas m3u8 solo contienen archivos mp4 si hay alguno presente en el conjunto de vídeos. Si no hay archivos mp4, estas respuestas solo contienen archivos f4v. Si no hay archivos mp4 ni f4v, la respuesta está vacía.

Las respuestas de f4m solo contienen archivos f4v si hay alguno presente en el conjunto de vídeos. Si no hay archivos f4v, estas respuestas solo contienen archivos mp4. Si no hay archivos f4v ni mp4, la respuesta está vacía.

Las tasas de bits que aparecen en las respuestas f4m/m3u8 corresponden a los valores de `catalog::TotalStreamBitRate` (convertidos a unidades adecuadas). Si no se define `catalog::TotalStreamBitRate` , se utiliza la suma de `catalog::VideoBitRate` y `catalog::AudioBitRate`.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::NonImgExpiration`.
