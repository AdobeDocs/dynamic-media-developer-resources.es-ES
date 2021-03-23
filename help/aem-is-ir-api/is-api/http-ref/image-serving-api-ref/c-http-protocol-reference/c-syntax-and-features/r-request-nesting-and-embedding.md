---
description: El servicio de imágenes admite el anidado ilimitado de solicitudes de servicio de imágenes, la incrustación de solicitudes de renderización de imágenes y la incrustación de imágenes recuperadas de servidores extranjeros. Solo las imágenes de capa y las máscaras de capa admiten estos mecanismos.
seo-description: El servicio de imágenes admite el anidado ilimitado de solicitudes de servicio de imágenes, la incrustación de solicitudes de renderización de imágenes y la incrustación de imágenes recuperadas de servidores extranjeros. Solo las imágenes de capa y las máscaras de capa admiten estos mecanismos.
seo-title: Anidado e incrustación de solicitudes
solution: Experience Manager
title: Anidado e incrustación de solicitudes
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 0%

---


# Anidado e incrustación de solicitudes{#request-nesting-and-embedding}

El servicio de imágenes admite el anidado ilimitado de solicitudes de servicio de imágenes, la incrustación de solicitudes de renderización de imágenes y la incrustación de imágenes recuperadas de servidores extranjeros. Solo las imágenes de capa y las máscaras de capa admiten estos mecanismos.

>[!NOTE]
>
>Algunos clientes de correo electrónico y servidores proxy pueden codificar las llaves utilizadas para la sintaxis de anidación e incrustación. Las aplicaciones para las que este es un problema deben utilizar paréntesis en lugar de llaves.

## Solicitudes anidadas de servicio de imágenes {#section-6954202119e0466f8ff27c79f4f039c8}

Se puede usar una solicitud completa de Image Serving como origen de capa especificándola en el comando `src=` (o `mask=`) utilizando la siguiente sintaxis:

`…&src=is( nestedRequest)&…`

El token `is` distingue entre mayúsculas y minúsculas.

La solicitud anidada no debe incluir la ruta raíz del servidor (normalmente ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>Los caracteres delimitadores de solicitud anidados ( `'(',')'`) y los caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) dentro de las solicitudes anidadas no deben estar codificados con HTTP. En la práctica, las solicitudes anidadas deben codificarse igual que la solicitud externa (anidamiento).

Las reglas de preprocesamiento se aplican a solicitudes anidadas.

Los siguientes comandos se omiten cuando se especifican en solicitudes anidadas (ya sea en la dirección URL de la solicitud o en `catalog::Modifier` o `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Si la imagen resultante de las solicitudes anidadas incluye datos de máscara (alfa), se pasa a la capa de incrustación como máscara de capa.

También se ignoran `attribute::MaxPix`y `attribute::DefaultPix` del catálogo de imágenes que se aplica a la solicitud anidada.

El resultado de la imagen de una solicitud IS anidada se puede almacenar en caché de forma opcional incluyendo `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está deshabilitado. El almacenamiento en caché solo debe habilitarse cuando se espera que la imagen intermedia se reutilice en una solicitud diferente en un periodo de tiempo razonable. Se aplica la administración estándar de caché del lado del servidor. Los datos se almacenan en caché en un formato sin pérdidas.

## Solicitudes de procesamiento de imágenes incrustadas {#section-69c5548db930412b9b90d9b2951a6969}

Cuando Dynamic Media Image Rendering está habilitado en el servidor, las solicitudes de renderización pueden utilizarse como fuentes de capa especificándolas en el comando src= (o mask=). Utilice la siguiente sintaxis:

` …&src=ir( *[!DNL renderRequest]*)&…`

El token `ir` distingue entre mayúsculas y minúsculas.

*[!DNL renderRequest]* es la solicitud de procesamiento de imágenes habitual, excluyendo la ruta raíz HTTP  ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>Los caracteres delimitadores de solicitud anidados ( `'(',')'`) y los caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) dentro de las solicitudes anidadas no deben estar codificados con HTTP. En la práctica, las solicitudes incrustadas deben codificarse igual que la solicitud externa (incrustación).

Los siguientes comandos de renderización de imágenes se omiten cuando se especifican en solicitudes anidadas:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

También se ignoran `attribute::MaxPix` y `attribute::DefaultPix` del catálogo de materiales que se aplica a la solicitud de renderización anidada.

