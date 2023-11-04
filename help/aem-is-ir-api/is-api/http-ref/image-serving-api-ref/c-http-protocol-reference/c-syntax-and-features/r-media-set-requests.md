---
description: El servicio de imágenes proporciona un mecanismo para recuperar una respuesta de texto jerárquico (xml o json) que representa todos los recursos y metadatos asociados con el conjunto de imágenes del catálogo para un registro determinado.
solution: Experience Manager
title: Solicitudes de conjunto de medios
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---

# Solicitudes de conjunto de medios{#media-set-requests}

El servicio de imágenes proporciona un mecanismo para recuperar una respuesta de texto jerárquico (xml o json) que representa todos los recursos y metadatos asociados con catalog::ImageSet para un registro determinado.

Los visualizadores pueden utilizar este mecanismo para generar respuestas que informen a la presentación de imágenes, vídeos, conjuntos de vídeos, conjuntos de muestras, conjuntos de giros, conjuntos de páginas (catálogos electrónicos) y conjuntos de medios sencillos.

## Sintaxis de solicitud {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

La respuesta establecida para un `catalog::ImageSet` se puede recuperar mediante la variable `req=set` modificador y referencia al id de registro de catálogo en la ruta siguiente. Como alternativa, el conjunto de imágenes se puede especificar directamente en la dirección URL utilizando `imageset=` modificador. Si la variable `imageset=` Cuando se utiliza un modificador para especificar el conjunto de imágenes, todo el valor debe incluirse entre llaves para omitir el valor del conjunto de imágenes y garantizar que los modificadores incluidos no se interpreten como parte de la cadena de consulta URL.

## Tipos de respuestas del conjunto {#section-93eb0a1f70344da2a888e56372ad3896}

El mecanismo de conjunto admite los siguientes tipos de respuestas:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>imágenes simples </p></td> 
  <td class="stentry"> <p>Un registro de imagen sin <span class="codeph"> catalog::ImageSet</span> definido. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>vídeos simples </p></td> 
  <td class="stentry"> <p>Una grabación de vídeo en el catálogo de contenido estático. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de muestras </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consta de una referencia a un registro de imagen y una referencia independiente opcional a un registro de imagen utilizado como muestra. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de muestras jerárquicos </p></td> 
  <td class="stentry"> <p>Un conjunto de elementos formado por un elemento de muestra básico o una referencia a un registro de conjunto de muestras. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de giros </p></td> 
  <td class="stentry"> <p>Un conjunto de elementos que consta de una lista simple de ID de imagen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de giros bidimensionales </p></td> 
  <td class="stentry"> <p>Conjunto de elementos formado por una imagen simple o una referencia a un conjunto de giros básico. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de páginas </p></td> 
  <td class="stentry"> <p>Conjunto de elementos formado por una lista de hasta tres imágenes de página </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de medios </p></td> 
  <td class="stentry"> <p>Conjunto de elementos formado por imágenes simples, conjuntos de vídeos, conjuntos de muestras, conjuntos de muestras jerárquicos, conjuntos de giros, conjuntos de giros bidimensionales, conjuntos de páginas y recursos de vídeo. Cada elemento del conjunto de medios también puede contener una muestra opcional. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de vídeos </p></td> 
  <td class="stentry"> <p>Un conjunto de elementos que consta de una lista de vídeos simples. </p></td> 
 </tr> 
</table>

## Detección del tipo de conjunto externo {#section-3dd6e453528d46898e559d31458a59ba}

Cuando un `req=set` Si se recibe la solicitud, el tipo de respuesta que se va a generar se determina mediante el valor de `catalog::AssetType`. If `catalog::AssetType` no está definida, el tipo de respuesta viene determinado por las siguientes reglas:

