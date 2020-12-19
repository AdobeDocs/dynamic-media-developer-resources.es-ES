---
description: El catálogo de sesiones es el catálogo de materiales que proporciona atributos de sesión para la solicitud, así como un valor predeterminado de catId para todos los comandos src=, vignette= y icc=.
seo-description: El catálogo de sesiones es el catálogo de materiales que proporciona atributos de sesión para la solicitud, así como un valor predeterminado de catId para todos los comandos src=, vignette= y icc=.
seo-title: Catálogo de sesiones
solution: Experience Manager
title: Catálogo de sesiones
topic: Scene7 Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# Catálogo de sesiones{#session-catalog}

El catálogo de sesiones es el catálogo de materiales que proporciona atributos de sesión para la solicitud, así como un valor predeterminado de catId para todos los comandos src=, vignette= y icc=.

El catálogo de sesiones se especifica como el primer elemento de ruta de acceso de la ruta de solicitud HTTP (inmediatamente después del nombre del servidor). Si el primer elemento de ruta de acceso no coincide con el atributo::RootId de ningún catálogo, el catálogo predeterminado se utiliza como catálogo de sesiones.

El catálogo de sesiones proporciona los siguientes valores predeterminados de sesión:

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Atributo </p> </th> 
   <th class="entry"> <p>Notas </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> Ruta raíz para archivos de datos de material </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::VignettePath</span> </p> </td> 
   <td> <p> Ruta de acceso raíz para archivos de viñeta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::IccProfileRgb</span> </p> </td> 
   <td> <p> Espacio de color de trabajo predeterminado si una viñeta no incrusta un perfil ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::RootUrl</span> </p> </td> 
   <td> <p> URL raíz para rutas de archivos HTTP relativas en comandos <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Estado inicial de visualización/ocultado para objetos superpuestos </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Caducidad</span> </p> </td> 
   <td> <p> Valor de tiempo de vida de la imagen de respuesta para las memorias caché del servidor proxy y del explorador </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::MaxPix</span> </p> </td> 
   <td> <p> Ancho y altura máximos permitidos de la imagen de respuesta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> Valores predeterminados para <span class="codeph"> wid=</span> y <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Format</span> </p> </td> 
   <td> <p> Valor predeterminado para <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::JpegQuality</span> </p> </td> 
   <td> <p> Valor predeterminado para <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::TiffEncoding</span> </p> </td> 
   <td> <p> Tipo de compresión para la salida de imagen TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Enfocar</span> </p> </td> 
   <td> <p> Valor predeterminado para <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::OnFailSel</span> </p> </td> 
   <td> <p> Especifica el comportamiento cuando falla un comando <span class="codeph"> sel=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::OnFailObj</span> </p> </td> 
   <td> <p> Especifica el comportamiento cuando falla un comando <span class="codeph"> obj=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

