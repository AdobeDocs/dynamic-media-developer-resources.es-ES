---
description: 'Dentro de este tipo, el campo pageReset es significativo para los tipos de recursos de imagen RenderSet y Catálogo '
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Conjuntos de imágenes
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 7%

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

Dentro de este tipo, el campo pageReset es significativo para los tipos de recursos de imagen RenderSet y Catálogo:

* Para `RenderSet`, `pageReset` indica el inicio de una nueva vista de procesamiento/grupo de muestras.

* Para Catálogo, `pageReset` indica el inicio de una nueva vista de página. Normalmente, hay 2 imágenes de página por vista de página, pero puede tener más o menos.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Controlador de recurso en la matriz de miembros del conjunto de imágenes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Restaura la página. <p>Se ignora la configuración y se fuerza el valor a true para <span class="codeph"> ImageSet</span> y <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>

