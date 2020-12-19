---
description: Parámetro común a todos los visores.
seo-description: Parámetro común a todos los visores.
seo-title: asset
solution: Experience Manager
title: recurso
topic: Dynamic media
uuid: 6a72257f-d204-4258-b6f8-de6f7b00fd54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 2%

---


# asset{#asset}

Parámetro común a todos los visores.

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId  </span> </span> </p> </td> 
   <td colname="col2"> <p> ID de recurso del vídeo único o del conjunto de vídeos adaptable. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esta propiedad es obligatoria, a menos que se utilice el parámetro `video`. Consulte [Compatibilidad con video externo](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) en Video o [Compatibilidad con video externo](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) en Video360.

o

` asset= *`imagen`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una sola imagen o un conjunto de carrusel. Aplique codificación HTTP de doble a cualquier carácter no seguro que exista en el nombre de la imagen o en el nombre del conjunto de carrusel. </p> </td> 
  </tr> 
 </tbody> 
</table>

o

` asset= *``* | *``* | *``* | *``* [%3F *`imageimageListimageListWithModiersmultiDimensionalSpinSetmodifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una sola imagen. Aplique codificación HTTP de doble a cualquier carácter no seguro que exista en el nombre de la imagen. </p> <p>O bien, especifica una referencia a un conjunto de imágenes. El visor recupera conjuntos de imágenes del servidor mediante la solicitud <span class="codeph"> req=set IS </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica un conjunto de imágenes explícito, que consiste en una secuencia ordenada de elementos o marcos, separados por comas. </p> <p> <p>Nota:  Esta función es compatible con Adobe Scene7 Publishing System; no se admite en Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica un conjunto de imágenes explícito en el que cada marco tiene sus propios modificadores de servicio de imágenes. En este caso, la lista de marcos se envuelve entre paréntesis. Asegúrese de aplicar codificación HTTP de doble a cualquier coma que esté presente en el modificador de servicio de imágenes específico del marco. </p> <p> <p>Nota:  Esta función es compatible con Adobe Scene7 Publishing System; no se admite en Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet  </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica un conjunto de giros multidimensional explícito con la siguiente sintaxis: </p> <p> <span class="codeph"> ((  <span class="varname"> horizontalSpinSet  </span>)[,(  <span class="varname"> horizontalSpinSet  </span>)])  </span> </p> <p> donde <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> es una lista de marcos separada por comas para un eje horizontal determinado. Todo <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> debe tener el mismo número de fotogramas. </p> <p> <p>Nota:  Esta función es compatible con Adobe Scene7 Publishing System; no se admite en Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modificadores  </span> </span> </p> </td> 
   <td colname="col2"> <p> Comandos de servicio de imágenes; Los separadores <span class="codeph"> &amp; </span> y <span class="codeph"> = </span> deben estar codificados en HTTP como <span class="codeph"> %26 </span> y <span class="codeph"> %3D </span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

o

` asset=( *``* | ( *``*; *``* | *``*; *``* | *``*; *``*); *``*;( *``*; *``* | *``*; *``* | *``*; *``*); *``*;] [%3F *`mediaSetvideoswatchIdimageswatchIdsetIdswatchIdIDvideoswatchIdimageswatchIdsetIdswatchIdIDmodifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una referencia a un conjunto de medios. El visor recupera conjuntos de medios del servidor mediante la solicitud IS req=set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> video  </span> </span> </p> </td> 
   <td colname="col2"> <p> Un solo vídeo o conjunto de vídeos adaptable. </p> <p> <p>Nota:  Esta función es compatible con Adobe Scene7 Publishing System; no se admite en Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image  </span> </span> </p> </td> 
   <td colname="col2"> <p> Imagen única. </p> <p> <p>Nota:  Esta función es compatible con Adobe Scene7 Publishing System; no se admite en Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId  </span> </span> </p> </td> 
   <td colname="col2"> <p> Conjunto de muestras. </p> <p> <p>Nota:  Esta función es compatible con Adobe Scene7 Publishing System; no se admite en Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId  </span> </span> </p> </td> 
   <td colname="col2"> <p>Imagen de muestra. </p> <p> <p>Nota:  Esta función es compatible con Adobe Scene7 Publishing System; no se admite en Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID  </span> </span> </p> </td> 
   <td colname="col2"> <p> El identificador de tipo de elemento de conjunto de medios puede ser uno de los siguientes: </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image  </span> </p> <p>Para una sola imagen. </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset  </span> </p> <p>Para conjunto de muestras anidadas. </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> girar  </span> </p> <p>Para conjunto de giros. </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> video  </span> </p> <p>Para un solo vídeo. </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set  </span> </p> <p>Para conjuntos de vídeos adaptables. </p> </li> 
     </ul> </p> <p> <p>Nota:  Esta función es compatible con Adobe Scene7 Publishing System; no se admite en Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modificadores  </span> </span> </p> </td> 
   <td colname="col2"> <p> Comandos de servicio de imágenes; Los separadores <span class="codeph"> &amp; </span> y <span class="codeph"> = </span> deben estar codificados en HTTP como <span class="codeph"> %26 </span> y <span class="codeph"> %3D </span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este visor no admite las imágenes que usan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario).

## Propiedades {#section-10ee45d637134e0fbcd943c62578cb78}

Obligatorio.

## Predeterminado {#section-d411e450028c460392cb8508f8ccc5d9}

Ninguno.

## Ejemplos {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Referencia de un solo recurso:

```
asset=Scene7SharedAssets/Backpack_B
```

o

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

o

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

o

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

o

```
asset=Viewers/space_station_360-AVS
```

Referencia única a un conjunto de imágenes definido en un catálogo:

```
asset=Viewers/Pluralist
```

Conjunto de imágenes explícito:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

Conjunto de imágenes explícitas con modificadores de servicio de imágenes específicos de marco:

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

Una sola referencia a un conjunto de giros definido en un catálogo:

```
asset=Scene7SharedAssets/SpinSet-Sample
```

Conjunto de giros explícito:

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

Conjunto de giros multidimensional explícito:

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

Una sola referencia de conjunto de medios mixtos:

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

Conjunto de medios mixtos explícito:

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

Modificador de enfoque añadido a todas las imágenes del conjunto:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```

