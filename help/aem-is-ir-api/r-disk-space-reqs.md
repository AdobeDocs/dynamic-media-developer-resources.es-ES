---
description: 'Además del espacio necesario para instalar el software, Image Serving tiene los siguientes requisitos de espacio en disco '
solution: Experience Manager
title: Requisitos y recomendaciones de espacio en disco
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# Requisitos y recomendaciones de espacio en disco{#disk-space-requirements-and-recommendations}

Además del espacio necesario para instalar el software, Image Serving tiene los siguientes requisitos de espacio en disco:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Descripción/ Ubicación predeterminada/ Configurar con</b> </th> 
   <th class="entry"> <b>Cálculo/Recomendación</b> </th> 
   <th class="entry"> <b>Comentarios</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Imágenes de origen, fuentes, perfiles ICC</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>Variables; consulte los comentarios a continuación. </p> </td> 
   <td> <p>Solo debe ser accesible para el servidor de imágenes; los servidores nunca modifican los datos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Caché de datos de respuesta HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2; se recomienda al menos 2 GB. </p> </td> 
   <td> <p>Esta caché también almacena datos anidados/incrustados e imágenes de origen externas. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Caché de datos del catálogo de imágenes</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>Permitir que la carpeta del catálogo utilice 1,5 veces el espacio. </p> </td> 
   <td> <p>Se rellena cuando los catálogos se cargan inicialmente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Datos de registro</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100 Mbytes o más. </p> </td> 
   <td> <p>Varía según la configuración de registro y el uso del servidor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Archivos temporales del servidor de imágenes</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 MBytes es suficiente para la mayoría de los usos. </p> </td> 
   <td> <p>Datos de corta duración; puede ser necesario para imágenes de origen distintas de PTIFF y ciertos formatos de imagen de respuesta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisitos de espacio en disco para imágenes de origen {#section-317da75099ad480d9a461c7e706d4f1c}

Se recomienda convertir todas las imágenes de origen al formato de archivo TIFF piramidal (PTIFF) mediante la herramienta de línea de comandos (IC) del conversor de imágenes. Esta conversión garantiza un rendimiento de tiempo de ejecución óptimo de Image Serving para todas las aplicaciones. Aunque Image Server puede procesar todos los formatos de archivo de origen aceptados por IC, Dynamic Media no proporciona soporte para estos usos.

Al utilizar archivos PTIFF, las siguientes reglas generales pueden ayudarle a determinar los requisitos de espacio.

*`total_space`* (bytes) =  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* El tamaño medio de píxeles (anchura x altura) de todas las imágenes de origen originales. Por ejemplo, si las imágenes originales suelen tener unos 2 k x 2 k píxeles, serían 4 M píxeles.
* *`avg_num_components`* Depende del tipo de imágenes. Para la mayoría de las imágenes RGB, es 3, para la mayoría de las imágenes CMYK o RGBA es 4. Utilice 3,5 si la mitad de las imágenes son RGB y la otra mitad es RGBA.
* *`p_factor`* Depende del tipo de compresión y del conjunto de calidad cuando las imágenes se convierten con IC.

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
   <td> <p>Compresión JPEG </p> </td> 
   <td> <p> 1 (típico de la calidad JPEG 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esta aproximación no tiene en cuenta la sobrecarga del sistema de archivos. El espacio real en disco puede ser sustancialmente mayor.

**Ejemplo**

Una implementación de servicio de imágenes espera utilizar 30 000 imágenes heredadas de baja resolución, con un tamaño promedio de 500 x 500 píxeles RGB. Se espera que se añadan nuevos datos de imagen de calidad de impresión a una tasa de 10.000 al año. El tamaño típico de la imagen CMYK será de 4 k x 6 kB bytes. Todos los datos serán JPEG comprimidos de alta calidad. La cantidad total de espacio en disco después de 3 años de uso se estima de la siguiente manera:

*`total_space`* = 30.000 x (2k + 0,5k x 0,5k x 3 x 0,1) + 3 x 10.000 x (2k + 4k x 6k x 4 x 0,1) = 2,2 G + 268 GB = aproximadamente 270 GB

Para garantizar la mejor calidad, se podría utilizar la compresión deflate (zip). Suponiendo un *`p_factor`* de 0,4, la cantidad total de espacio en disco requerido es aproximadamente 4 veces mayor. En este caso, algo más de 1 TB.
