---
description: Especificador de objetos de origen. Los objetos de perfil de imagen, SVG y ICC pueden especificarse como entradas de catálogo de imágenes o rutas de archivo relativas
solution: Experience Manager
title: objeto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 1%

---

# objeto{#object}

Especificador de objetos de origen. Los objetos de perfil de imagen, SVG y ICC pueden especificarse como entradas de catálogo de imágenes o rutas de archivo relativas

`*`object`*[/]{[ *`rootId`*/] *`objId`*}| *`ruta`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>nombre del catálogo de imágenes ( <span class="codeph"> atributo::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span> </span> </p> </td> 
  <td class="stentry"> <p>id del registro de imagen, SVG, plantilla o perfil ICC en el catálogo de imágenes especificado, principal o predeterminado </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ruta </span> </span> </p> </td> 
  <td class="stentry"> <p>imagen relativa, máscara o ruta y nombre del archivo de perfil ICC </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object </span> </span> </p> </td> 
  <td class="stentry"> <p>puede producirse en la ruta de URL principal o en una <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>o <span class="codeph"> icc= </span> command </p> </td> 
 </tr> 
</table>

*`rootId`* identifica un catálogo de imágenes. (Consulte [Catálogo de imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) para obtener más información). If *`rootId`* se especifica en la ruta URL, ese catálogo se convierte en la variable *catálogo principal* para esta solicitud. De lo contrario, el catálogo predeterminado se utiliza como catálogo principal. En la misma solicitud se pueden usar varios catálogos de imágenes diferentes.

El servidor asume inicialmente que *`rootId`* se omite en `src=`, `mask=`y `icc=` e intentará encontrar una entrada de catálogo en el catálogo principal. En la práctica, el servidor intenta usar todo el *`object`* string como *`objId.`*

Si se encuentra una entrada de catálogo, se utiliza; de lo contrario, el servidor siguiente intenta coincidir con el *`rootId`* de un catálogo de imágenes. Si se identifica un catálogo, se busca *`objId`*. Si se encuentra y , se utiliza.

De lo contrario, *`object`* se supone que es una ruta de archivo explícita. En este caso, si `attribute::FullMatch` se establece en el catálogo principal, se ignora el catálogo para este objeto y se utiliza el catálogo predeterminado en su lugar. If `attribute::FullMatch` no está configurado, el catálogo principal se utiliza para un procesamiento posterior.

Ambas *`rootId`* y *`objId`* distinguen entre mayúsculas y minúsculas. *`path`* distingue entre mayúsculas y minúsculas solo en UNIX.

Si un encabezado `/` se especifica, se busca en el catálogo predeterminado en lugar del catálogo principal. Esto resulta principalmente útil cuando una ruta explícita requiere `default::RootPath` en lugar del catálogo principal `attribute::RootPath`, pero también se puede utilizar para obtener acceso a las entradas del catálogo predeterminado que, de lo contrario, serían anuladas por las entradas del catálogo principal.

Consulte *Administración de contenido* en el *Guía de configuración del servidor* para obtener más información sobre cómo *`path`* se traduce a una ruta de archivo física.

>[!NOTE]
>
>Los caracteres de coma &#39;,&#39; no están permitidos en *`object.`*

## Formatos de archivo de imagen compatibles {#section-12c85aead78e4f759856ca9ff10637d7}

Consulte la descripción de la utilidad IC (Image Converter) para obtener una lista completa de los formatos de archivo admitidos.

Las aplicaciones que requieran datos de imagen en varias resoluciones diferentes tendrán un mejor rendimiento al usar el formato de varias resoluciones del TIFF piramidal de Dynamic Media (PTIF). La utilidad IC se utiliza para crear imágenes PTIF a partir de cualquier formato de imagen admitido.

## Ejemplos {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Acceso a una imagen y a un perfil ICC en dos catálogos de imágenes diferentes**

Recupere la imagen &#39; [!DNL myImage]&#39; en el catálogo de imágenes identificado como &#39; [!DNL myCatalog]&#39; y adjunte el perfil ICC &#39; [!DNL sRGB]&#39; ubicado en el catálogo de imágenes llamado &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Uso de un catálogo de imágenes único con capas

**Cree una imagen compuesta simple que consta de tres capas, todas recuperadas de &#39; [!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Acceso a archivos de imagen directamente mientras se sigue utilizando un catálogo para proporcionar atributos**

Acceso [!DNL my/image/path/myImage.tif], utilizando los atributos JPG predeterminados configurados en `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Véase también {#section-b6eccefad63f441d922699c4aba58fc9}

[Utilidad IC](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [atributo::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
