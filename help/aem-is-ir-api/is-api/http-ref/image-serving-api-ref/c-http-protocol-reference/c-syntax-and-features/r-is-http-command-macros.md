---
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos. Las macros se definen en archivos de definición de macro separados, que pueden adjuntarse a catálogos de imágenes o al catálogo predeterminado.
solution: Experience Manager
title: Macros de comandos
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# Macros de comandos{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos. Las macros se definen en archivos de definición de macro separados, que pueden adjuntarse a catálogos de imágenes o al catálogo predeterminado.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Nombre de macro. </p></td> 
 </tr> 
</table>

`*``*` el nombre no distingue entre mayúsculas y minúsculas y puede consistir en cualquier combinación de letras ASCII, números , &#39;-&#39;, &#39;_&#39; y &#39;.&#39; caracteres.

Las macros se pueden invocar en cualquier parte de una solicitud después de &#39;?&#39;, así como en cualquier parte dentro de un campo `catalog::Modifier` o `catalog::PostModifier`. Las macros solo pueden representar uno o más comandos completos de servicio de imágenes y deben separarse de otros comandos con separadores &quot;&amp;&quot;.

Las invocaciones de macro se sustituyen por sus cadenas de sustitución antes de analizar. Los comandos dentro de las macros anulan los mismos comandos en la solicitud si se producen antes de la invocación de macro en la solicitud. Esto es diferente a `catalog::Modifier`, donde los comandos de la cadena de solicitud siempre anulan los comandos de la cadena `catalog::Modifier`, independientemente de la posición en la solicitud.

Las macros de comandos no pueden tener valores de argumento, pero pueden utilizarse variables personalizadas para pasar valores de la solicitud a la macro.

Las macros se pueden anidar, con la siguiente restricción: Una macro solo puede invocarse si ya está definida en el momento en que se analiza la definición de la macro, ya sea al aparecer antes en el mismo archivo de definición de macro o al colocar la definición de dicha macro incrustada en el archivo de definición de macro predeterminada.

## Ejemplo {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Las macros pueden resultar útiles si se van a aplicar los mismos atributos a diferentes imágenes.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Podemos definir una macro para los atributos comunes:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

La macro se utilizaría de la siguiente manera:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Dado que `wid=` es diferente para la tercera solicitud, simplemente anulamos el valor *después* de invocar la macro (especificar `wid=`*antes* `$view$` no tendría ningún efecto).

## Véase también {#section-8cdba0ed2480444ca61e719e54f8871c}

[catálogo::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [catálogo::Modificador](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), Referencia de definición de  [macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
