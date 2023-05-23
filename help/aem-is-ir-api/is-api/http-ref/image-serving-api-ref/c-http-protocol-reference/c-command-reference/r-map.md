---
description: Datos de mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Anula los datos del mapa del catálogo de esta capa.
solution: Experience Manager
title: mapa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# mapa{#map}

Datos de mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Anula los datos de catalog::Map para esta capa.

`map=[ *`cadena`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cadena</span></span> </p></td> 
  <td class="stentry"> <p>Datos de mapa de imagen para esta capa en coordenadas de capa. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Datos de mapa de imagen para esta capa en coordenadas de imagen de origen. </p></td> 
 </tr> 
</table>

Una cadena vacía indica que esta capa no debe proporcionar un mapa de imagen. La cadena debe tener la codificación HTTP correcta para evitar problemas de análisis.

Todos los caracteres ampersand (&amp;) que se producen en *`string`* debe tener codificación http.

While `mapA=` y `catalog::Map` especificar datos de mapa en coordenadas de imagen de origen, `map=` asume coordenadas de capa relativas a la esquina superior izquierda del rectángulo de capa (después de `rotate=` y `extend=` se han aplicado).

El mapa de imagen de salida siempre se recorta en el rectángulo de capa. Si la variable `shape` el atributo se omite o se establece en `default`, todo el rectángulo de capa se utiliza como área del mapa de imagen.

## Propiedades {#section-a18d9ea95c71414a905a68b8839c0843}

Atributo de capa. Cuando se aplica a `layer=comp`, los datos de mapa especificados se superponen a todos los demás mapas de imagen. Ignorado a menos que `req=map`. Ignorado por las capas de efecto. `mapA=` se ignora si `map=` también se especifica.

## Predeterminado {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` se utiliza si `map=` no especificado.

## Ejemplo {#section-cd7691c94f984222845c86dcb0051ce8}

Defina un mapa de imagen rectangular para una capa de texto simple:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Un `AREA` elemento con atributos predeterminados (principalmente) se utiliza para insertar el área del mapa para todo el rectángulo de capa.

## Véase también {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Mapas de imagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
