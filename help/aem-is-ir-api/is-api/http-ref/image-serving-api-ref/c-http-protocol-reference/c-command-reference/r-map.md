---
description: Datos del mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Anula cualquier dato del mapa del catálogo de esta capa.
seo-description: Datos del mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Anula cualquier dato del mapa del catálogo de esta capa.
seo-title: mapa
solution: Experience Manager
title: mapa
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 3%

---


# mapa{#map}

Datos del mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Anula cualquier dato del catálogo::Map para esta capa.

`map=[ *``*]mapA=[ *`cadenaA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Datos de mapa de imagen para esta capa en coordenadas de capa. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Datos de mapa de imagen para esta capa en coordenadas de imagen de origen. </p></td> 
 </tr> 
</table>

Una cadena vacía indica que esta capa no debe proporcionar un mapa de imagen. La cadena debe tener la codificación HTTP correcta para evitar problemas de análisis.

Todos los caracteres de símbolo &amp; que se encuentren en *`string`* deben tener codificación http.

Mientras que `mapA=` y `catalog::Map` especifican datos de mapa en las coordenadas de la imagen de origen, `map=` supone coordenadas de capa relativas a la esquina superior izquierda del rectángulo de capa (después de aplicar `rotate=` y `extend=`).

El mapa de imagen de salida siempre se recorta al rectángulo de la capa. Si se omite el atributo `shape` o se establece en `default`, se utilizará todo el rectángulo de capa como área de mapa de imagen.

## Propiedades {#section-a18d9ea95c71414a905a68b8839c0843}

Atributo de capa. Cuando se aplica a `layer=comp`, los datos de mapa especificados se superponen a todos los demás mapas de imágenes. Se omite a menos que `req=map`. Ignorado por capas de efecto. `mapA=` se ignora si también  `map=` se especifica .

## Predeterminado {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` se utiliza si no  `map=` se especifica.

## Ejemplo {#section-cd7691c94f984222845c86dcb0051ce8}

Defina un mapa de imagen rectangular para una capa de texto simple:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Se utiliza un elemento `AREA` con atributos predeterminados (principalmente) para insertar el área de asignación para todo el rectángulo de capa.

## Véase también {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Mapas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab) de imágenes,  [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
