---
title: Catálogo de sesiones
description: El catálogo de sesiones es el catálogo de materiales que proporciona atributos de sesión para la solicitud y un valor catId predeterminado para todos los comandos src=, vignette= e icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Catálogo de sesiones{#session-catalog}

El catálogo de sesiones es el catálogo de materiales que proporciona atributos de sesión para la solicitud y un valor catId predeterminado para todos `src=`, `vignette=`, y `icc=` comandos.

El catálogo de sesiones se especifica como el primer elemento de ruta de la ruta de solicitud HTTP (inmediatamente después del nombre del servidor). Si el primer elemento de ruta no coincide con attribute::RootId de ningún catálogo, el catálogo predeterminado se utiliza como catálogo de sesión.

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
   <td> <p> <span class="codeph"> attribute::RutaDeViñeta</span> </p> </td> 
   <td> <p> Ruta raíz para archivos de viñeta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::IccProfileRgb</span> </p> </td> 
   <td> <p> Espacio de color de trabajo predeterminado si una viñeta no incrusta un perfil ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> URL raíz para rutas de archivo HTTP relativas en <span class="codeph"> src=</span> comandos </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Estado inicial de mostrar/ocultar para objetos superpuestos </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Caducidad</span> </p> </td> 
   <td> <p> Valor de tiempo de vida de la imagen de respuesta para las memorias caché del servidor proxy y del explorador </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> Anchura y altura máximas para la imagen de respuesta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> Valores predeterminados para <span class="codeph"> wid=</span> y <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Formato</span> </p> </td> 
   <td> <p> Valor predeterminado para <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
   <td> <p> Valor predeterminado para <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::TiffEncoding</span> </p> </td> 
   <td> <p> Tipo de compresión para la salida de imagen del TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Enfoque</span> </p> </td> 
   <td> <p> Valor predeterminado para <span class="codeph"> enfocar=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailSel</span> </p> </td> 
   <td> <p> Especifica el comportamiento cuando <span class="codeph"> sel=</span> el comando falla </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> Especifica el comportamiento cuando una <span class="codeph"> obj=</span> el comando falla </p> </td> 
  </tr> 
 </tbody> 
</table>
