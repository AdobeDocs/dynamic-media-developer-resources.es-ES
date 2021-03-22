---
description: La localización de cadenas de texto permite que los catálogos de imágenes contengan varias representaciones específicas de la configuración regional para el mismo valor de cadena.
seo-description: La localización de cadenas de texto permite que los catálogos de imágenes contengan varias representaciones específicas de la configuración regional para el mismo valor de cadena.
seo-title: Localización de cadenas de texto
solution: Experience Manager
title: Localización de cadenas de texto
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 3%

---


# Localización de cadena de texto{#text-string-localization}

La localización de cadenas de texto permite que los catálogos de imágenes contengan varias representaciones específicas de la configuración regional para el mismo valor de cadena.

El servidor devuelve al cliente la representación que coincide con la configuración regional especificada con `locale=`, evitando así la localización del lado del cliente y permitiendo que las aplicaciones cambien de configuraciones regionales simplemente enviando el valor `locale=` apropiado con las solicitudes de texto IS.

## Ámbito {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

La localización de cadenas de texto se aplica a todos los elementos de cadena que incluyen el token de localización ` ^loc= *`locId`*^` en los siguientes campos de catálogo:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Campo Catálogo</b> </th> 
   <th class="entry"> <b>Elemento de cadena en el campo</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::ImageSet  </span> </p> </td> 
   <td> <p>Cualquier subelemento que contenga una cadena traducible (delimitado por cualquier combinación de separadores ',' ';' ':' y/o el inicio/final del campo). </p> <p> Un valor de color <span class="codeph"> 0xrrgbb </span> al principio de un campo localizable se excluye de la localización y se transfiere sin modificaciones. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Map  </span> </p> </td> 
   <td> <p>Cualquier valor de atributo entre comillas simples o dobles, excepto los valores de los atributos <span class="codeph"> coords= </span> y <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Targets  </span> </p> </td> 
   <td> <p>El valor de cualquier destinatario <span class="codeph">.Destino *.label </span> y <span class="codeph">.*.userdata </span> propiedad. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::UserData  </span> </p> </td> 
   <td> <p>El valor de cualquier propiedad. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sintaxis de cadena {#section-d12320edf300409f8e17565b143acafc}

Los elementos *`string`* habilitados para la localización del catálogo de imágenes constan de una o más cadenas localizadas, cada una precedida por un token de localización.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de configuración regional interna para el <span class="varname"> localizedString </span> siguiendo este <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Cadena localizada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Cadena que se utilizará para configuraciones regionales desconocidas. </p> </td> 
 </tr> 
</table>

*`locId`* debe ser ASCII y no puede incluir &#39;^&#39;.

&#39;^&#39; puede ocurrir en cualquier parte de subcadenas con o sin codificación HTTP. El servidor coincide con todo el patrón *`localizationToken`* `^loc=locId^` para separar subcadenas.

*`stringElements`* que no incluyen al menos uno no  *`localizationToken`* se tienen en cuenta para la localización.

## El mapa de traducción {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` define las reglas que utiliza el servidor para determinar cuál  *`localizedStrings`* se devolverá al cliente. Consiste en una lista de entrada *`locales`* (que coincide con los valores especificados con `locale=`), cada uno con ninguno o más identificadores de configuración regional internos ( *`locId`*). Por ejemplo:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Los valores *`locId`* vacíos indican que el *`defaultString`* debe devolverse, si está disponible.

Consulte la descripción de `attribute::LocaleStrMap` para obtener más información.

## El proceso de traducción {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Dado el ejemplo de mapa de traducción anterior y la solicitud `/is/image/myCat/myItem?req=&locale=nl`, el servidor busca primero &quot; `nl`&quot; en el mapa de configuración regional. La entrada coincidente `nl,N` indica que para cada *`stringElement`*, debe devolverse el *`localizedString`* marcado con `^loc=N^`. Si este *`localizationToken`* no está presente en el *`stringElement`*, se devuelve un valor vacío.

Supongamos que `catalog::UserData` para `myCat/myItem` contiene lo siguiente (se insertan saltos de línea para una mayor claridad):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

El servidor devolverá lo siguiente en respuesta a nuestra solicitud de ejemplo:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Configuraciones regionales desconocidas {#section-26dfeefbd60345de94bbfeaaf7741223}

En el ejemplo anterior, `attribute::LocaleStrMap` tiene una entrada con un valor *`locale`* vacío. El servidor utiliza esta entrada para gestionar todos los valores `locale=` que no se especifican explícitamente en el mapa de traducción.

El mapa de traducción de ejemplo especifica que, en tal caso, el *`defaultString`* debe devolverse si está disponible. Por lo tanto, se devolverá lo siguiente si este mapa de traducción se aplica a la solicitud `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Ejemplos {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Familias de idiomas**

Se pueden asociar varios valores *`locId`* con cada *`locale`* en el mapa de traducción. Esto permite admitir variaciones específicas del país o la región (por ejemplo, inglés de EE. UU. vs inglés de Reino Unido) para seleccionar *`stringElements`* mientras se gestiona la mayoría de los contenidos con configuraciones regionales de base comunes (por ejemplo, inglés internacional).

Para nuestro ejemplo, queremos agregar compatibilidad con el inglés específico de EE. UU. ( `*`locId`* EUS`) y el inglés específico de Reino Unido ( `*`locId`* EUK`), para admitir la ortografía alternativa ocasional. Si no existen EUK o EUS, volveremos a E. De manera similar, las variantes específicas de Austria para Alemania ( `DAT`) podrían estar disponibles cuando sea necesario mientras se devuelve el alemán común *`localizedStrings`* (marcado con `D`) la mayor parte del tiempo.

`attribute::LocaleStrMap` tendría este aspecto:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

La siguiente tabla describe el resultado de algunas combinaciones *`stringElement`* y *`locale`* representativas:

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>locale</i> </th> 
   <th class="entry"> <p>Cadena de salida </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German  </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>todos los demás </p> </td> 
   <td> <p>Inglés </p> <p>Alemán </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austria  </span> </p> </td> 
   <td> <p> en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>todos los demás </p> </td> 
   <td> <p>Inglés </p> <p>UK-English </p> <p>Alemán </p> <p>Austria </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=es^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> Tenga en cuenta que para este ejemplo el <span class="varname"> locId </span> DDE no existe en el atributo <span class="codeph">::LocaleStrMap </span> y, por lo tanto, nunca se devuelve la subcadena asociada con este <span class="varname"> locId </span>. </p> </td> 
   <td> <p> en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>todos los demás </p> </td> 
   <td> <p>Inglés </p> <p>US-English </p> <p>Alemán </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

