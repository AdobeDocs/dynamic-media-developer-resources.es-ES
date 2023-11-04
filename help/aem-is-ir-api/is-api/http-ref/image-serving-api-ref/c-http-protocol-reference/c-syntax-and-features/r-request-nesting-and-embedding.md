---
description: El servicio de imágenes admite el anidamiento ilimitado de solicitudes del servicio de imágenes, la incrustación de solicitudes de procesamiento de imágenes y la incrustación de imágenes recuperadas de servidores externos. Solo las imágenes de capa y las máscaras de capa admiten estos mecanismos.
solution: Experience Manager
title: Solicitud de anidación e incrustación
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1044'
ht-degree: 0%

---

# Solicitud de anidación e incrustación{#request-nesting-and-embedding}

El servicio de imágenes admite el anidamiento ilimitado de solicitudes del servicio de imágenes, la incrustación de solicitudes de procesamiento de imágenes y la incrustación de imágenes recuperadas de servidores externos. Solo las imágenes de capa y las máscaras de capa admiten estos mecanismos.

>[!NOTE]
>
>Algunos clientes de correo electrónico y servidores proxy pueden codificar las llaves utilizadas para anidar e incrustar sintaxis. Las aplicaciones para las que esto es un problema deben utilizar paréntesis en lugar de llaves.

## Solicitudes de servicio de imágenes anidadas {#section-6954202119e0466f8ff27c79f4f039c8}

Una solicitud de servicio de imágenes completa se puede utilizar como origen de capa especificándola en la variable `src=` (o `mask=`) mediante la siguiente sintaxis:

`…&src=is( nestedRequest)&…`

El `is` distingue entre mayúsculas y minúsculas.

