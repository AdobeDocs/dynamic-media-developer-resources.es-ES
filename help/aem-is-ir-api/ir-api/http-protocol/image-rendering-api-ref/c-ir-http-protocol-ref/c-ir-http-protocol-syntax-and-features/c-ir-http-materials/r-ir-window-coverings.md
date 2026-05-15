---
title: Revestimientos para ventanas
description: Los materiales de revestimiento de ventanas incluyen tanto revestimientos de ventanas suaves (cortinas, vallas, cortinas de café), como revestimientos de ventanas duras (persianas y persianas).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
TQID: 'https://experienceleague.adobe.com/PuQ48u-44qc1KjyuX8HYi5FvCI3UNxsNm-HULPoPhgU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 3%

---

# Revestimientos para ventanas{#window-coverings}

Los materiales de revestimiento de ventanas incluyen tanto revestimientos de ventanas suaves (cortinas, vallas, cortinas de café), como revestimientos de ventanas duras (persianas y persianas).

Los materiales de cobertura de ventana especifican un *archivo de estilo de cobertura de ventana* (extensión de archivo [!DNL .vnw]), un archivo de datos especial similar a una viñeta que contiene datos de máscara, iluminación, diseño y textura que definen la cobertura de ventana.

[!DNL vnw] archivos no incluyen el color y la textura (tejido) para el recubrimiento de la ventana. Esta información se especifica por separado, de forma similar a las texturas repetibles.

Los materiales de recubrimiento de ventanas sólo se pueden aplicar a objetos de marco de recubrimiento de ventanas, que son objetos superpuestos.

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
   <th colname="col3" class="entry"> <p>Predeterminado </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Archivo de estilo de cobertura de ventana; obligatorio. </p> </td> 
   <td colname="col3"> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Archivo de imagen de textura (segundo valor para <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolución de textura. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repetición= </span> </a> </p> </td> 
   <td colname="col2"> <p>Modo de repetición. </p> </td> 
   <td colname="col3"> <p>0 (repetición recta) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>Color sólido (o colorea la textura). </p> </td> 
   <td colname="col3"> <p>128 (gris neutro) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Enfoque. </p> </td> 
   <td colname="col3"> <p>0 (sin enfoque) </p> </td> 
  </tr> 
 </tbody> 
</table>
