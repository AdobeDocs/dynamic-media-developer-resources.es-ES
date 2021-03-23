---
description: Los materiales decorativos incluyen prendas de vestir como aplicaciones, impresiones para camisetas y logotipos bordados o impresos, así como objetos planos no repetibles utilizados en aplicaciones interiores o exteriores, como alfombras de área, carteles, etc.
seo-description: Los materiales decorativos incluyen prendas de vestir como aplicaciones, impresiones para camisetas y logotipos bordados o impresos, así como objetos planos no repetibles utilizados en aplicaciones interiores o exteriores, como alfombras de área, carteles, etc.
seo-title: Decretos
solution: Experience Manager
title: Decretos
uuid: 6e64f382-f15f-4018-b00c-4fd21a4ebc8c
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---


# Decretos{#decals}

Los materiales decorativos incluyen prendas de vestir como aplicaciones, impresiones para camisetas y logotipos bordados o impresos, así como objetos planos no repetibles utilizados en aplicaciones interiores o exteriores, como alfombras de área, carteles, etc.

Un material se considera un calco si se especifica en un MSS calco. Una calcomanía suele ser una imagen RGBA, con el canal alfa que define la forma del calco.

Se puede aplicar un calco a cada objeto plano, de línea de flujo, de boceto, de plano o de pared (a menos que se haya establecido el indicador &quot;Sin textura&quot;). Las marcas se aplican al objeto alineando el `anchor=` del calco con el punto de origen del calco del objeto de la viñeta. La posición se puede ajustar con `pos=`.

Se representa una sombra paralela si el material de calcomanía define un grosor y el objeto de viñeta define un vector de luz.

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
   <td colname="col2"> <p>Imagen (normalmente con alfa); obligatorio. </p> </td> 
   <td colname="col3"> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Ancho, altura y grosor de la calcomanía (para sombra paralela). </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth  </span> x  <span class="codeph"> res  </span>,  <span class="varname"> imageHeight  </span> x  <span class="codeph"> res, 0  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolución de la textura (se ignora si se especifica size=). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo:Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Punto de alineación de la calcomanía. </p> </td> 
   <td colname="col3"> <p>Centro de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Posición relativa de calcomanía. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Decal opacity. </p> </td> 
   <td colname="col3"> <p>100 % </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> Sharp=  </span> </a> </td> 
   <td colname="col2"> <p>Enfoque. </p> </td> 
   <td colname="col3"> <p>0 (sin nitidez) </p> </td> 
  </tr> 
 </tbody> 
</table>

