---
description: Los archivos de datos de origen del servicio de imágenes incluyen archivos de imagen y máscara, fuentes y perfiles ICC.
seo-description: Los archivos de datos de origen del servicio de imágenes incluyen archivos de imagen y máscara, fuentes y perfiles ICC.
seo-title: Datos de origen
solution: Experience Manager
title: Datos de origen
topic: Scene7 Image Serving - Image Rendering API
uuid: d654eee7-ef2d-4546-93bb-72f80c38e018
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Datos de origen{#source-data}

Los archivos de datos de origen del servicio de imágenes incluyen archivos de imagen y máscara, fuentes y perfiles ICC.

El servidor de imágenes debe tener acceso a todos los archivos de datos de origen. El servicio de imágenes ofrece una serie de alternativas para especificar la ubicación de los archivos de datos:

` *`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Path|catálogo::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> ruta y nombre relativos del archivo de imagen especificados en una solicitud HTTP de servicio de imágenes</span> </p></td> 
 </tr> 
</table>

El servidor combina segmentos de ruta de acceso de derecha a izquierda hasta que se establece una ruta absoluta de archivo.

Todos los segmentos ` *`rootPath`*` pueden estar vacíos, relativos o absolutos.

` *``*` catalogPath es una ruta de acceso o nombre de archivo absoluta o relativa. ` *``*` requestPath debe ser una ruta/nombre de archivo relativo.

`Multiple IS::RootPath` los valores se pueden definir en ImageServerRegistry.xml (o a través de la interfaz de administración). Esto permite que los archivos de datos de origen se distribuyan en varios sistemas de archivos. El servidor de imágenes intentará rutas alternativas en el orden especificado hasta que se encuentre el archivo de datos.

Se pueden agregar nuevos archivos de datos de cualquier tipo en cualquier momento sin detener el servidor.
