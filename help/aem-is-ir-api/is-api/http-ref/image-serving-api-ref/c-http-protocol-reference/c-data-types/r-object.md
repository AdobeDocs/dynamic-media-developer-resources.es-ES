---
description: Especificador de objeto de origen. Los objetos de perfil de imagen, SVG e ICC se pueden especificar como entradas de catálogo de imágenes o rutas de archivo relativas
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

Especificador de objeto de origen. Los objetos de perfil de imagen, SVG e ICC se pueden especificar como entradas de catálogo de imágenes o rutas de archivo relativas

`*`objeto`*[/]{[ *`rootId`*/] *`objId`*}| *`ruta`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>nombre del catálogo de imágenes ( <span class="codeph"> attribute::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span> </span> </p> </td> 
  <td class="stentry"> <p>id del registro de imagen, SVG, plantilla o perfil ICC en el catálogo de imágenes especificado, principal o predeterminado </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ruta </span> </span> </p> </td> 
  <td class="stentry"> <p>ruta y nombre del archivo de perfil de imagen, máscara o ICC relativa </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objeto </span> </span> </p> </td> 
  <td class="stentry"> <p>puede producirse en la ruta de URL principal o en un <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>, o <span class="codeph"> icc= </span> mando </p> </td> 
 </tr> 
</table>

*`rootId`* identifica un catálogo de imágenes. (Consulte [Catálogo de imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) para obtener más información). If *`rootId`* se especifica en la ruta URL, ese catálogo se convierte en el *catálogo principal* para esta solicitud. De lo contrario, el catálogo predeterminado se utiliza como catálogo principal. Se pueden utilizar varios catálogos de imágenes diferentes en la misma solicitud.

El servidor supone inicialmente que *`rootId`* se omite en `src=`, `mask=`, y `icc=` e intentará encontrar una entrada de catálogo en el catálogo principal. Efectivamente, el servidor intenta usar el *`object`* cadena como *`objId.`*

Si se encuentra una entrada de catálogo, se utiliza; de lo contrario, el servidor intenta buscar la coincidencia en el *`rootId`* de un catálogo de imágenes. Si se identifica un catálogo, se busca *`objId`*. Si se encuentra la entrada y, se utiliza.

De lo contrario, *`object`* se supone que es una ruta de archivo explícita. En este caso, si `attribute::FullMatch` se establece en el catálogo principal, el catálogo se ignora para este objeto y se utiliza el catálogo predeterminado en su lugar. If `attribute::FullMatch` no está configurado, el catálogo principal se utiliza para un procesamiento posterior.

Ambos *`rootId`* y *`objId`* distinguen entre mayúsculas y minúsculas. *`path`* distingue entre mayúsculas y minúsculas solo en UNIX.

Si un interlineado `/` se especifica, se busca en el catálogo predeterminado en lugar del catálogo principal. Esto resulta principalmente útil cuando una ruta explícita requiere `default::RootPath` en lugar del catálogo principal `attribute::RootPath`, pero también se puede utilizar para obtener acceso a las entradas del catálogo predeterminado que, de lo contrario, se anularían con las entradas del catálogo principal.

Consulte *Administración de contenido* en el *Guía de configuración del servidor* para obtener más información sobre cómo *`path`* se traduce a una ruta de archivo física.

>[!NOTE]
>
>No se permiten caracteres comas &quot;,&quot; en *`object.`*

## Formatos de archivo de imagen admitidos {#section-12c85aead78e4f759856ca9ff10637d7}

Consulte la descripción de la utilidad IC (Image Converter) para obtener una lista completa de los formatos de archivo compatibles.

Las aplicaciones que requieren datos de imagen en varias resoluciones diferentes funcionan mejor cuando se utiliza el formato de varias resoluciones del TIFF piramidal de Dynamic Media (PTIF). La utilidad IC se utiliza para crear imágenes PTIF a partir de cualquier formato de imagen admitido.

## Ejemplos {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Acceso a una imagen y a un perfil ICC en dos catálogos de imágenes diferentes**

Recupere la imagen &#39; [!DNL myImage]&#39; en el catálogo de imágenes identificado como &#39; [!DNL myCatalog]&#39; y adjuntar el perfil ICC &#39; [!DNL sRGB]&#39; ubicado en el catálogo de imágenes denominado &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Uso de un único catálogo de imágenes con capas

**Crear una imagen compuesta simple que consta de tres capas, todas recuperadas de &#39; [!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Acceso directo a archivos de imagen mientras se sigue utilizando un catálogo para proporcionar atributos**

Acceso [!DNL my/image/path/myImage.tif], utilizando los atributos jpg predeterminados configurados en `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Véase también {#section-b6eccefad63f441d922699c4aba58fc9}

[Utilidad IC](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