El resultado de la imagen de una solicitud IR anidada se puede almacenar en caché de forma opcional incluyendo `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está deshabilitado. El almacenamiento en caché solo debe habilitarse cuando se espera que la imagen intermedia se reutilice en una solicitud diferente en un periodo de tiempo razonable. Se aplica la administración estándar de caché del lado del servidor. Los datos se almacenan en caché en un formato sin pérdidas.

## Solicitudes de renderización FXG integradas {#section-c817e4b4f7da414ea5a51252ca7e120a}

Cuando el procesador de gráficos FXG (también conocido como [!DNL AGMServer]) está instalado y habilitado con Image Serving, las solicitudes FXG se pueden utilizar como fuentes de capa especificándolas en comandos `src=` (o `mask=`). Utilice la siguiente sintaxis:

`…&src=fxg( renderRequest)&…`

El token `fxg` distingue entre mayúsculas y minúsculas.

>[!NOTE]
>
>La renderización de gráficos FXG solo está disponible en el entorno alojado de Dynamic Media y puede requerir licencias adicionales. Póngase en contacto con el servicio de asistencia técnica de Dynamic Media para obtener más información.

*[!DNL renderRequest]* es la solicitud de procesamiento FXG habitual, excluyendo la ruta raíz HTTP  ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Los caracteres delimitadores ( `'(',')'`) y los caracteres delimitadores de comandos ( `'?'`, `'&'`, `'='`) dentro de solicitudes anidadas no deben estar codificados con HTTP. En la práctica, las solicitudes incrustadas deben codificarse igual que la solicitud externa (incrustación).

Los siguientes comandos FXG se ignoran cuando se especifican en solicitudes anidadas:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Fuentes de imagen externas {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP extranjeros.

>[!NOTE]
>
>Solo se admite el protocolo HTTP para direcciones URL remotas.

Para especificar una URL externa para un comando `src=` o `mask=`, delimite el fragmento de URL o URL externo con paréntesis:

`…&src=( foreignUrl)&…`

Importante Los caracteres delimitadores ( `'(',')'`) y los caracteres delimitadores de comandos ( `'?'`, `'&'`, `'='`) dentro de las solicitudes anidadas no deben estar codificados con HTTP. En la práctica, las solicitudes incrustadas deben codificarse igual que la solicitud externa (incrustación).

Se permiten direcciones URL absolutas completas (si `attribute::AllowDirectUrls` está establecido) y direcciones URL relativas a `attribute::RootUrl`. Se produce un error si se incrusta una dirección URL absoluta y el atributo: `AllowDirectUrls` es 0, o si se especifica una dirección URL relativa y `attribute::RootUrl` está vacía.

Aunque las direcciones URL externas no se pueden especificar directamente en el componente de ruta de la dirección URL de la solicitud, es posible configurar una regla de preprocesamiento para permitir la conversión de rutas relativas a direcciones URL absolutas (consulte el ejemplo siguiente).

El servidor almacena en caché las imágenes externas según los encabezados de almacenamiento en caché incluidos con la respuesta HTTP. Si no hay un encabezado de respuesta `ETag` ni un encabezado de respuesta HTTP de última modificación, la respuesta no se almacena en caché. Esto puede causar un rendimiento deficiente para accesos repetidos para la misma imagen externa, ya que Image Serving necesita recuperar y revalidar la imagen en cada acceso.

Este mecanismo admite los mismos formatos de archivo de imagen compatibles con la utilidad Image Convert (IC), a excepción de las imágenes de origen con 16 bits por componente.

>[!NOTE]
>
>Image Serving ejecutará automáticamente la utilidad de validación cuando se utilice por primera vez una imagen externa para garantizar que la imagen sea válida y no se haya dañado durante la transmisión. Esto puede causar un ligero retraso en el primer acceso. Para obtener el mejor rendimiento, se recomienda limitar el tamaño de dichas imágenes y/o utilizar un formato de archivo de imagen que se comprima bien.

## Restricciones {#section-fb68e3f0d40947feb94d7bf183b64929}

Normalmente, el tamaño de la imagen generada por las solicitudes anidadas/incrustadas se optimiza automáticamente. Si el almacenamiento en caché de imágenes de solicitud anidadas está habilitado, se pueden obtener mejoras de rendimiento incrementales especificando el tamaño exacto de la imagen anidada, de modo que no se requiera ningún escalado adicional cuando se vuelva a utilizar la entrada de caché.

Importante: El servicio de imágenes no admite la doble codificación de solicitudes anidadas o incrustadas. Las solicitudes anidadas e incrustadas deben estar codificadas en HTTP del mismo modo que las solicitudes simples.

## Ejemplos {#section-d800cfc31abe46d2a964f8e7929231f1}

**Plantilla de capas con almacenamiento en caché:**

Utilice el anidado para añadir el almacenamiento en caché a una plantilla de capas. Un número limitado de imágenes de fondo están superpuestas con texto altamente variable. La cadena de plantilla inicial puede tener este aspecto:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Con ligeras modificaciones, podemos escalar previamente la imagen de capa 0 y almacenarla en caché de forma persistente, reduciendo así la carga del servidor:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Incrustación de solicitudes para el procesamiento de imágenes de Dynamic Media**

Uso de una plantilla almacenada en [!DNL myCatalog/myTemplate]; genere la imagen para la capa 2 de la plantilla mediante el procesamiento de imágenes de Dynamic Media:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Observe las llaves anidadas. La solicitud de renderización de imágenes incrusta una llamada de vuelta en Image Serving para recuperar una textura repetible.

## Véase también {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Image Rendering Reference,  [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [Image Serving Utilities](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
