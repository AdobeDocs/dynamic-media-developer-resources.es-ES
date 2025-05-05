---
title: asset
description: Parámetro común a todos los visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: edcd18b6-5292-44da-80be-b7f75ee4c48e
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---

# asset{#asset}

Parámetro común a todos los visualizadores.

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId </span> </span> </p> </td> 
   <td colname="col2"> <p> ID de recurso de un solo vídeo o conjunto de vídeos adaptable. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esta propiedad es obligatoria, a menos que se use el parámetro `video`. Consulte [Compatibilidad con vídeo externo](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) en Vídeo o [Compatibilidad con vídeo externo](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) en Video360.

o

` asset= *`imagen`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imagen </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una sola imagen o un conjunto de carrusel. Aplique una codificación HTTP doble a cualquier carácter no seguro que exista en el nombre de la imagen o en el nombre del conjunto de carrusel. </p> </td> 
  </tr> 
 </tbody> 
</table>

o

` asset= *`image`* | *`imageList`* | *`imageListWithModifiers`* | *`multiDimensionalSpinSet`* [%3F *`modifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imagen </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una sola imagen. Aplique una codificación HTTP doble a cualquier carácter no seguro que exista en el nombre de la imagen. </p> <p>O bien, especifica una referencia a un conjunto de imágenes. El visor recupera conjuntos de imágenes del servidor mediante la solicitud <span class="codeph"> req=set IS </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica un conjunto de imágenes explícito formado por una secuencia ordenada de elementos o fotogramas separados por comas. </p> <p> <p>Nota: Esta función es compatible con Adobe Dynamic Media Classic, no con Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica un conjunto de imágenes explícito en el que cada fotograma tiene sus propios modificadores de servicio de imágenes. En este caso, la lista de marcos se coloca entre paréntesis. Asegúrese de aplicar la codificación HTTP doble a cualquier coma que esté presente en el modificador del servicio de imágenes específico del fotograma. </p> <p> <p>Nota: Esta función es compatible con Adobe Dynamic Media Classic, no con Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica un conjunto de giros multidimensional explícito utilizando la siguiente sintaxis: </p> <p> <span class="codeph"> (( <span class="varname"> horizontalSpinSet </span>) [,( <span class="varname"> horizontalSpinSet </span>)]) </span> </p> <p> donde <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> es una lista de fotogramas separados por comas para un eje horizontal determinado. Todos los <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> deben tener el mismo número de fotogramas. </p> <p> <p>Nota: Esta función es compatible con Adobe Dynamic Media Classic, no con Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modificadores </span> </span> </p> </td> 
   <td colname="col2"> <p> Los comandos del servicio de imágenes; los separadores <span class="codeph"> y </span> y <span class="codeph"> = </span> deben estar codificados en HTTP como <span class="codeph"> %26 </span> y <span class="codeph"> %3D </span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

o

` asset=( *`mediaSet`* | ( *`video`*; *`swatchId`* | *`image`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;( *`video`*; *`swatchId`* | *`image`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;] [%3F *`modifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una referencia a un conjunto de medios. El visor recupera conjuntos de medios del servidor mediante la solicitud req=set IS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> vídeo </span> </span> </p> </td> 
   <td colname="col2"> <p> Un solo vídeo o conjunto de vídeos adaptable. </p> <p> <p>Nota: Esta función es compatible con Adobe Dynamic Media Classic, no con Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imagen </span> </span> </p> </td> 
   <td colname="col2"> <p> Imagen única. </p> <p> <p>Nota: Esta función es compatible con Adobe Dynamic Media Classic, no con Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId </span> </span> </p> </td> 
   <td colname="col2"> <p> Juego de muestras. </p> <p> <p>Nota: Esta función es compatible con Adobe Dynamic Media Classic, no con Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId </span> </span> </p> </td> 
   <td colname="col2"> <p>Imagen de muestra. </p> <p> <p>Nota: Esta función es compatible con Adobe Dynamic Media Classic, no con Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID </span> </span> </p> </td> 
   <td colname="col2"> <p> El identificador del tipo de elemento del conjunto de medios puede ser uno de los siguientes: </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image </span> </p> <p>Para una sola imagen. </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset </span> </p> <p>Para conjuntos de muestras anidados. </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> giro </span> </p> <p>Para el conjunto de giros. </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> vídeo </span> </p> <p>Para un solo vídeo. </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set </span> </p> <p>Para Conjuntos De Vídeos Adaptables. </p> </li> 
     </ul> </p> <p> <p>Nota: Esta función es compatible con Adobe Dynamic Media Classic, no con Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modificadores </span> </span> </p> </td> 
   <td colname="col2"> <p> Los comandos del servicio de imágenes; los separadores <span class="codeph"> y </span> y <span class="codeph"> = </span> deben estar codificados en HTTP como <span class="codeph"> %26 </span> y <span class="codeph"> %3D </span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content) no son compatibles con este visor.

## Propiedades {#section-10ee45d637134e0fbcd943c62578cb78}

Obligatorio.

## Predeterminado {#section-d411e450028c460392cb8508f8ccc5d9}

Ninguno.

## Ejemplos {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Referencia de recurso único:

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

Conjunto de imágenes explícito con modificadores de servicio de imágenes específicos de marcos:

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

Referencia única a un conjunto de giros definido en un catálogo:

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

Referencia de conjunto de medios mixtos únicos:

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
