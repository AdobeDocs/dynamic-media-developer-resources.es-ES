---
description: Opciones que se utilizan al recortar automáticamente imágenes en función de la transparencia.
solution: Experience Manager
title: AutoTransparentCropOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 351f63a4-cc1b-4db9-93df-c21acd02e12a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 11%

---

# AutoTransparentCropOptions{#autotransparentcropoptions}

Opciones que se utilizan al recortar automáticamente imágenes en función de la transparencia.

Sintaxis

## Parámetros {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> tolerancia</span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Elimina el espacio en blanco de los bordes de la imagen en función de la transparencia. Usos: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 para que coincida exactamente con los colores. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 para activar la mayoría de las diferencias de color. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
