---
description: Las variables de sustitución se utilizan para transferir valores desde la dirección URL de la solicitud a la composición de plantillas almacenadas en catálogos de imágenes. Las variables también se pueden utilizar para transmitir el mismo valor a diferentes lugares de una solicitud compleja.
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

Las variables de sustitución se utilizan para transferir valores desde la dirección URL de la solicitud a la composición de plantillas almacenadas en catálogos de imágenes. Las variables también se pueden utilizar para transmitir el mismo valor a diferentes lugares de una solicitud compleja.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de la variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor al que se debe configurar la variable (cadena). </p> </td> 
 </tr> 
</table>

Las definiciones y referencias de variables pueden producirse en la parte de consulta de la solicitud, en `catalog::Modifier`y en `catalog::PostModifier`.

Las variables se definen como se indica arriba, de forma similar a otros comandos IS; el elemento principal &#39;$&#39; identifica el comando como una definición de variable. Las variables deben definirse antes de hacer referencia a ellas.

El nombre de la variable *`var`* no distingue entre mayúsculas y minúsculas y puede consistir en cualquier combinación de letras ASCII, números, &#39;-&#39;, &#39;_&#39; y &#39;.&#39;.

>[!NOTE]
>
>*`value`* debe tener codificación de dirección URL de paso único para la transmisión HTTP segura. Se requiere una codificación doble si *`value`* se retransmite mediante HTTP. Este es el caso cuando *`value`* se sustituye en una solicitud externa anidada o en el atributo href de un SVG `<image>` elemento.

Las referencias de variables constan del nombre de variable delimitado por &#39;$&#39; inicial y final ($)*var*$). Las referencias pueden producirse en cualquier parte de la porción de valor de cualquier comando IS (es decir, entre el &#39;=&#39; después del nombre del comando y el &#39;&amp;&#39; posterior o el final de la solicitud). Las variables personalizadas no se pueden aplicar a la variable `layer=` y `effect=` comandos. Se permiten varias variables en el mismo valor de comando. El servidor sustituye cada incidencia de ` $ *`var`*$` con *`value`*.

Es posible que las referencias de variables no estén anidadas. Cualquier ocurrencia de ` $ *`var`*$` en *`value`* no se sustituyen.

Por ejemplo, el fragmento de solicitud:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

resuelve en:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; no es un carácter reservado; de lo contrario, podría ocurrir en la solicitud. Por ejemplo, `src=my$image$file.tif` es un comando válido (suponiendo que una entrada de catálogo o un archivo de imagen denominado `my$image$file.tif` existe), while `wid=$number$` no, porque `wid` requiere un argumento numérico.

## Procesamiento de variables en solicitudes anidadas {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` las referencias pueden producirse en cualquier lugar dentro de las llaves de una solicitud anidada de Image Serving o Image Rendering, incluso a la izquierda de &#39;?&#39; separar la ruta de acceso de la consulta. El servidor sustituye estas referencias por valores (ya sea de la dirección url o de `catalog::Modifier` del catálogo de imágenes principal) antes de seguir analizando y procesando la solicitud anidada.

Además, todas las ` $ *`var`*=` definiciones de la dirección url o `catalog::Modifier` se reenvían a todas las solicitudes anidadas de Image Serving y Image Rendering. Esto garantiza que todas las definiciones de variables estén disponibles para todas las plantillas, independientemente del nivel de anidación.

Independientemente del nivel de anidación, solo se debe aplicar una codificación HTTP de un solo paso a los valores de las variables que se van a sustituir en cualquier lugar de las solicitudes anidadas de Representación de imágenes o Servicio de imágenes o sus correspondientes `catalog::Modifier` cadenas.

## Procesamiento de variables en solicitudes externas incrustadas {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` las referencias que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes. Esto permite colocar las solicitudes externas incrustadas en una plantilla en un catálogo de imágenes.

Los valores de variable que se van a sustituir en solicitudes externas generalmente deben codificarse dos veces, ya que no se aplica ninguna recodificación antes de que el servidor intente transmitir la dirección url externa final.

## Procesamiento de variables en archivos SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` pueden producirse referencias en archivos SVG en valores de atributo y en `<text>` cadenas. El servicio de imágenes los sustituye por la coincidencia ` $ *`var`*=` definiciones conocidas en el nivel de anidación de solicitudes en el que se especifica el archivo SVG.

>[!NOTE]
>
>Cualquier valor de variable que se vaya a sustituir por un `href` el valor de atributo debe tener una codificación URL doble; todos los demás deben codificarse de forma individual.

## Variable de ruta predefinida {#section-930d0dd12e8f49499becc9fe8df24092}

La variable *`object`* especificado en la ruta de solicitud se asigna a la variable predefinida `*`$object`*`. &#39; ` $ *`object`*$`&#39; puede colocarse en cualquier lugar de la solicitud, en la plantilla a la que hace referencia la solicitud o en una solicitud anidada o incrustada en la que se permita dicho objeto, incluido el valor de `src=` y `mask=`y la ruta de una solicitud anidada/incrustada.

Por ejemplo, la siguiente solicitud reutiliza la imagen especificada en la ruta como origen de una capa en una solicitud anidada:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Esto equivale a

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

La definición de `*`$object`*` se puede anular especificando explícitamente ` $ *`object`*=` con el valor deseado.

La variable de ruta predefinida se usa comúnmente junto con `template=`.

## Predeterminado {#section-b02483d15529444586a2e9504805b155}

Ninguno. El servidor solo sustituye las variables que se han definido (excepto la variable de ruta predefinida $object, que siempre se sustituirá). Cualquier ocurrencia de ` $ *`var`*$` permanecer literal si `*`var`*`no se puede comparar con una definición de variable existente.

## Ejemplos {#section-fba9393df6984247b7e30b3f93992e86}

Consulte &quot;Ejemplo A&quot; en [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Véase también {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
