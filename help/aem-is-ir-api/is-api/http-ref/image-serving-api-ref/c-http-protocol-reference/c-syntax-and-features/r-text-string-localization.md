---
title: Localización de cadenas de texto
description: La localización de cadenas de texto permite que los catálogos de imágenes contengan varias representaciones específicas de la configuración regional para el mismo valor de cadena.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 3%

---

# Localización de cadenas de texto{#text-string-localization}

La localización de cadenas de texto permite que los catálogos de imágenes contengan varias representaciones específicas de la configuración regional para el mismo valor de cadena.

El servidor devuelve al cliente la representación que coincide con la configuración regional especificada por `locale=`, evitando la localización del lado del cliente y permitiendo que las aplicaciones cambien de configuración regional simplemente enviando el `locale=` con las solicitudes de texto de IS.

## Ámbito {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

La localización de cadenas de texto se aplica a todos los elementos de cadena que incluyen el token de localización ` ^loc= *`locId`*^` en los campos de catálogo siguientes:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Campo de catálogo</b> </th> 
   <th class="entry"> <b>Elemento de cadena en el campo</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>Cualquier subelemento que contenga una cadena traducible (delimitado por cualquier combinación de separadores ',' ';' ':' o el inicio/final del campo). </p> <p> A <span class="codeph"> 0xrrggbb </span> el valor del color al principio de un campo localizable se excluye de la localización y se pasa sin modificaciones. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>Cualquier valor de atributo entre comillas simples o dobles, excepto los valores del atributo <span class="codeph"> coords= </span> y <span class="codeph"> shape= </span> atributos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>El valor de cualquiera <span class="codeph"> objetivo.*.label </span> y <span class="codeph"> objetivo.*.userdata </span> propiedad. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>El valor de cualquier propiedad. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sintaxis de cadena {#section-d12320edf300409f8e17565b143acafc}

Localization-enabled *`string`* los elementos del catálogo de imágenes constan de una o más cadenas localizadas, cada una precedida por un token de localización.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de configuración regional interna para <span class="varname"> localizedString </span> siguiendo esto <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>Cadena localizada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>Cadena que se utilizará para configuraciones regionales desconocidas. </p> </td> 
 </tr> 
</table>

El *`locId`* debe ser ASCII y no puede incluir ^.

El ^ puede aparecer en cualquier parte en subcadenas con o sin codificación HTTP. El servidor coincide con todo el *`localizationToken`* `^loc=locId^` pattern para separar subcadenas.

El *`stringElements`*, que no incluyen al menos uno *`localizationToken`*, no se tienen en cuenta para la localización.

## El mapa de traducción {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` define las reglas que utiliza el servidor para determinar qué *`localizedStrings`* para volver al cliente. Consiste en una lista de entradas *`locales`* (que coinciden con los valores especificados por `locale=`), cada uno con uno o más id de configuración regional internos ( *`locId`*). Por ejemplo:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Empty *`locId`* Los valores indican que la variable *`defaultString`* debe devolverse, si está disponible.

Consulte la descripción de `attribute::LocaleStrMap` para obtener más información.

## El proceso de traducción {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Se proporciona el mapa de traducción de ejemplo anterior y la solicitud `/is/image/myCat/myItem?req=&locale=nl`, el servidor busca primero &quot; `nl`&quot; en el mapa de configuración regional. La entrada coincidente `nl,N` indica que para cada *`stringElement`*, el *`localizedString`* marcado con `^loc=N^` debería devolverse. Si esto *`localizationToken`* no está presente en el *`stringElement`*, se devuelve un valor vacío.

Digamos que... `catalog::UserData` para `myCat/myItem` contiene lo siguiente (saltos de línea insertados para mayor claridad):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

El servidor devolverá lo siguiente en respuesta a la solicitud de ejemplo:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Configuraciones regionales desconocidas {#section-26dfeefbd60345de94bbfeaaf7741223}

En el ejemplo anterior, `attribute::LocaleStrMap` tiene una entrada con un vacío *`locale`* valor. El servidor utiliza esta entrada para gestionar todo `locale=` valores que no se especifican explícitamente de otra manera en el mapa de traducción.

El mapa de traducción de ejemplo especifica que, en tal caso, la variable *`defaultString`* debe devolverse, si está disponible. Por lo tanto, se devuelve lo siguiente si este mapa de traducción se aplica a la solicitud `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Ejemplos {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Familias lingüísticas**

Múltiple *`locId`* Los valores de pueden asociarse con cada *`locale`* en el mapa de traducción. El motivo es que permite admitir variaciones específicas de país o región (por ejemplo, inglés de EE. UU. frente a inglés de Reino Unido) para determinados *`stringElements`* mientras se gestiona la mayoría de los contenidos con configuraciones regionales base comunes (por ejemplo, inglés internacional).

Para el ejemplo, se agrega compatibilidad con el inglés específico de EE. UU. ( `*`locId`* EUS`) e inglés específico del Reino Unido ( `*`locId`* EUK`), para admitir la ortografía alternativa ocasional. Si no existe EUK o EUS, se remonta a E. Del mismo modo, las variantes alemanas específicas de Austria ( `DAT`) podría estar disponible donde sea necesario mientras se devuelve el alemán común *`localizedStrings`* (marcado con `D`) la mayor parte del tiempo.

El `attribute::LocaleStrMap` tendría este aspecto:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

En la tabla siguiente se describen los resultados de algunos elementos representativos *`stringElement`* y *`locale`* combinaciones:

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
   <td> <p> <span class="codeph"> ^loc=E^Inglés^loc=D^Alemán </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>todos los demás </p> </td> 
   <td> <p>Inglés </p> <p>Alemán </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>todos los demás </p> </td> 
   <td> <p>Inglés </p> <p>RU-inglés </p> <p>Alemán </p> <p>austriaco </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> Para este ejemplo, la variable <span class="varname"> locId </span> El DDE no existe en <span class="codeph"> attribute::LocaleStrMap </span>y, por lo tanto, la subcadena asociada a esto <span class="varname"> locId </span> nunca se devuelve. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>todos los demás </p> </td> 
   <td> <p>Inglés </p> <p>inglés estadounidense </p> <p>Alemán </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
