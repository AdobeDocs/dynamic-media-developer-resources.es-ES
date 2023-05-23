---
description: Las funciones y sintaxis de los catálogos de imágenes se describen en esta sección.
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

Las funciones y sintaxis de los catálogos de imágenes se describen en esta sección.

Los catálogos de imágenes ofrecen las siguientes funciones:

* Permite la asociación persistente de imágenes con determinados metadatos y comandos modificadores.

   Se hace referencia a las entradas de los catálogos de imágenes mediante una notación de acceso directo `*`rootId/objId`*`, donde `*`rootId`*` identifica el catálogo de imágenes y `*`objId`*` identifica un registro de datos en el catálogo.
* Proporcione valores predeterminados para determinados atributos de solicitud, como la calidad del JPEG o si se va a aplicar una marca de agua.
* Administrar fuentes, perfiles ICC, definiciones de macros y plantillas de solicitudes

Aunque no se haya definido ningún catálogo de imágenes específico, todas las funciones de los catálogos de imágenes están disponibles a través del catálogo predeterminado ( [!DNL default.ini]).

If `*`rootId`*` en la ruta URL de la solicitud, la ruta coincide `attribute::RootId` de un catálogo de imágenes específico, ese catálogo se convierte en el catálogo principal para esta solicitud. El catálogo principal proporciona los atributos y la configuración predeterminados para toda la solicitud. Si no se encuentra ninguna coincidencia, se utiliza el catálogo predeterminado en su lugar.

Un catálogo identificado en una `src=` o `mask=` proporciona los siguientes atributos de catálogo y datos a la capa actual:

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Atributo/Datos</b> </th> 
   <th class="entry"> <b> Notas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> la extensión predeterminada para todas las rutas de archivo de imagen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Caducidad</span> </p> </td> 
   <td> <p> predeterminado para <span class="codeph"> catalog::Expiration</span> o la caducidad de la capa actual si no hay ningún registro de catálogo implicado </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> el perfil de color ICC en funcionamiento, la intención de procesamiento y el indicador de compensación de punto negro para la solicitud o la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> se utiliza para todas las rutas de archivos de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> predeterminado para <span class="codeph"> catalog::Resolution</span> solamente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> predeterminado para <span class="codeph"> anchor=</span> valor de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> </p> </td> 
   <td> <p> el valor de caducidad más pequeño de todas las capas se utiliza como valor de tiempo de vida de la imagen de respuesta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> el perfil de color de la imagen de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map</span> </p> </td> 
   <td> <p> los datos de mapa de imagen para la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> predeterminado para <span class="codeph"> mask=</span> para la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modificador</span> </p> </td> 
   <td> <p> comandos prefix para la capa actual (cada comando en <span class="codeph"> catalog::Modificador</span> puede ser anulado por el mismo comando en la dirección URL, si se especifica para la misma capa) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> el archivo de imagen de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> comandos postfix para la capa actual (similar a <span class="codeph"> catalog::Modificador</span>, pero comandos en <span class="codeph"> catalog::PostModifier</span> anule los mismos comandos especificados en la dirección URL o en <span class="codeph"> catalog::Modificador</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> la resolución del objeto de la capa actual </p> </td> 
  </tr> 
 </tbody> 
</table>

Dentro de la misma capa, `src=` y `mask=` debe hacer referencia al mismo catálogo de imágenes (si lo hay).

Un catálogo identificado en una `icc=` El comando solo se utiliza para buscar una entrada de la tabla de perfil ICC del catálogo. No hay otros datos o atributos de catálogo implicados.

Si, `*`rootId`*` se resuelve en un catálogo y `*`objId`*` coincide con un `catalog::Id` en este catálogo, `*`rootId/objId`*` se ha sustituido efectivamente por la entrada de catálogo de esta manera:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Véase también {#section-00e4f6b39cd14244bcce537a3f831259}

[Referencia de catálogo de imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
