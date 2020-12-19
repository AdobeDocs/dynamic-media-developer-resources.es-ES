---
description: Datos de mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Sobrescribe cualquier dato del mapa del catálogo para esta capa.
seo-description: Datos de mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Sobrescribe cualquier dato del mapa del catálogo para esta capa.
seo-title: mapa
solution: Experience Manager
title: mapa
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 3%

---


# mapa{#map}

Datos de mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Sobrescribe cualquier dato del catálogo::Map para esta capa.

`map=[ *``*]mapA=[ *`stringstringA`*]`

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

Todos los caracteres de símbolo de unión (&amp;) que se producen en *`string`* deben tener codificación http.

Mientras que `mapA=` y `catalog::Map` especifican los datos del mapa en las coordenadas de la imagen de origen, `map=` asume las coordenadas de la capa en relación con la esquina superior izquierda del rectángulo de capa (después de que se hayan aplicado `rotate=` y `extend=`).

El mapa de imagen de salida siempre se recorta al rectángulo de la capa. Si se omite el atributo `shape` o se establece en `default`, se utilizará todo el rectángulo de capa como área del mapa de imagen.

## Propiedades {#section-a18d9ea95c71414a905a68b8839c0843}

Atributo de capa. Cuando se aplica a `layer=comp`, los datos del mapa especificado se sitúan detrás de todos los demás mapas de imagen. Se omite a menos que `req=map`. Omitido por capas de efectos. `mapA=` se ignora si  `map=` se especifica también.

## Predeterminado {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` si no  `map=` se especifica.

## Ejemplo {#section-cd7691c94f984222845c86dcb0051ce8}

Defina un mapa de imagen rectangular para una capa de texto simple:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Se utiliza un elemento `AREA` con atributos predeterminados (principalmente) para insertar el área del mapa para todo el rectángulo de la capa.

## Véase también {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Mapas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab) de imagen,  [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
