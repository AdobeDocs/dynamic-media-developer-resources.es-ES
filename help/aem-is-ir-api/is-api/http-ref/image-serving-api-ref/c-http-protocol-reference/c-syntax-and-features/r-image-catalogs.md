---
description: Las características y la sintaxis de los catálogos de imágenes se describen en esta sección.
solution: Experience Manager
title: Catálogos de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# Catálogos de imágenes{#image-catalogs}

Las características y la sintaxis de los catálogos de imágenes se describen en esta sección.

Los catálogos de imágenes ofrecen las siguientes funciones:

* Permita la asociación persistente de imágenes con determinados comandos de modificador y metadatos.

   Se hace referencia a las entradas de los catálogos de imágenes mediante una notación de método abreviado `*`rootId/objId`*`, donde `*`rootId`*` identifica el catálogo de imágenes y `*`objId`*` identifica un registro de datos en el catálogo.
* Proporcione valores predeterminados para ciertos atributos de solicitud, como la calidad del JPEG o si se va a aplicar una marca de agua.
* Administrar fuentes, perfiles ICC, definiciones de macro y plantillas de solicitud

Aunque no se definan catálogos de imágenes específicos, todas las funciones de los catálogos de imágenes están disponibles a través del catálogo predeterminado ( [!DNL default.ini]).

If `*`rootId`*` en la ruta de URL de la solicitud coincide con `attribute::RootId` de un catálogo de imágenes específico, ese catálogo se convierte en el catálogo principal para esta solicitud. El catálogo principal proporciona los atributos y la configuración predeterminados para toda la solicitud. Si no se encuentra ninguna coincidencia, se utiliza el catálogo predeterminado en su lugar.

Un catálogo identificado en un `src=` o `mask=` proporciona los siguientes atributos y datos de catálogo a la capa actual:

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
   <td> <p> <span class="codeph"> atributo::Icc*</span> </p> </td> 
   <td> <p> el perfil de color ICC de trabajo, la intención de procesamiento y el indicador de compensación de punto negro para la solicitud o la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::RootPath</span> </p> </td> 
   <td> <p> se utiliza para todas las rutas de archivos de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo:Resolution</span> </p> </td> 
   <td> <p> predeterminado para <span class="codeph"> catálogo::Resolution</span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Anchor</span> </p> </td> 
   <td> <p> de forma predeterminada para la variable <span class="codeph"> anchor=</span> valor de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Caducidad</span> </p> </td> 
   <td> <p> el menor valor de caducidad de todas las capas se utiliza como valor de tiempo de vida de la imagen de respuesta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::IccProfile</span> </p> </td> 
   <td> <p> el perfil de color de la imagen de origen para la capa actual </p> </td> 
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
   <td> <p> <span class="codeph"> catálogo::Modifier</span> </p> </td> 
   <td> <p> comandos prefix para la capa actual (cada comando de <span class="codeph"> catálogo::Modifier</span> se puede anular con el mismo comando en la dirección URL, si se especifica para la misma capa) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Path</span> </p> </td> 
   <td> <p> el archivo de imagen de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::PostModifier</span> </p> </td> 
   <td> <p> comandos postfix para la capa actual (similar a <span class="codeph"> catálogo::Modifier</span>, pero los comandos de <span class="codeph"> catálogo::PostModifier</span> anule los mismos comandos especificados en la dirección URL o en <span class="codeph"> catálogo::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Resolution</span> </p> </td> 
   <td> <p> la resolución de objeto de la capa actual </p> </td> 
  </tr> 
 </tbody> 
</table>

Dentro de la misma capa, `src=` y `mask=` debe hacer referencia al mismo catálogo de imágenes (si lo hay).

Un catálogo identificado en un `icc=` solo se utiliza para buscar una entrada de la tabla de perfiles ICC del catálogo. No se incluyen otros atributos o datos de catálogo.

Si, `*`rootId`*` se resuelve en un catálogo y `*`objId`*` coincide con un `catalog::Id` en este catálogo, luego `*`rootId/objId`*` se reemplaza efectivamente por la entrada de catálogo de este modo:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Véase también {#section-00e4f6b39cd14244bcce537a3f831259}

[Referencia del catálogo de imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
