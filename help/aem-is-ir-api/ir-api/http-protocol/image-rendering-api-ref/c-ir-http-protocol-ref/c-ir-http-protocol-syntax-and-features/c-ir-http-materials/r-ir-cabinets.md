---
description: Los materiales de gabinetes especifican un archivo de estilo archivador (extensión de archivo .vnc), un archivo de datos especial que contiene representaciones fotográficas de los archivadores, junto con definiciones de diseño paramétrico y otra información necesaria para procesar frontales de archivador.
seo-description: Los materiales de gabinetes especifican un archivo de estilo archivador (extensión de archivo .vnc), un archivo de datos especial que contiene representaciones fotográficas de los archivadores, junto con definiciones de diseño paramétrico y otra información necesaria para procesar frontales de archivador.
seo-title: Armarios
solution: Experience Manager
title: Armarios
topic: Scene7 Image Serving - Image Rendering API
uuid: d515c613-07c5-49ef-ad6e-568a1f6c1335
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Armarios{#cabinets}

Los materiales de gabinetes especifican un archivo de estilo archivador (extensión de archivo .vnc), un archivo de datos especial que contiene representaciones fotográficas de los archivadores, junto con definiciones de diseño paramétrico y otra información necesaria para procesar frontales de archivador.

[!DNL vnc] los archivos pueden incluir una textura de grano de madera repetible o la textura puede proporcionarse externamente mediante un segundo argumento de `src=`. Ciertos [!DNL vnc] archivos permiten colorear o texturar áreas seleccionadas de los frontales del archivador (generalmente se utilizan para laminar estilos de archivador).

Los materiales de gabinete sólo se pueden aplicar a objetos de gabinete.

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
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
   <td colname="col2"> <p>Archivo de estilo de archivador; requerido. </p> </td> 
   <td colname="col3"> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>Archivo de imagen de textura opcional (segundo valor para <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>Resolución de textura opcional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span></a> </p> </td> 
   <td colname="col2"> <p>Coloriza el gabinete y/o la textura. </p> </td> 
   <td colname="col3"> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span></a> </p> </td> 
   <td colname="col2"> <p>Enfoque. </p> </td> 
   <td colname="col3"> <p>0 (sin enfoque) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> flag= </span></a> </p> </td> 
   <td colname="col2"> <p>Indicadores de procesamiento especiales. </p> </td> 
   <td colname="col3"> <p>0 (sin indicadores) </p> </td> 
  </tr> 
 </tbody> 
</table>

