---
description: Los materiales decorativos incluyen prendas de vestir, como aparatos, estampas para camisetas y logotipos bordados o impresos, así como objetos planos y no repetibles utilizados en aplicaciones interiores o exteriores, como alfombras de área, carteles, etc.
seo-description: Los materiales decorativos incluyen prendas de vestir, como aparatos, estampas para camisetas y logotipos bordados o impresos, así como objetos planos y no repetibles utilizados en aplicaciones interiores o exteriores, como alfombras de área, carteles, etc.
seo-title: Llamadas
solution: Experience Manager
title: Llamadas
topic: Scene7 Image Serving - Image Rendering API
uuid: 6e64f382-f15f-4018-b00c-4fd21a4ebc8c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Declaciones{#decals}

Los materiales decorativos incluyen prendas de vestir, como aparatos, estampas para camisetas y logotipos bordados o impresos, así como objetos planos y no repetibles utilizados en aplicaciones interiores o exteriores, como alfombras de área, carteles, etc.

Un material se considera una calcomanía si se especifica en un MSS de calcomanía. Una calcomanía suele ser una imagen RGBA, con el canal alfa que define la forma de la calcomanía.

Se puede aplicar una calcomanía a cada objeto plano, de línea de flujo, de esbozo, de plano o de pared (a menos que se haya definido el indicador &#39;Sin textura&#39;). Las marcas se aplican al objeto alineando el `anchor=` de la calcomanía con el punto de origen de calcomanía del objeto de viñeta. La posición se puede ajustar con `pos=`.

Se representa una sombra paralela si el material de calado define un grosor y el objeto de viñeta define un vector de luz.

<table id="table_3F119BC9B7654FD092826A34F5827268"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
   <th colname="col3" class="entry"> <p>Predeterminado </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Imagen (normalmente con alfa); requerido. </p> </td> 
   <td colname="col3"> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Ancho, altura y grosor de la capa de calado (para sombra paralela). </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth  </span> x  <span class="codeph"> res  </span>,  <span class="varname"> imageHeight  </span> x  <span class="codeph"> res, 0  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolución de textura (se omite si se especifica size=). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Punto de alineación de cierre. </p> </td> 
   <td colname="col3"> <p>Centro de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Posición relativa de cierre. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Opacidad de cierre. </p> </td> 
   <td colname="col3"> <p>100 % </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </td> 
   <td colname="col2"> <p>Enfoque. </p> </td> 
   <td colname="col3"> <p>0 (sin enfoque) </p> </td> 
  </tr> 
 </tbody> 
</table>

