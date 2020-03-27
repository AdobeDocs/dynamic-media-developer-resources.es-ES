---
description: Un material se considera un borde de pared cuando se especifica en un MSS de borde de pared (introducido con sub=3.5).
seo-description: Un material se considera un borde de pared cuando se especifica en un MSS de borde de pared (introducido con sub=3.5).
seo-title: Bordes de pared
solution: Experience Manager
title: Bordes de pared
topic: Scene7 Image Serving - Image Rendering API
uuid: 40acd667-5e8b-4425-b44a-0681e608d189
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Bordes de pared{#wall-borders}

Un material se considera un borde de pared cuando se especifica en un MSS de borde de pared (introducido con sub=3.5).

Las imágenes de textura de borde de pared pueden incluir un canal alfa para definir la forma del borde. Los bordes de las paredes solo se pueden aplicar a objetos de pared.

<table id="table_906C5CC4CADF4024AA0E29544AF48080"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
   <th colname="col3" class="entry"> <p>Predeterminado </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>Imagen de textura repetible; requerido </p> </td> 
   <td colname="col3"> <p>Ninguno </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>Resolución de textura </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span></a> </p> </td> 
   <td colname="col2"> <p>Alineación de textura horizontal (se omite el valor y) </p> </td> 
   <td colname="col3"> <p>0 (borde izquierdo de la imagen) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span></a> </p> </td> 
   <td colname="col2"> <p>Enfoque </p> </td> 
   <td colname="col3"> <p>0 (sin enfoque) </p> </td> 
  </tr> 
 </tbody> 
</table>

