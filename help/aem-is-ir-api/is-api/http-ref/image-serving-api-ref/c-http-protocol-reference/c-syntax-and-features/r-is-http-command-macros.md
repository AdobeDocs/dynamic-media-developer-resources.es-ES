---
title: Macros de comandos
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos. Las macros se definen en archivos de definición de macros independientes, que se pueden adjuntar a los catálogos de imágenes o al catálogo predeterminado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
TQID: 'https://experienceleague.adobe.com/a7vbT8heEkiWfmxn3wPudnzYTRN-H-I5D22038P4mJE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 311
ht-degree: 0%

---

# Macros de comandos{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos. Las macros se definen en archivos de definición de macros independientes, que se pueden adjuntar a los catálogos de imágenes o al catálogo predeterminado.

`$ *`nombre`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nombre</span></span> </p> </td> 
  <td class="stentry"> <p>Nombre de la macro. </p></td> 
 </tr> 
</table>

`*`name`*` no distingue entre mayúsculas y minúsculas y puede contener cualquier combinación de letras ASCII, números, caracteres &quot;-&quot;, &quot;_&quot; y &quot;.&quot;.

Las macros pueden invocarse en cualquier lugar de una solicitud después de &quot;?&quot; y en cualquier lugar dentro de un campo `catalog::Modifier` o `catalog::PostModifier`. Las macros solo pueden representar uno o más comandos completos del servicio de imágenes y deben separarse de otros comandos con separadores de `&`.

Las invocaciones a macros se sustituyen por sus cadenas de sustitución al principio del análisis. Los comandos dentro de las macros anulan los mismos comandos de la solicitud si se producen antes de la invocación de la macro en la solicitud. Este flujo de procesamiento es diferente de `catalog::Modifier`, donde los comandos de la cadena de solicitud siempre anulan los comandos de la cadena `catalog::Modifier`, independientemente de la posición en la solicitud.

Las macros de comandos no pueden tener valores de argumento, pero se pueden utilizar variables personalizadas para pasar valores de la solicitud a la macro.

Las macros pueden estar anidadas. Sin embargo, una macro sólo se puede invocar si ya está definida en el momento de analizar la definición de la macro. Este flujo de trabajo se realiza apareciendo anteriormente en el mismo archivo de definición de macro o colocando la definición de dicha macro incrustada en el archivo de definición de macro predeterminado.

## Ejemplo {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Las macros pueden resultar útiles si se van a aplicar los mismos atributos a imágenes diferentes.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Puede definir una macro para los atributos comunes:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

La macro se usaría de la siguiente manera:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Dado que `wid=` es diferente para la tercera solicitud, simplemente puede anular el valor *después de* de que se invoque la macro (especificando `wid=`*antes de* `$view$` no tiene ningún efecto).

## Véase también {#section-8cdba0ed2480444ca61e719e54f8871c}

[catálogo::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catálogo::Modificador](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [Referencia de definición de macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
