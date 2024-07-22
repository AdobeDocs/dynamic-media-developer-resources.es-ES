---
title: imageSet
description: Conjunto de imágenes. Especifica un valor de conjunto de imágenes para utilizarlo al generar la respuesta req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---

# imageSet{#imageset}

Conjunto de imágenes. Especifica un valor de conjunto de imágenes para utilizarlo al generar la respuesta req=set.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Cadena del conjunto de imágenes. </p></td> 
 </tr> 
</table>

Para omitir el valor y asegurarse de que los modificadores incluidos no se interpreten como parte de la cadena de consulta URL, todo el valor debe incluirse entre llaves. Si el registro de catálogo se especifica en la ruta de acceso de red, este valor de modificador anula `catalog::ImageSet` del registro principal. Para obtener una descripción de la sintaxis válida del conjunto de imágenes, consulte la documentación de `catalog::ImageSet`.

## Propiedades {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Atributo de solicitud. Opcional. Anula `catalog::ImageSet` del registro principal.

## Predeterminado {#section-e8622ff40408450fb79d028f8d37fa6b}

Ninguno.

## Ejemplo {#section-68513d3c601f477399602a0741dab390}

Especificar conjunto de imágenes para usar con la solicitud `req=set`:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Véase también {#section-7e0320b2e09d475897082711a8f023a9}

[catálogo::Conjunto de imágenes](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) , [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Solicitudes de conjunto de medios](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
