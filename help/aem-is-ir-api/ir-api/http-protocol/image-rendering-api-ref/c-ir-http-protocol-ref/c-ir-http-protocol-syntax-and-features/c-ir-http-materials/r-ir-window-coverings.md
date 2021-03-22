---
description: Los materiales de revestimiento de las ventanas incluyen revestimientos de ventanas suaves (cortinas, cortinas de café), así como revestimientos de ventanas duras (tonos y persianas).
seo-description: Los materiales de revestimiento de las ventanas incluyen revestimientos de ventanas suaves (cortinas, cortinas de café), así como revestimientos de ventanas duras (tonos y persianas).
seo-title: Cubiertas de ventana
solution: Experience Manager
title: Cubiertas de ventana
uuid: 3d74466a-b7c3-43b0-9b0b-f8bb809e2773
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 3%

---


# Coberturas de ventana{#window-coverings}

Los materiales de revestimiento de las ventanas incluyen revestimientos de ventanas suaves (cortinas, cortinas de café), así como revestimientos de ventanas duras (tonos y persianas).

Los materiales de cubierta de ventanas especifican un *archivo de estilo de cubierta de ventana* (extensión de archivo [!DNL .vnw]), un archivo de datos especial similar a una viñeta, que contiene datos de máscara, iluminación, diseño y textura que definen el encubrimiento de ventanas.

[!DNL vnw] los archivos no incluyen el color y la textura (tela) para la cubierta de la ventana. Esta información se especifica por separado, de forma similar a las texturas repetibles.

Los materiales de recubrimiento de ventanas solo se pueden aplicar a los objetos de recubrimiento de ventanas, que son objetos superpuestos.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Ventana que cubre el archivo de estilo; obligatorio. </p> </td> 
   <td colname="col3"> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Archivo de imagen de textura (segundo valor para <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolución de textura. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo:Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repetir=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Modo de repetición. </p> </td> 
   <td colname="col3"> <p>0 (repetición recta) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Color sólido (o colorea textura). </p> </td> 
   <td colname="col3"> <p>128 (gris neutro) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> Sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Enfoque. </p> </td> 
   <td colname="col3"> <p>0 (sin nitidez) </p> </td> 
  </tr> 
 </tbody> 
</table>

