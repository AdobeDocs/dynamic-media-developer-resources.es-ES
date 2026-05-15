---
description: Los archivos de datos de origen del servicio de imágenes incluyen archivos de imagen y máscara, fuentes y perfiles ICC.
solution: Experience Manager
title: Datos de Source
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
TQID: 'https://experienceleague.adobe.com/36EvEOjHZ8ik-gps-vaap5PhFCf5rwV9ecfkKHZcIhk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Datos de Source{#source-data}

Los archivos de datos de origen del servicio de imágenes incluyen archivos de imagen y máscara, fuentes y perfiles ICC.

El servidor de imágenes debe poder acceder a todos los archivos de datos de origen. El servicio de imágenes proporciona una serie de alternativas para especificar la ubicación de los archivos de datos:

`*`carpeta_instalación`*/ *`rutaDeAccesoRaíz`*/ *`rutaDeAccesoDeArchivo`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> ES::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rutaDeAccesoDeArchivo </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rutaDeAccesoDeCatálogo</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> ruta de acceso y nombre de archivo de imagen relativo especificados en una solicitud HTTP del servicio de imágenes</span> </p></td> 
 </tr> 
</table>

El servidor combina los segmentos de ruta de derecha a izquierda hasta que se establece una ruta de archivo absoluta.

Todos los `*`segmentos rootPath`*` pueden ser segmentos de ruta de acceso vacíos, relativos o absolutos.

`*`catalogPath`*` es una ruta de acceso o un nombre de archivo absoluto o relativo. `*`requestPath`*` debe ser una ruta/nombre de archivo relativo.

Los valores `Multiple IS::RootPath` se pueden definir en ImageServerRegistry.xml (o a través de la interfaz de administración). Esto permite distribuir los archivos de datos de origen entre varios sistemas de archivos. El servidor de imágenes intenta encontrar rutas alternativas en el orden especificado hasta encontrar el archivo de datos.

Se pueden agregar nuevos archivos de datos de cualquier tipo en cualquier momento sin detener el servidor.
