---
description: Dentro de este tipo, el campo pageReset es significativo para los tipos de recursos de imagen RenderSet y Catalog
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 7%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

Dentro de este tipo, el campo pageReset es significativo para los tipos de recursos de imagen RenderSet y Catalog:

* Para `RenderSet`, `pageReset` indica el inicio de una nueva vista de procesamiento/grupo de muestras.

* Para el catálogo, `pageReset` indica el inicio de una nueva vista de página. Normalmente, hay dos imágenes de página por vista de página, pero puede tener más o menos.

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
   <td colname="col3"> Controlador de recursos en la matriz de miembros del conjunto de imágenes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Restablece la página. <p>La configuración se ignora y el valor se fuerza en true para <span class="codeph"> ImageSet</span> y <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>
