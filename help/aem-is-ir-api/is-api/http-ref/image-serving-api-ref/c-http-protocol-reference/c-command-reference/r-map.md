---
title: mapa
description: Datos de mapa de imagen. Proporciona datos de mapa de imagen para esta capa. Anula los datos del mapa del catálogo de esta capa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
TQID: 'https://experienceleague.adobe.com/9JJUVcw5-wl0B-rP-m6DC1c1DGIqxaV2UgboocFGGV8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 224
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
