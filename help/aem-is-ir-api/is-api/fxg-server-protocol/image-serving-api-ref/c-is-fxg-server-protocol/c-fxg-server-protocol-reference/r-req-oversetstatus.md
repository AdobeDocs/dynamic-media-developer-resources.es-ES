---
title: req
description: Tipo de solicitud. Especifica el tipo de solicitud.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# req{#req}

Tipo de solicitud. Especifica el tipo de solicitud.

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Valor </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> validar</span> </p> </td> 
   <td colname="col2"> <p> Devuelve cualquier error al procesar el fxg con los modificadores de URL proporcionados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contenido</span> </p> </td> 
   <td colname="col2"> <p> Devuelve la lista xml de todos los elementos con un valor de atributo s7:element<span class="codeph"> de </span> y una lista de todas las páginas del documento fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> estado de sobrescritura</span> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista XML de los cuales <span class="codeph"> elementos &lt;RichText/&gt;</span> están desbordados. </p> <p>Devuelve una lista xml de <span class="+ topic/ph pr-d/codeph codeph"> elementos &lt;RichText/&gt;</span> que se han desbordado para su procesamiento en el lado del cliente. Solo se devuelven <span class="+ topic/ph pr-d/codeph codeph"> elementos &lt;RichText/&gt;</span> que estén desbordados. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementd</span> es un atributo &lt;RichText/&gt;<span class="+ topic/ph pr-d/codeph codeph"> </span> necesario al usar <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. No aparece ningún elemento &lt;RichText/&gt;<span class="+ topic/ph pr-d/codeph codeph"> de </span> desbordado sin <span class="+ topic/ph pr-d/codeph codeph"> s7:elementd</span>. Cada elemento &lt;RichText/&gt;<span class="+ topic/ph pr-d/codeph codeph"> de </span> de la lista tiene <span class="+ topic/ph pr-d/codeph codeph"> s7:elementd</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> y el cuadro delimitador del marco de texto desbordado. El atributo s7:endCharIndex<span class="+ topic/ph pr-d/codeph codeph"> de </span> indica el índice de texto del artículo hasta el cual el texto cabía en el marco. El <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> solo se aplica a <span class="+ topic/ph pr-d/codeph codeph"> elementos &lt;RichText/&gt;</span> en el FXG solicitado. No enumera ningún elemento &lt;RichText/&gt;<span class="+ topic/ph pr-d/codeph codeph"> de </span> de ningún FXG incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificador único de solicitud reqId </p> <p>Devuelve una sola propiedad denominada catalogRecord.exists. El valor de la propiedad se establece en "1" si la entrada de catálogo especificada existe en la imagen o en el catálogo predeterminado; de lo contrario, se establece en "0". req=exists indica la presencia o ausencia de un registro especificado en el catálogo de contenido estático. </p> </td> 
  </tr> 
 </tbody> 
</table>
