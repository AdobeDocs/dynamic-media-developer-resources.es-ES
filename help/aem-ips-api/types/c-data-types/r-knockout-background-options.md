---
title: KnockoutBackgroundOptions
description: Enmascarar (eliminar) el fondo de las imágenes seleccionadas. Este tipo de datos le permite superponerlos en otras capas con una transparencia fuera de la imagen del sujeto. Un parámetro opcional que está desactivado de forma predeterminada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed8cf2e-5a09-43ff-9420-0d0d54059515
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# [!DNL KnockoutBackgroundOptions]{#knockoutbackgroundoptions}

Enmascarar (eliminar) el fondo de las imágenes seleccionadas. Este tipo de datos le permite superponerlos en otras capas con una transparencia fuera de la imagen del sujeto.

Este tipo de datos es opcional y está desactivado de forma predeterminada.

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## Parámetros {#section-3149b49ccb714e6eafa6655354816819}

>[!IMPORTANT]
>
>Si está configurando `KnockoutBackgroundOptions` en Adobe Experience Manager, use los siguientes parámetros:
>* `kbCorner`
>* `kbTolerance`
>* `kbFillMethod`
>
>Por ejemplo: `kbCorner=UpperLeft&kbTolerance=0.2&kbFillMethod=MatchPixel`

<table id="table_68131DE0A3C84908A43C6F7777F20973"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> esquina</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Selecciona la esquina con la que desea trabajar. <span class="codeph"> corner</span> acepta estos valores: 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> UpperLeft</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> BottomLeft</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> UpperRight</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> BottomRight</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolerancia</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Una configuración opcional que elimina el espacio en blanco de los bordes de la imagen en función de la transparencia. Acepta un rango de valores de 0,0 a 1,0. Especifique: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 para que coincida exactamente con los colores. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 para habilitar la mayoría de las diferencias de color. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Controlar la transparencia de píxeles en la ubicación especificada por la variable <span class="codeph"><span class="varname"> corner</span></span>. <span class="codeph"> fillMethod</span> acepta estos valores: </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>: convierte todos los píxeles de la esquina especificada en transparentes. </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>: Vuelve transparentes todos los píxeles coincidentes independientemente de la ubicación. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-3f9edfff321a4e4394f766298b9e284d}

```
<complexType name="KnockoutBackgroundOptions">
        <sequence>
            <!-- corner one of UpperLeft, BottomLeft, UpperRight, BottomRight -->
            <element name="corner" type="xsd:string" minOccurs="1"/>
            <!-- Tolerance real value between 0.0 and 1.0 -->
            <element name="tolerance" type="xsd:double" minOccurs="0"/>
            <!-- one of FloodFill or MatchPixel is required -->
            <element name="fillMethod" type="xsd:string" minOccurs="1"/>
        </sequence>
    </complexType>
```

## Utilizado por {#section-28c43baafe85434a9ee9e303ed10569a}

El tipo `KnockoutBackgroundOptions` lo utiliza:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [CargarTrabajo](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
