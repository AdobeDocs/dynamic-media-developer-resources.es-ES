---
title: SVG
description: La configuración de esta sección debe tenerse en cuenta solo si se requiere el procesamiento por SVG.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 2%

---

# SVG{#svg}

La configuración de esta sección debe tenerse en cuenta solo si se requiere el procesamiento por SVG.

## SV::SvgHeapSize - Tamaño de pila de SVG {#section-59ab17681daa4be8b5d794713e1a504e}

El tamaño de la pila Java para el procesador SVG. El valor predeterminado es 200 m (200 MB).

## PS::svgProvider.rootPaths: carpetas raíz de datos de SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Ubicación de los archivos de datos de origen de SVG. Puede ser una o más rutas de acceso de archivo absolutas o rutas de acceso relativas a *[!DNL install_folder]*, separadas por punto y coma. Normalmente se establece con el mismo valor que `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit: tamaño máximo de archivo de SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Tamaño máximo del archivo de origen SVG en kBytes. El servidor devuelve un error cuando se intenta procesar un archivo SVG que supera este límite. El valor predeterminado es 1024 kbytes.

## IS::SvgMAxRenderRgnPixels: límite de tamaño de imagen de salida de SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Limita el tamaño de las imágenes que SVGRender puede producir. Valor entero mayor que 0 en millones de píxeles. Se devuelve un error si una operación de procesamiento supera el límite de tamaño. El valor predeterminado es 4.

## PS::svgProvider.port - Puerto de escucha [!DNL Platform Server] {#section-f7e42a96c2dd4523b46f0557c239e659}

Puerto utilizado por SvgRender para obtener imágenes de [!DNL Platform Server] que se van a incrustar en las representaciones de SVG.

Importante: Para que el componente SVGRender funcione correctamente, esta opción de configuración debe establecerse con el mismo valor que `TC::PsPort`.

## PS::svgProvider.fontRoot: carpeta de archivos de fuentes de SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Especifica dónde encuentra SvgRender los archivos de fuente necesarios para representar texto de SVG; normalmente, una de las rutas especificadas en `IS::RootPaths`. El valor predeterminado es [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort: puerto de comunicaciones de SVG {#section-608687123aa644b7b58fe42385d71b79}

Configura el puerto en el que se comunican el servidor de imágenes y el componente SVGRender.

>[!NOTE]
>
>Para el correcto funcionamiento del componente SVGRender, se debe especificar el mismo número de puerto para `SVG::SVGRender.port` y `IS::SVGTcpPort`.
