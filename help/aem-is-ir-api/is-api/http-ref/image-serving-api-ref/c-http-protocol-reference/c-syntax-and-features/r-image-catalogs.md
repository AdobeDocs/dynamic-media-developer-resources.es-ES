---
description: Las funciones y sintaxis de los catálogos de imágenes se describen en esta sección.
solution: Experience Manager
title: Catálogos de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Catálogos de imágenes{#image-catalogs}

Las funciones y sintaxis de los catálogos de imágenes se describen en esta sección.

Los catálogos de imágenes ofrecen las siguientes funciones:

* Permite la asociación persistente de imágenes con determinados metadatos y comandos modificadores.

  Se hace referencia a las entradas de los catálogos de imágenes mediante una notación de acceso directo `*`rootId/objId`*`, donde `*`rootId`*` identifica el catálogo de imágenes y `*`objId`*` identifica un registro de datos en el catálogo.
* Proporcione valores predeterminados para determinados atributos de solicitud, como la calidad del JPEG o si se va a aplicar una marca de agua.
* Administrar fuentes, perfiles ICC, definiciones de macros y plantillas de solicitudes

Aunque no se haya definido ningún catálogo de imágenes específico, todas las características de los catálogos de imágenes están disponibles mediante el catálogo predeterminado ( [!DNL default.ini]).

Si `*`rootId`*` en la ruta URL de la solicitud coincide con `attribute::RootId` de un catálogo de imágenes específico, ese catálogo se convierte en el catálogo principal para esta solicitud. El catálogo principal proporciona los atributos y la configuración predeterminados para toda la solicitud. Si no se encuentra ninguna coincidencia, se utiliza el catálogo predeterminado en su lugar.

Un catálogo identificado en un comando `src=` o `mask=` proporciona los siguientes datos y atributos de catálogo a la capa actual:

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> atributo/datos</b> </th> 
   <th class="entry"> <b> notas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::DefaultExt</span> </p> </td> 
   <td> <p> la extensión predeterminada para todas las rutas de archivo de imagen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Expiration</span> </p> </td> 
   <td> <p> valor predeterminado para <span class="codeph"> catalog::Expiration</span> o caducidad de la capa actual si no hay ningún registro de catálogo involucrado </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Icc*</span> </p> </td> 
   <td> <p> el perfil de color ICC en funcionamiento, la intención de procesamiento y el indicador de compensación de punto negro para la solicitud o la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::RootPath</span> </p> </td> 
   <td> <p> se utiliza para todas las rutas de archivos de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Resolution</span> </p> </td> 
   <td> <p> valor predeterminado solo para el catálogo <span class="codeph">::Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Anclaje</span> </p> </td> 
   <td> <p> predeterminado para el valor <span class="codeph"> anchor=</span> de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Expiración</span> </p> </td> 
   <td> <p> el valor de caducidad más pequeño de todas las capas se utiliza como valor de tiempo de vida de la imagen de respuesta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::IccProfile</span> </p> </td> 
   <td> <p> el perfil de color de la imagen de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Map</span> </p> </td> 
   <td> <p> los datos de mapa de imagen para la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::MaskPath</span> </p> </td> 
   <td> <p> predeterminado para <span class="codeph"> máscara=</span> para la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Modificador</span> </p> </td> 
   <td> <p> comandos prefix para la capa actual (cada comando del catálogo <span class="codeph">::Modifier</span> puede ser anulado por el mismo comando en la dirección URL, si se especifica para la misma capa) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Path</span> </p> </td> 
   <td> <p> el archivo de imagen de origen de la capa actual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::PostModifier</span> </p> </td> 
   <td> <p> los comandos postfix de la capa actual (similares a <span class="codeph"> catalog::Modifier</span>, pero los comandos del catálogo <span class="codeph">::PostModifier</span> anulan los mismos comandos especificados en la dirección URL o en el catálogo <span class="codeph">::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Resolution</span> </p> </td> 
   <td> <p> la resolución del objeto de la capa actual </p> </td> 
  </tr> 
 </tbody> 
</table>

Dentro de la misma capa, `src=` y `mask=` deben hacer referencia al mismo catálogo de imágenes (si existe).

Un catálogo identificado en un comando `icc=` solo se usa para buscar una entrada de la tabla de perfiles ICC del catálogo. No hay otros datos o atributos de catálogo implicados.

Si `*`rootId`*` se resuelve en un catálogo y `*`objId`*` coincide con un `catalog::Id` en este catálogo, entonces `*`rootId/objId`*` se reemplaza con la entrada del catálogo de esta manera:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Véase también {#section-00e4f6b39cd14244bcce537a3f831259}

[Referencia de catálogo de imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [máscara=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anclaje=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
