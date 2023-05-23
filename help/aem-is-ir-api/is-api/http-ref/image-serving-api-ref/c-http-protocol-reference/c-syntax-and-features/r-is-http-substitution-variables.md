---
description: Las variables de sustitución se utilizan para transferir valores desde la dirección URL de la solicitud a plantillas de composición almacenadas en catálogos de imágenes. Las variables también se pueden utilizar para transmitir el mismo valor a diferentes lugares de una solicitud compleja.
solution: Experience Manager
title: Variables de sustitución
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Variables de sustitución{#substitution-variables}

Las variables de sustitución se utilizan para transferir valores desde la dirección URL de la solicitud a plantillas de composición almacenadas en catálogos de imágenes. Las variables también se pueden utilizar para transmitir el mismo valor a diferentes lugares de una solicitud compleja.

` $ *`var`*= *`valor`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor en el que se va a establecer la variable (cadena). </p> </td> 
 </tr> 
</table>

Las definiciones y referencias de variables pueden producirse en la parte de consulta de la solicitud, en `catalog::Modifier`, y en `catalog::PostModifier`.

Las variables se definen como se ha indicado anteriormente, de forma similar a otros comandos IS; el &#39;$&#39; inicial identifica el comando como una definición de variable. Se deben definir las variables antes de hacer referencia a ellas.

El nombre de la variable *`var`* no distingue entre mayúsculas y minúsculas y puede consistir en cualquier combinación de letras ASCII, números, &#39;-&#39;, &#39;_&#39; y &#39;.&#39;.

>[!NOTE]
>
>*`value`* debe tener codificación URL de un solo paso para la transmisión HTTP segura. La codificación doble es necesaria si *`value`* se retransmite mediante HTTP. Este es el caso cuando *`value`* se sustituye en una solicitud externa anidada o en el atributo href de un SVG `<image>` Elemento.

Las referencias de variable consisten en el nombre de variable delimitado por &#39;$&#39; ($) al principio y al final *var*$). Las referencias pueden producirse en cualquier parte de la porción de valor de cualquier comando IS (es decir, entre el signo &quot;=&quot; después del nombre del comando y el signo &quot;&amp;&quot; o el final de la solicitud). Las variables personalizadas no se pueden aplicar al `layer=` y `effect=` comandos. Se permiten varias variables en el mismo valor de comando. El servidor sustituye cada incidencia de ` $ *`var`*$` con *`value`*.

Las referencias de variables no pueden estar anidadas. Cualquier incidencia de ` $ *`var`*$` dentro *`value`* no se sustituyen.

Por ejemplo, el fragmento de solicitud:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

se resuelve en:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$$&#39; no es un carácter reservado; de lo contrario, puede aparecer en la solicitud. Por ejemplo, `src=my$image$file.tif` es un comando válido (suponiendo que una entrada de catálogo o un archivo de imagen llamado `my$image$file.tif` existe), mientras que `wid=$number$` no es, porque `wid` requiere un argumento numérico.

## Procesamiento de variables en solicitudes anidadas {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` Las referencias pueden producirse en cualquier lugar dentro de las llaves de una solicitud de servicio o procesamiento de imágenes anidada, incluso a la izquierda de &quot;?&quot; separar la ruta de la consulta. El servidor sustituye estas referencias por valores (desde la dirección URL o desde `catalog::Modifier` del catálogo de imágenes principal) antes de seguir analizando y procesando la solicitud anidada.

Además, todas las ` $ *`var`*=` definiciones de la dirección url o `catalog::Modifier` se reenvían a todas las solicitudes anidadas de servicio y procesamiento de imágenes. Esto garantiza que todas las definiciones de variables estén disponibles para todas las plantillas, independientemente del nivel de anidamiento.

Independientemente del nivel de anidamiento, solo se debe aplicar la codificación HTTP de un solo paso a los valores de variable que se van a sustituir en cualquier lugar de las solicitudes anidadas de procesamiento de imágenes o servicio de imágenes o sus solicitudes asociadas `catalog::Modifier` cadenas.

## Procesamiento de variables en solicitudes externas incrustadas {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` las referencias que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes. Esto permite colocar solicitudes externas incrustadas en una plantilla de un catálogo de imágenes.

Los valores de variable que se sustituyen en solicitudes externas suelen ser de codificación doble, ya que no se aplica ninguna recodificación antes de que el servidor intente transmitir la dirección URL externa final.

## Procesamiento de variables en archivos de SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` las referencias pueden producirse en archivos de SVG en valores de atributo y en `<text>` cadenas. El servicio de imágenes los sustituye por el correspondiente ` $ *`var`*=` definiciones conocidas en el nivel de anidamiento de solicitud en el que se especifica el archivo SVG.

>[!NOTE]
>
>Cualquier valor de variable que deba sustituirse por un `href` el valor del atributo debe tener codificación URL doble; todos los demás deben tener codificación individual.

## Variable de ruta predefinida {#section-930d0dd12e8f49499becc9fe8df24092}

El *`object`* especificado en la ruta de solicitud se asigna a la variable predefinida `*`$object`*`. &#39; ` $ *`objeto`*$`&#39; puede colocarse en cualquier lugar de la solicitud, en la plantilla a la que hace referencia la solicitud o en una solicitud anidada o incrustada en la que dicho objeto esté permitido, incluido el valor de `src=` y `mask=`y la ruta de una solicitud anidada o incrustada.

Por ejemplo, la siguiente solicitud reutilizará la imagen especificada en la ruta como origen de una capa en una solicitud anidada:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Esto equivale a

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

La definición de `*`$object`*` se puede sobrescribir especificando explícitamente ` $ *`objeto`*=` con el valor deseado.

La variable de ruta predefinida se utiliza comúnmente junto con `template=`.

## Predeterminado {#section-b02483d15529444586a2e9504805b155}

Ninguno. El servidor solo sustituye las variables que se han definido (excepto la variable de ruta predefinida $object, que siempre se sustituirá). Cualquier incidencia de ` $ *`var`*$` permanecer literal si `*`var`*`no coincide con una definición de variable existente.

## Ejemplos {#section-fba9393df6984247b7e30b3f93992e86}

Consulte &quot;Ejemplo A&quot; en [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Véase también {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
