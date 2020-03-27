---
description: El servicio de imágenes proporciona un mecanismo para traducir los identificadores de objeto externos a los ID de objeto (catálogo) específicos de la configuración regional. La aplicación principal es para proporcionar contenido y contenido específicos de la configuración regional que se comparten entre varias configuraciones regionales sin que la aplicación cliente necesite conocer los ID de objeto específicos de la configuración regional.
seo-description: El servicio de imágenes proporciona un mecanismo para traducir los identificadores de objeto externos a los ID de objeto (catálogo) específicos de la configuración regional. La aplicación principal es para proporcionar contenido y contenido específicos de la configuración regional que se comparten entre varias configuraciones regionales sin que la aplicación cliente necesite conocer los ID de objeto específicos de la configuración regional.
seo-title: Traslación de ID de objeto
solution: Experience Manager
title: Traslación de ID de objeto
topic: Scene7 Image Serving - Image Rendering API
uuid: 8b4c2f44-033a-428a-b505-af389865c70a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Traslación de ID de objeto{#object-id-translation}

El servicio de imágenes proporciona un mecanismo para traducir los identificadores de objeto externos a los ID de objeto (catálogo) específicos de la configuración regional. La aplicación principal es para proporcionar contenido y contenido específicos de la configuración regional que se comparten entre varias configuraciones regionales sin que la aplicación cliente necesite conocer los ID de objeto específicos de la configuración regional.

La aplicación se puede escribir utilizando únicamente ID de objeto globales y el servicio de imágenes sustituirá automáticamente las imágenes específicas de la configuración regional y otro contenido cuando esté disponible.

El *`locale`* se especifica en las solicitudes de servicio de imágenes con el `locale=` comando.

>[!NOTE]
>
>La traducción de ID de objeto solo se aplica al uso basado en catálogo del servicio de imágenes. Los nombres de archivo no se pueden traducir.

## Ámbito {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Todas las referencias a las entradas de los catálogos de contenido estático, SVG y de imagen se tienen en cuenta para las fuentes de traducción y las referencias de perfil ICC no se traducen. Además de *`object`* en la ruta de [!DNL /is/image] y [!DNL /is/static requests], estos comandos y atributos del catálogo están sujetos a la traducción de ID: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage`y `attribute::Watermark`.

## El mapa de traducción de ID {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` define las reglas utilizadas por el servidor para determinar el ID del contenido localizado, dado como entradas el ID de objeto genérico y el `locale=` valor.

`attribute::LocaleMap` consiste en una lista de *configuraciones regionales* de entrada (que coinciden con los valores especificados con `locale=`), cada una con ninguno o más sufijos de configuración regional de salida ( ` *`locSuffixes`*`).

Por ejemplo, `attribute::LocaleMap` puede tener este aspecto:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

La solicitud `/is/image/myCat/myImg?locale=de_de` devolverá la imagen asociada con la entrada de catálogo `myCat/myImg_D` (suponiendo que existe dicha entrada de catálogo).

Consulte la descripción de `attribute::LocaleMap` para obtener más información.

## El proceso de traducción {#section-1f64db17e9f644d88e09853670e14a16}

Dado el ejemplo anterior, el servidor busca primero el *`locale`* &quot; `de_de`&quot; en el mapa de traducción de ID. A continuación, se repite sobre el *`locSuffixes`* elemento asociado a esta entrada, en este caso &quot; `_D`&quot; y &quot;&quot; (sufijo vacío). Para cada iteración, el sufijo se anexa al ID de imagen y el ID resultante se prueba para que exista en el catálogo. Si se encuentra, se utiliza esa entrada de catálogo; de lo contrario, se prueba la siguiente. En este ejemplo, estas entradas están marcadas: `myCat/myImg_D`, y `myCat/myImg`. Si no se encuentra ninguna coincidencia, el servidor devuelve un error o una imagen predeterminada (si está configurada).

## Localizaciones desconocidas {#section-b2f3c83f2dc845d69b5908107b775537}

En el ejemplo anterior, `attribute::LocaleMap` incluye un vacío *`locale`* que define la regla de traducción predeterminada, utilizada para valores desconocidos `locale=` (es decir, aquellos que no aparecen explícitamente en el mapa de traducción). Si este mapa de traducción se aplicara a la solicitud `/is/image/myCat/myImg?locale=ja`, se resolvería `myCat/myImg_E`, si existe, o de otro modo `myCat/myImg`.

Si un mapa de traducción no especifica una regla de traducción predeterminada, se mostrará un error en todas las solicitudes con `locale=` valores desconocidos.

## Ejemplos {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Búsqueda de varios niveles**

A menudo es deseable agrupar configuraciones regionales (por ejemplo, europeas, de Oriente Medio y norteamericanas) para abordar estándares regionales. Esto se puede lograr con una búsqueda de varios niveles.

Para este ejemplo, queremos admitir colecciones para uso en Occidente y Oriente Medio. Ambas colecciones se basan en la colección de imágenes genéricas y ambas añaden o modifican ciertas imágenes. Both collections are then further refined for specific locales ( `m1`, `m2` for two middle-eastern variants, and `w1`, `w2`, and `w3` for three Western locales), except that images are shared for `w1` and `w3`. Las configuraciones regionales desconocidas solo se asignan a la colección genérica y no tienen acceso a las imágenes específicas de configuración regional.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

La siguiente tabla ilustra las entradas de catálogo que se tendrán en cuenta y el orden en el que se tienen en cuenta para el ID de entrada genérico `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>ID de catálogo que se buscarán</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>todos los demás </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Buscar ID específicos**

Es posible que algunas convenciones de nomenclatura de imágenes no admitan los ID de imagen genéricos internamente. Los ID genéricos de la solicitud siempre deben asignarse a un ID específico del catálogo; a menudo puede que no se conozca la ID específica exacta.

En este ejemplo, las imágenes para todos los idiomas pueden tener `_1`, `_2`o `_3` sufijo. Las imágenes específicas de las configuraciones regionales francesas pueden tener `_22` o `_23` sufijo, y las imágenes específicas de las configuraciones regionales alemanas pueden tener `_470` o `_480` sufijo.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

La siguiente tabla ilustra qué entradas de catálogo se consideran y el orden en que se consideran para el ID de entrada genérico `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>ID de salida para buscar</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>todos los demás </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Véase también {#section-05893816c66a406d89f9bfd6ace8d47a}

[atributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [atributo::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
