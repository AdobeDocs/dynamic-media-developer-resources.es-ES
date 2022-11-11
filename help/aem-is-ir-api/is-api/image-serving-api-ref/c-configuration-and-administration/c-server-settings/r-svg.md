---
description: La configuración de esta sección solo debe considerarse si se requiere una renderización del SVG.
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# SVG{#svg}

La configuración de esta sección solo debe considerarse si se requiere una renderización del SVG.

## SV::SvgHeapSize - Tamaño de pila del SVG {#section-59ab17681daa4be8b5d794713e1a504e}

El tamaño de pila de Java para el procesador del SVG. El valor predeterminado es &quot;200 m&quot; (200 Mbytes).

## PS::svgProvider.rootPaths - Carpetas raíz de datos del SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

La ubicación de los archivos de datos de origen del SVG. Puede ser una o más rutas absolutas de archivos o rutas relativas a *[!DNL install_folder]*, separada con punto y coma. Generalmente se establece en el mismo valor que `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Tamaño máximo del archivo SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Tamaño máximo del archivo de origen del SVG en kBytes. El servidor devuelve un error cuando se intenta procesar un archivo SVG que supera este límite. El valor predeterminado es 1024 kbytes.

## IS::SvgMAxRenderRgnPixels - Límite de tamaño de imagen de salida de SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Limita el tamaño de las imágenes que puede producir SVGRender. Valor entero mayor que 0 en millones de píxeles. Se devuelve un error si una operación de renderización supera el límite de tamaño. El valor predeterminado es 4.

## PS::svgProvider.port - [!DNL Platform Server] Puerto de escucha {#section-f7e42a96c2dd4523b46f0557c239e659}

El puerto utilizado por SvgRender para obtener imágenes de la variable [!DNL Platform Server] para incrustarlo en representaciones de SVG.

Importante: Para el correcto funcionamiento del componente SVGRender, esta opción de configuración debe establecerse en el mismo valor que `TC::PsPort`.

## PS::svgProvider.fontRoot: carpeta de archivos de fuente del SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Especifica dónde encontrará el SvgRender los archivos de fuente necesarios para procesar el texto del SVG; normalmente una de las rutas especificadas en `IS::RootPaths`. El valor predeterminado es [!DNL  *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Puerto de comunicaciones del SVG {#section-608687123aa644b7b58fe42385d71b79}

Configura el puerto en el que se comunican el servidor de imágenes y el componente SVGRender.

>[!NOTE]
>
>Para el correcto funcionamiento del componente SVGRender, debe especificarse el mismo número de puerto para `SVG::SVGRender.port` y `IS::SVGTcpPort`.
