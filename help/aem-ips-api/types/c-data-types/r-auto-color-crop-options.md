---
description: Opciones para recortar automáticamente imágenes en función del color.
seo-description: Opciones para recortar automáticamente imágenes en función del color.
seo-title: AutoColorCropOptions
solution: Experience Manager
title: AutoColorCropOptions
topic: Scene7 Image Production System API
uuid: 632ae721-7b39-4cd1-a1c6-1a3554167a4e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AutoColorCropOptions{#autocolorcropoptions}

Opciones para recortar automáticamente imágenes en función del color.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> esquina</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Selección de la esquina de recorte automático. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolerancia</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:doble</span> </td> 
   <td colname="col3">Especificación de coincidencia de color. Usos: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 para coincidir exactamente con los colores. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 para activar la mayor cantidad de diferencias de color. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

