---
description: Especificador de objetos de origen. Los objetos de imagen, SVG y perfil ICC pueden especificarse como entradas de catálogo de imágenes o rutas de archivos relativas
seo-description: Especificador de objetos de origen. Los objetos de imagen, SVG y perfil ICC pueden especificarse como entradas de catálogo de imágenes o rutas de archivos relativas
seo-title: objeto
solution: Experience Manager
title: objeto
topic: Scene7 Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# objeto{#object}

Especificador de objetos de origen. Los objetos de imagen, SVG y perfil ICC pueden especificarse como entradas de catálogo de imágenes o rutas de archivos relativas

` *``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>nombre del catálogo de imágenes ( atributo <span class="codeph">::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID del registro de perfil de imagen, SVG, plantilla o ICC en el catálogo de imágenes especificado, principal o predeterminado </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> path  </span> </span> </p> </td> 
  <td class="stentry"> <p>nombre y ruta relativos del archivo de perfil ICC, máscara o imagen relativa </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object  </span> </span> </p> </td> 
  <td class="stentry"> <p>puede producirse en la ruta de URL principal o en un comando <span class="codeph"> src= </span>, <span class="codeph"> mask= </span> o <span class="codeph"> icc= </span> </p> </td> 
 </tr> 
</table>

*`rootId`* identifica un catálogo de imágenes. (Consulte [Catálogo de imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) para obtener más información). Si se especifica *`rootId`* en la ruta de URL, ese catálogo se convierte en el *catálogo principal* para esta solicitud. De lo contrario, el catálogo predeterminado se utiliza como catálogo principal. En la misma solicitud se pueden usar varios catálogos de imágenes diferentes.

El servidor asume inicialmente que *`rootId`* se omite en los comandos `src=`, `mask=` y `icc=` e intentará encontrar una entrada de catálogo en el catálogo principal. Efectivamente, el servidor intenta utilizar toda la cadena *`object`* como *`objId.`*

Si se encuentra una entrada de catálogo, se utiliza; de lo contrario, el servidor siguiente intenta coincidir con el *`rootId`* de un catálogo de imágenes. Si se identifica un catálogo, se busca *`objId`*. Si se encuentra y entrada, se utiliza.

De lo contrario, *`object`* se asume que es una ruta de archivo explícita. En este caso, si `attribute::FullMatch` está establecido en el catálogo principal, se ignora el catálogo para este objeto y se utiliza el catálogo predeterminado en su lugar. Si `attribute::FullMatch` no está establecido, el catálogo principal se utiliza para un procesamiento posterior.

Tanto *`rootId`* como *`objId`* distinguen entre mayúsculas y minúsculas. *`path`* distingue entre mayúsculas y minúsculas solo en UNIX.

Si se especifica un &#39;/&#39; inicial, se buscará el catálogo predeterminado en lugar del catálogo principal. Esto es principalmente útil cuando una ruta explícita requiere `default::RootPath` en lugar de `attribute::RootPath` del catálogo principal, pero también se puede utilizar para obtener acceso a las entradas del catálogo predeterminado que, de lo contrario, serían anuladas por las entradas del catálogo principal.

Consulte *Administración de contenido* en la *Guía de configuración del servidor* para obtener detalles sobre cómo *`path`* se traduce a una ruta de archivo física.

>[!NOTE]
>
>Los caracteres de coma &#39;,&#39; no están permitidos en *`object.`*

## Formatos de archivo de imagen admitidos {#section-12c85aead78e4f759856ca9ff10637d7}

Consulte la descripción de la utilidad IC (Image Converter) para obtener una lista completa de los formatos de archivo admitidos.

Las aplicaciones que requieren datos de imagen en varias resoluciones diferentes funcionarán mejor al utilizar el formato de varias resoluciones TIFF (PTIF) piramidal de Scene7. La utilidad IC se utiliza para crear imágenes PTIF a partir de cualquier formato de imagen admitido.

## Ejemplos {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Acceso a una imagen y a un perfil ICC en dos catálogos de imágenes diferentes**

Recupere la imagen &#39; [!DNL myImage]&#39; en el catálogo de imágenes identificado como &#39; [!DNL myCatalog]&#39; y adjunte el perfil ICC &#39; [!DNL sRGB]&#39; ubicado en el catálogo de imágenes llamado &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Uso de un único catálogo de imágenes con capas

**Cree una imagen compuesta simple compuesta de tres capas, todas recuperadas de &#39;  [!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Acceso directo a archivos de imagen mientras se utiliza un catálogo para proporcionar atributos**

Acceda a [!DNL my/image/path/myImage.tif] mediante los atributos jpg predeterminados configurados en `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Véase también {#section-b6eccefad63f441d922699c4aba58fc9}

[IC Utility](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [atributo::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