* Si el registro se encuentra en el catálogo de imágenes Y `catalog::ImageSet` está definido

   * Supongamos que el catálogo electrónico se ha definido si al menos una entrada del campo de registro Conjunto de imágenes contiene dos puntos
   * Supongamos que el conjunto de medios está establecido si al menos una entrada del campo de conjunto de imágenes de registro contiene dos punto y coma.
   * Supongamos que el conjunto de imágenes está establecido si al menos una entrada del campo de conjunto de imágenes de registro contiene un punto y coma.
   * Supongamos que hay un conjunto de giros si ninguna entrada contiene dos puntos ni un punto y coma, pero al menos una entrada contiene un conjunto referenciado o un conjunto en línea (se trata de un conjunto de giros 2D).
   * Supongamos que se trata de un conjunto desconocido si ninguna entrada contiene dos puntos o un punto y coma, ni un conjunto al que se hace referencia ni un conjunto en línea (es decir, una lista de imágenes separadas por comas).

* Si el registro se encuentra en los catálogos de contenido estático Y de imagen

   * Supongamos que el vídeo tiene la extensión de archivo en el siguiente conjunto: mp3, mp4, flv, f4v, swf, xml
   * Suponer imagen de lo contrario

* Si el registro se encuentra en el catálogo de contenido estático pero NO en el catálogo de imágenes

   * Supongamos que el vídeo tiene la extensión de archivo en el siguiente conjunto: mp3, mp4, flv, f4v, swf, xml
   * Suponer estático en caso contrario

* Si el registro de se encuentra en el catálogo de imágenes pero NO en el catálogo de contenido estático

   * Asumir imagen

* Si el registro NO se encuentra en el catálogo de imágenes y NO se encuentra en el catálogo de contenido estático

   * Supongamos que hay un vídeo basado en archivos si la extensión de archivo está en el siguiente conjunto: mp3, mp4, flv, f4v, swf, xml
   * De lo contrario, supongamos una imagen basada en archivos

En todos los casos, la respuesta xml resultante se ajusta al documento XML especificado con el nodo raíz establecido correspondiente al tipo detectado.

## Detección del tipo de conjunto interno {#section-8f46490e467247e69ce284704def06f3}

Cuando se detecta el conjunto externo como un conjunto de medios de tipo, la respuesta contiene un conjunto de elementos de conjunto de medios correspondientes a cada entrada de conjunto de medios en `catalog::ImageSet`. Si se especifica el parámetro de tipo opcional para una entrada de conjunto de medios determinada, se asigna a un tipo de salida según la tabla siguiente:

| Tipo de entrada | Tipo de salida |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

Si no se especifica el parámetro de tipo opcional para una entrada de conjunto de medios concreta o corresponde a un tipo no admitido, el tipo de elemento del conjunto de medios se detecta automáticamente utilizando las mismas reglas que se aplicaron en el nivel del conjunto externo.

## Especificación XML {#section-c1bd60948ef545759a16885bb6fcc607}

La respuesta xml devuelta se ajusta a la siguiente especificación:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

El `labelkey=` se utiliza junto con el modificador `catalog::UserData`para generar etiquetas para imágenes y muestras. El `catalog:UserData` El campo se analiza como un conjunto de pares clave/valor y los índices labelkey se incluyen en este conjunto para recuperar el valor de la clave dada. Este valor se devuelve en la variable *`l`* para el *`s`* y *`i`*.

## Restricciones forzadas {#section-b9f042873bee45a5ae11b69fd42f2bca}

Para limitar el tamaño de la respuesta y evitar problemas de autorreferencia, la propiedad del servidor controla la profundidad máxima de anidación `PS::fvctx.nestingLimit`. Si se supera este límite, se devuelve un error.

Para limitar el tamaño de las respuestas xml de los grandes conjuntos de catálogos electrónicos, se suprimen los metadatos privados para los elementos de conjuntos de folletos según la propiedad del servidor `PS::fvctx.brochureLimit`. Todos los metadatos privados asociados con el folleto se exportan hasta que se alcanza el límite. Una vez superado el límite, los mapas privados y los datos de usuario se suprimen y se establece un indicador correspondiente para indicar qué tipo de datos se suprimió.

No se admiten conjuntos de medios anidados. Un conjunto de medios anidado se define como un conjunto de medios que contiene un elemento del conjunto de medios del tipo conjunto de medios. Si se detecta esta condición, se devuelve un error.

## Ejemplos {#section-588c9d33aa05482c86cd2b1936887228}

Para respuestas XML de ejemplo para `req=set` , consulte la página Propiedades en el encabezado Ejemplos de HTML.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Véase también {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [Referencia de catálogo de imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
