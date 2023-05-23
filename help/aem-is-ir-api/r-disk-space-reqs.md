---
description: Además del espacio necesario para instalar el software, el servicio de imágenes cuenta con los siguientes requisitos de espacio en disco
solution: Experience Manager
title: Requisitos y recomendaciones de espacio en disco
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# Requisitos y recomendaciones de espacio en disco{#disk-space-requirements-and-recommendations}

Además del espacio necesario para instalar el software, el servicio de imágenes tiene los siguientes requisitos de espacio en disco:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Descripción/ Ubicación predeterminada/ Definir con</b> </th> 
   <th class="entry"> <b>Cálculo/ Recomendación</b> </th> 
   <th class="entry"> <b>Comentarios</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Imágenes de origen, fuentes, perfiles ICC</b> </p> <p> <span class="filepath"> <span class="varname"> carpeta_instalación </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>Varía; consulte los comentarios siguientes. </p> </td> 
   <td> <p>Solo debe ser accesible para el servidor de imágenes; los servidores nunca modifican los datos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Caché de datos de respuesta HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> carpeta_instalación </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; se recomiendan al menos 2 GB. </p> </td> 
   <td> <p>Esta caché también almacena datos anidados/incrustados e imágenes de origen externo. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Caché de datos del catálogo de imágenes</b> </p> <p> <span class="filepath"> <span class="varname"> carpeta_instalación </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Permita que la carpeta del catálogo utilice 1,5 veces el espacio. </p> </td> 
   <td> <p>Se rellena cuando los catálogos se cargan inicialmente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Datos de registro</b> </p> <p> <span class="filepath"> <span class="varname"> carpeta_instalación </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100 Mbytes o más. </p> </td> 
   <td> <p>Varía según la configuración de registro y el uso del servidor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Archivos temporales del servidor de imágenes</b> </p> <p> <span class="filepath"> <span class="varname"> carpeta_instalación </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 MBytes es suficiente para la mayoría de los usos. </p> </td> 
   <td> <p>Datos de corta duración; pueden ser necesarios para imágenes de origen distintas de PTIFF y ciertos formatos de imagen de respuesta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisitos de espacio en disco para imágenes de origen {#section-317da75099ad480d9a461c7e706d4f1c}

Se recomienda convertir todas las imágenes de origen al formato de archivo TIFF piramidal (PTIFF) con la herramienta de línea de comandos (IC) Image Converter. Esta conversión garantiza el rendimiento óptimo del tiempo de ejecución del servicio de imágenes para todas las aplicaciones. Aunque el servidor de imágenes puede procesar todos los formatos de archivo de origen aceptados por IC, Dynamic Media no proporciona soporte para estos usos.

Cuando se utilizan archivos PTIFF, las siguientes reglas pueden ayudarle a determinar los requisitos de espacio.

*`total_space`* (bytes) = *`number_of_images`* x(2000 + *`avg_pixel_count`* x *`avg_num_components`* x *`p_factor`*)

* *`avg_pixel_count`* El tamaño de píxel promedio (anchura x altura) de todas las imágenes de origen originales. Por ejemplo, si las imágenes originales tienen normalmente unos píxeles de 2k x 2k, sería de 4M píxeles.
* *`avg_num_components`* Depende del tipo de imágenes. Para imágenes mayoritariamente RGB es 3, para imágenes mayoritariamente CMYK o RGBA es 4. Utilice 3,5 si la mitad de las imágenes son RGB y la otra mitad es RGBA.
* *`p_factor`* Depende del tipo de compresión y de la calidad establecida cuando las imágenes se convierten con IC.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Compresión PTIFF</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Sin comprimir </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0,75, según la imagen </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compresión de JPEG </p> </td> 
   <td> <p> 1 (típico de calidad JPEG 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esta aproximación no tiene en cuenta la sobrecarga del sistema de archivos. El espacio real en el disco puede ser considerablemente mayor.

**Ejemplo**

Una implementación del servicio de imágenes espera utilizar 30 000 imágenes heredadas de baja resolución, con un tamaño medio de 500 x 500 píxeles de RGB. Se espera añadir nuevos datos de calidad de impresión a un ritmo de 10.000 al año. El tamaño de imagen CMYK típico es de 4 k x 6 k bytes. Todos los datos tienen una compresión JPEG de alta calidad. La cantidad total de espacio en disco después de 3 años de uso se estima de la siguiente manera:

*`total_space`* = 30 000 x (2 k + 0,5 k x 0,5 k x 3 x 0,1) + 3 x 10 000 x (2 k + 4 k x 6 k x 4 x 0,1) = 2,2 G + 268 GB = aproximadamente 270 GB

Para garantizar la mejor calidad, se puede utilizar la compresión deflate (zip). Suponiendo un *`p_factor`* de 0,4, la cantidad total de espacio en disco necesario es aproximadamente 4 veces mayor. En este caso, un poco más de 1 TB.
