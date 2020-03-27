---
description: Las texturas repetibles incluyen materiales interiores y exteriores, como telas (tanto de vestimenta como de tapicería), revestimientos de suelo de pared a pared, papeles pintados, materiales de contrapeso, texturas de granos de madera, materiales de tejado y revestimiento, y cualquier otra textura genérica.
seo-description: Las texturas repetibles incluyen materiales interiores y exteriores, como telas (tanto de vestimenta como de tapicería), revestimientos de suelo de pared a pared, papeles pintados, materiales de contrapeso, texturas de granos de madera, materiales de tejado y revestimiento, y cualquier otra textura genérica.
seo-title: Texturas repetibles
solution: Experience Manager
title: Texturas repetibles
topic: Scene7 Image Serving - Image Rendering API
uuid: 11a55d9f-a1d7-490e-af0e-9bf2c3a35501
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Texturas repetibles{#repeatable-textures}

Las texturas repetibles incluyen materiales interiores y exteriores, como telas (tanto de vestimenta como de tapicería), revestimientos de suelo de pared a pared, papeles pintados, materiales de contrapeso, texturas de granos de madera, materiales de tejado y revestimiento, y cualquier otra textura genérica.

Las texturas repetibles se pueden aplicar a objetos planos, de línea de flores, de boceto, planos, paredes y armarios. Cuando se aplica a un objeto no texturable, el objeto se pinta con `color=` (o `bgc=` si no `color=` se especifica).

Un material se considera una textura si incluye un `src=` atributo que especifica una imagen y si se produce en un MSS que no sea el borde de la descomposición o de la pared.

Cuando se procesa, la textura se alinea con el objeto haciendo coincidir el `anchor=` punto del material de textura con el punto de origen de textura del objeto (como se crea en la viñeta).

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
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
   <td colname="col3"> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>Resolución de textura </p> </td> 
   <td colname="col3"> <span class="codeph"> attribute::Resolution </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span></a> </p> </td> 
   <td colname="col2"> <p>Punto de alineación de textura </p> </td> 
   <td colname="col3"> <p>Esquina superior izquierda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span></a> </p> </td> 
   <td colname="col2"> <p>Modo de repetición </p> </td> 
   <td colname="col3"> <p>0 (repetición directa). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span></a> </p> </td> 
   <td colname="col2"> <p>Enfoque </p> </td> 
   <td colname="col3"> <p>0 (sin enfoque). </p> </td> 
  </tr> 
 </tbody> 
</table>

Además de estos atributos básicos, las texturas repetibles admiten los siguientes atributos de propósito especial para aplicaciones avanzadas:

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
   <th colname="col3" class="entry"> <p>Predeterminado </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout= </span></a> </p> </td> 
   <td colname="col2"> <p>Color y grosor del grupo; útil para materiales de cerámica o de piedra </p> </td> 
   <td colname="col3"> <p>El grupo ya está presente en la imagen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align= </span></a> </p> </td> 
   <td colname="col2"> <p>Modo de alineación (entre objetos); utilizado para aplicaciones de tapicería </p> </td> 
   <td colname="col3"> <p>Coincidencia de centro </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>Ángulo de rotación de la textura; no admitidos por objetos de pared </p> </td> 
   <td colname="col3"> <p>0 (sin rotación) </p> </td> 
  </tr> 
 </tbody> 
</table>

