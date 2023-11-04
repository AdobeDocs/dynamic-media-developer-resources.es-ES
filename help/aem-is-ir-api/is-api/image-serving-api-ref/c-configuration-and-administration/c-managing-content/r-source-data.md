---
description: Los archivos de datos de origen del servicio de imágenes incluyen archivos de imagen y máscara, fuentes y perfiles ICC.
solution: Experience Manager
title: Datos de origen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Datos de origen{#source-data}

Los archivos de datos de origen del servicio de imágenes incluyen archivos de imagen y máscara, fuentes y perfiles ICC.

El servidor de imágenes debe poder acceder a todos los archivos de datos de origen. El servicio de imágenes proporciona una serie de alternativas para especificar la ubicación de los archivos de datos:

`*`carpeta_instalación`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> ruta y nombre relativos al archivo de imagen especificados en una solicitud HTTP del servicio de imágenes</span> </p></td> 
 </tr> 
</table>

El servidor combina los segmentos de ruta de derecha a izquierda hasta que se establece una ruta de archivo absoluta.

Todo `*`rootPath`*` los segmentos pueden ser segmentos de ruta vacíos, relativos o absolutos.

`*`catalogPath`*` es una ruta de acceso o un nombre de archivo absoluto o relativo. `*`requestPath`*` debe ser una ruta/nombre de archivo relativo.

`Multiple IS::RootPath` Los valores de se pueden definir en ImageServerRegistry.xml (o a través de la interfaz de administración). Esto permite distribuir los archivos de datos de origen entre varios sistemas de archivos. El servidor de imágenes intenta encontrar rutas alternativas en el orden especificado hasta encontrar el archivo de datos.

Se pueden agregar nuevos archivos de datos de cualquier tipo en cualquier momento sin detener el servidor.
