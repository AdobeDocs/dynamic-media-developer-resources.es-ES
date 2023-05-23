---
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos. Las macros se definen en archivos de definición de macros independientes, que se pueden adjuntar a los catálogos de imágenes o al catálogo predeterminado.
solution: Experience Manager
title: Macros de comandos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 1%

---

# Macros de comandos{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos. Las macros se definen en archivos de definición de macros independientes, que se pueden adjuntar a los catálogos de imágenes o al catálogo predeterminado.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Nombre de la macro. </p></td> 
 </tr> 
</table>

`*`name`*` no distingue entre mayúsculas y minúsculas y puede consistir en cualquier combinación de letras ASCII, números , &#39;-&#39;, &#39;_&#39; y &#39;.&#39; caracteres.

Las macros pueden invocarse en cualquier lugar de una solicitud después de &quot;?&quot;, así como en cualquier lugar dentro de un `catalog::Modifier` o `catalog::PostModifier` field. Las macros solo pueden representar uno o más comandos completos del servicio de imágenes y deben separarse de otros comandos con separadores &quot;&amp;&quot;.

Las invocaciones a macros se sustituyen por sus cadenas de sustitución al principio del análisis. Los comandos dentro de las macros anularán los mismos comandos de la solicitud si se producen antes de la invocación de la macro en la solicitud. Esto es diferente a `catalog::Modifier`, donde los comandos de la cadena de solicitud siempre anulan los comandos de `catalog::Modifier` cadena, independientemente de la posición en la solicitud.

Las macros de comandos no pueden tener valores de argumento, pero se pueden utilizar variables personalizadas para pasar valores de la solicitud a la macro.

Las macros pueden anidarse con la siguiente restricción: sólo se puede invocar una macro si ya está definida en el momento de analizar la definición de la macro, ya sea apareciendo anteriormente en el mismo archivo de definición de macro o colocando la definición de dicha macro incrustada en el archivo de definición de macro predeterminado.

## Ejemplo {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Las macros pueden resultar útiles si se van a aplicar los mismos atributos a imágenes diferentes.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Podemos definir una macro para los atributos comunes:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

La macro se usaría de la siguiente manera:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Desde `wid=` es diferente para la tercera solicitud, simplemente anulamos el valor *después* se invoca la macro (especificando `wid=`*antes* `$view$` no tendría ningún efecto).

## Véase también {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalog::Modificador](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [Referencia de definición de macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
