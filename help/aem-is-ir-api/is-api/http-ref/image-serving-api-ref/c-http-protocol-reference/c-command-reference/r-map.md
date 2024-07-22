---
title: mapa
description: Datos de mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Anula los datos del mapa del catálogo de esta capa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# mapa{#map}

Datos de mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Anula los datos de catalog::Map para esta capa.

`map=[ *`cadena`*]mapA=[ *`cadenaA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cadena</span></span> </p></td> 
  <td class="stentry"> <p>Datos de mapa de imagen para esta capa en coordenadas de capa. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cadenaA</span></span> </p></td> 
  <td class="stentry"> <p>Datos de mapa de imagen para esta capa en coordenadas de imagen de origen. </p></td> 
 </tr> 
</table>

Una cadena vacía indica que esta capa no debe proporcionar un mapa de imagen. La cadena debe tener la codificación HTTP correcta para evitar problemas de análisis.

Todos los caracteres ampersand (&amp;) que se producen en *`string`* deben estar codificados en http.

Mientras `mapA=` y `catalog::Map` especifican datos de mapa en las coordenadas de imagen de origen, `map=` supone coordenadas de capa relativas a la esquina superior izquierda del rectángulo de capa (después de aplicar `rotate=` y `extend=`).

El mapa de imagen de salida siempre se recorta en el rectángulo de capa. Si el atributo `shape` se omite o se establece en `default`, se utilizará todo el rectángulo de capa como área del mapa de imagen.

## Propiedades {#section-a18d9ea95c71414a905a68b8839c0843}

Atributo de capa. Cuando se aplica a `layer=comp`, los datos de mapa especificados se superponen a todos los demás mapas de imagen. Se omitió a menos que `req=map`. Ignorado por las capas de efecto. `mapA=` se omite si `map=` también se especifica.

## Predeterminado {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` se usa si `map=` no se especifica.

## Ejemplo {#section-cd7691c94f984222845c86dcb0051ce8}

Defina un mapa de imagen rectangular para una capa de texto simple:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Se utiliza un elemento `AREA` con atributos predeterminados (en la mayoría de los casos) para insertar el área del mapa para todo el rectángulo de capa.

## Véase también {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Mapas de imagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
