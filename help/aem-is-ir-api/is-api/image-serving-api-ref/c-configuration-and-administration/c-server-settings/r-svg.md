---
description: La configuración de esta sección solo debe considerarse si se requiere el procesamiento de SVG.
seo-description: La configuración de esta sección solo debe considerarse si se requiere el procesamiento de SVG.
seo-title: SVG
solution: Experience Manager
title: SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e69b150-46ac-480f-96db-afadccc40fe4
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 1%

---


# SVG{#svg}

La configuración de esta sección solo debe considerarse si se requiere el procesamiento de SVG.

## SV::SvgHeapSize - Tamaño de pila SVG {#section-59ab17681daa4be8b5d794713e1a504e}

El tamaño del montón de Java para el procesador SVG. El valor predeterminado es &quot;200m&quot; (200 Mbytes).

## PS::svgProvider.rootPaths - Carpetas raíz de datos SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Ubicación de los archivos de datos de origen SVG. Puede ser una o más rutas absolutas de archivos o rutas relativas a *[!DNL install_folder]*, separadas con punto y coma. Generalmente se configura en el mismo valor que `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Tamaño máximo del archivo SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Tamaño máximo del archivo de origen SVG en kBytes. El servidor devuelve un error cuando se intenta procesar un archivo SVG mayor que este límite. El valor predeterminado es 1024 kbytes.

## IS::SvgMAxRenderRgnPixels - Límite de tamaño de imagen de salida SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Limita el tamaño de las imágenes que SVGRender puede producir. Valor entero mayor que 0 en millones de píxeles. Se devuelve un error si una operación de procesamiento supera el límite de tamaño. El valor predeterminado es 4.

## PS::svgProvider.port: puerto de escucha de Platform Server {#section-f7e42a96c2dd4523b46f0557c239e659}

El puerto utilizado para SvgRender para obtener imágenes del servidor de Platform que se van a incrustar en representaciones SVG.

Importante Para el correcto funcionamiento del componente SVGRender, esta opción de configuración debe establecerse en el mismo valor que `TC::PsPort`.

## PS::svgProvider.fontRoot - Carpeta de archivos de fuente SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Especifica dónde encontrará SvgRender los archivos de fuente necesarios para procesar el texto SVG; normalmente una de las rutas especificadas en `IS::RootPaths`. El valor predeterminado es [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Puerto de comunicaciones SVG {#section-608687123aa644b7b58fe42385d71b79}

Configura el puerto en el que se comunican el servidor de imágenes y el componente SVGRender.

>[!NOTE]
>
>Para el correcto funcionamiento del componente SVGRender, se debe especificar el mismo número de puerto para `SVG::SVGRender.port` y `IS::SVGTcpPort`.

