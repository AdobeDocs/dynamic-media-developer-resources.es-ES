---
description: Las características y la sintaxis de los catálogos de imágenes se describen en esta sección.
seo-description: Las características y la sintaxis de los catálogos de imágenes se describen en esta sección.
seo-title: Catálogos de imágenes
solution: Experience Manager
title: Catálogos de imágenes
topic: Scene7 Image Serving - Image Rendering API
uuid: d329807a-22b0-42a3-9297-8dad7a1dce43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Catálogos de imágenes{#image-catalogs}

Las características y la sintaxis de los catálogos de imágenes se describen en esta sección.

Los catálogos de imágenes oferta las siguientes funciones:

* Permitir la asociación persistente de imágenes con determinados comandos de modificador y metadatos.

   Se hace referencia a las entradas de los catálogos de imágenes mediante una notación de método abreviado ` *`rootId/objId`*`, donde ` *`rootId`*` identifica el catálogo de imágenes y ` *`objId`*` identifica un registro de datos del catálogo.
* Proporcione valores predeterminados para determinados atributos de solicitud, como la calidad JPEG o si se va a aplicar una marca de agua.
* Administrar fuentes, perfiles ICC, definiciones de macros y plantillas de solicitud

Aunque no se definan catálogos de imágenes específicos, todas las funciones de los catálogos de imágenes están disponibles a través del catálogo predeterminado ( [!DNL default.ini]).

Si ` *`rootId`*` en la ruta de URL de la solicitud coincide con `attribute::RootId` un catálogo de imágenes específico, ese catálogo se convertirá en el catálogo principal para esta solicitud. El catálogo principal proporciona los atributos y la configuración predeterminados para toda la solicitud. Si no se encuentra ninguna coincidencia, se utiliza el catálogo predeterminado.

Un catálogo identificado en un `src=` comando o `mask=` proporciona los siguientes atributos y datos de catálogo a la capa actual:

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Atributo/Datos</b> </th> 
   <th class="entry"> <b> Notas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::DefaultExt</span> </p> </td> 
   <td> <p> la extensión predeterminada para todas las rutas de archivos de imagen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Caducidad</span> </p> </td> 
   <td> <p> predeterminado para <span class="codeph"> catálogo::Caducidad</span> o caducidad de la capa actual si no hay ningún registro de catálogo involucrado </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> el perfil de color ICC en funcionamiento, la intención de procesamiento y el indicador de compensación de punto negro para la solicitud y/o la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> se utiliza para todas las rutas de archivos de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> predeterminado para <span class="codeph"> catálogo::Solo resolución</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Anclaje</span> </p> </td> 
   <td> <p> valor predeterminado para el valor <span class="codeph"> anchor=</span> de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Caducidad</span> </p> </td> 
   <td> <p> el valor de caducidad más pequeño de todas las capas se utiliza como valor de tiempo de vida de la imagen de respuesta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::IccProfile</span> </p> </td> 
   <td> <p> el perfil de color de la imagen de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Map</span> </p> </td> 
   <td> <p> los datos del mapa de imagen para la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::MaskPath</span> </p> </td> 
   <td> <p> predeterminado para <span class="codeph"> mask=</span> para la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Modificador</span> </p> </td> 
   <td> <p> comandos de prefijo para la capa actual (cada comando del <span class="codeph"> catálogo::Modificador</span> se puede anular con el mismo comando de la URL, si se especifica para la misma capa) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Path</span> </p> </td> 
   <td> <p> el archivo de imagen de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::PostModifier</span> </p> </td> 
   <td> <p> los comandos postfix de la capa actual (similar a <span class="codeph"> catálogo::Modificador</span>, pero los comandos de <span class="codeph"> catálogo::PostModifier</span> anulan los mismos comandos especificados en la URL o en el <span class="codeph"> catálogo::Modificador</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Resolución</span> </p> </td> 
   <td> <p> la resolución de objeto de la capa actual </p> </td> 
  </tr> 
 </tbody> 
</table>

Dentro de la misma capa, `src=` y `mask=` debe hacer referencia al mismo catálogo de imágenes (si existe).

Un catálogo identificado en un `icc=` comando solo se utiliza para buscar una entrada de la tabla de perfil ICC del catálogo. No hay otros atributos o datos de catálogo involucrados.

Si ` *`rootId`*` se resuelve en un catálogo y ` *`objId`*` coincide con un `catalog::Id` en este catálogo, ` *`rootId/objId`*` se reemplaza efectivamente por la entrada del catálogo de este modo:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Véase también {#section-00e4f6b39cd14244bcce537a3f831259}

[Referencia](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)del catálogo de imágenes, [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