La solicitud anidada no debe incluir la ruta raíz del servidor (normalmente ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>Los caracteres delimitadores de solicitud anidados ( `'(',')'`) y los caracteres delimitadores de comandos ( `'?'`, `'&'`, `'='`) en las solicitudes anidadas no debe tener codificación HTTP. En la práctica, las solicitudes anidadas deben codificarse igual que la solicitud externa (anidación).

Las reglas de preprocesamiento se aplican a las solicitudes anidadas.

Los siguientes comandos se omiten cuando se especifican en solicitudes anidadas (en la dirección URL de la solicitud o en `catalog::Modifier` o `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Si la imagen de resultado de las solicitudes anidadas incluye datos de máscara (alfa), se pasa a la capa de incrustación como máscara de capa.

También se ignoran `attribute::MaxPix`y `attribute::DefaultPix` del catálogo de imágenes que se aplica a la solicitud anidada.

El resultado de imagen de una solicitud IS anidada se puede almacenar en caché de forma opcional incluyendo `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está deshabilitado. El almacenamiento en caché solo debe habilitarse cuando se espere que la imagen intermedia se reutilice en una solicitud diferente en un período de tiempo razonable. Se aplica la administración de caché estándar del lado del servidor. Los datos se almacenan en caché en un formato sin pérdidas.

## Solicitudes de procesamiento de imágenes incrustadas {#section-69c5548db930412b9b90d9b2951a6969}

Cuando el procesamiento de imágenes de Dynamic Media está habilitado en el servidor, las solicitudes de procesamiento se pueden utilizar como fuentes de capas especificándolas en el comando src= (o mask=). Utilice la siguiente sintaxis:

` …&src=ir( *[!DNL renderRequest]*)&…`

El `ir` distingue entre mayúsculas y minúsculas.

*[!DNL renderRequest]* es la solicitud de procesamiento de imágenes habitual, excluyendo la ruta raíz HTTP ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>Los caracteres delimitadores de solicitud anidados ( `'(',')'`) y los caracteres delimitadores de comandos ( `'?'`, `'&'`, `'='`) en las solicitudes anidadas no debe tener codificación HTTP. En la práctica, las solicitudes incrustadas deben codificarse igual que la solicitud externa (incrustación).

Los siguientes comandos de procesamiento de imágenes se omiten cuando se especifican en solicitudes anidadas:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

También se ignoran `attribute::MaxPix` y `attribute::DefaultPix` del catálogo de materiales que se aplica a la solicitud de procesamiento anidada.

El resultado de imagen de una solicitud IR anidada se puede almacenar en caché de forma opcional incluyendo `cache=on`. De forma predeterminada, el almacenamiento en caché de datos intermedios está deshabilitado. El almacenamiento en caché solo debe habilitarse cuando se espere que la imagen intermedia se reutilice en una solicitud diferente en un período de tiempo razonable. Se aplica la administración de caché estándar del lado del servidor. Los datos se almacenan en caché en un formato sin pérdidas.

## Solicitudes de procesamiento FXG incrustadas {#section-c817e4b4f7da414ea5a51252ca7e120a}

Cuando el procesador de gráficos FXG (aka [!DNL AGMServer]) está instalado y habilitado con el servicio de imágenes, las solicitudes FXG se pueden utilizar como fuentes de capa especificándolas en `src=` (o `mask=`) comandos. Utilice la siguiente sintaxis:

`…&src=fxg( renderRequest)&…`

El `fxg` distingue entre mayúsculas y minúsculas.

>[!NOTE]
>
>El procesamiento de gráficos FXG solo está disponible en el entorno alojado de Dynamic Media y puede requerir licencias adicionales. Póngase en contacto con el soporte técnico de Dynamic Media para obtener más información.

*[!DNL renderRequest]* es la solicitud de procesamiento FXG habitual, excluyendo la ruta raíz HTTP ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Los caracteres delimitadores ( `'(',')'`) y los caracteres delimitadores de comandos ( `'?'`, `'&'`, `'='`) en las solicitudes anidadas no debe tener codificación HTTP. En la práctica, las solicitudes incrustadas deben codificarse igual que la solicitud externa (incrustación).

Los siguientes comandos FXG se omiten cuando se especifican en solicitudes anidadas:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Fuentes de imagen externas {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP externos.

>[!NOTE]
>
>Solo se admite el protocolo HTTP para las direcciones URL remotas.

Para especificar una dirección URL externa para una `src=` o una `mask=` , delimite la URL externa o el fragmento de URL con paréntesis:

`…&src=( foreignUrl)&…`

Importante: Los caracteres delimitadores ( `'(',')'`) y los caracteres delimitadores de comandos ( `'?'`, `'&'`, `'='`) en las solicitudes anidadas no debe tener codificación HTTP. En la práctica, las solicitudes incrustadas deben codificarse igual que la solicitud externa (incrustación).

Direcciones URL absolutas completas (si `attribute::AllowDirectUrls` se ha configurado) y direcciones URL relativas a `attribute::RootUrl` están permitidos. Se produce un error si una dirección URL absoluta está incrustada y tiene el atributo: `AllowDirectUrls` es 0 o si se especifica una dirección URL relativa y `attribute::RootUrl` está vacío.

Aunque las direcciones URL extranjeras no se pueden especificar directamente en el componente de ruta de la dirección URL de solicitud, es posible configurar una regla de preprocesamiento para permitir la conversión de rutas relativas a direcciones URL absolutas (consulte el ejemplo siguiente).

El servidor almacena en caché las imágenes externas según los encabezados de almacenamiento en caché incluidos con la respuesta HTTP. Si no hay `ETag` Si no hay ningún encabezado de respuesta HTTP Last-Modified, la respuesta no se almacena en caché. Esto puede causar un mal rendimiento para los accesos repetidos para la misma imagen externa, ya que el servicio de imágenes necesita recuperar y revalidar la imagen en cada acceso.

Este mecanismo admite los mismos formatos de archivo de imagen que la utilidad Image Convert (IC), con la excepción de las imágenes de origen con 16 bits por componente.

>[!NOTE]
>
>El servicio de imágenes ejecuta automáticamente la utilidad validate cuando se utiliza una imagen externa por primera vez, para garantizar que la imagen sea válida y que no se haya dañado durante la transmisión. Esto puede causar un ligero retraso en el primer acceso. Para obtener el mejor rendimiento, se recomienda limitar el tamaño de dichas imágenes o utilizar un formato de archivo de imagen que se comprima bien.

## Restricciones {#section-fb68e3f0d40947feb94d7bf183b64929}

El tamaño de la imagen generada por las solicitudes anidadas/incrustadas normalmente se optimiza automáticamente. Si se habilita el almacenamiento en caché de imágenes de solicitud anidadas, se pueden lograr mejoras de rendimiento incrementales especificando el tamaño exacto de la imagen anidada, de modo que no se requiera un escalado adicional cuando se reutilice la entrada de caché.

Importante: El servicio de imágenes no admite la codificación doble de solicitudes anidadas o incrustadas. Las solicitudes anidadas e incrustadas deben estar codificadas en HTTP como las solicitudes simples.

## Ejemplos {#section-d800cfc31abe46d2a964f8e7929231f1}

**Plantilla de capas con almacenamiento en caché:**

Utilice el anidamiento para añadir el almacenamiento en caché a una plantilla de capas. Un número limitado de imágenes de fondo se superponen con texto altamente variable. La cadena de plantilla inicial puede tener este aspecto:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Con pequeñas modificaciones, podemos escalar previamente la imagen de capa 0 y almacenarla en caché de forma persistente, reduciendo así la carga del servidor:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Incrustar solicitudes para el procesamiento de imágenes de Dynamic Media**

Uso de una plantilla almacenada en [!DNL myCatalog/myTemplate]; genere la imagen para la capa 2 de la plantilla mediante Dynamic Media Image Rendering:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Observe las llaves anidadas. La solicitud de procesamiento de imágenes incrusta una llamada de nuevo al servicio de imágenes para recuperar una textura repetible.

## Véase también {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Solicitar procesamiento previo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Referencia de procesamiento de imágenes, [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Utilidades del servicio de imágenes](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
