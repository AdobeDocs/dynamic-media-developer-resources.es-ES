---
description: Tipo de solicitud. Especifica el tipo de solicitud.
seo-description: Tipo de solicitud. Especifica el tipo de solicitud.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 4%

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
   <td colname="col2"> <p> Devuelve una lista xml de todos los elementos con un valor de atributo <span class="codeph"> s7:element</span> y una lista de todas las páginas del documento fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista XML cuyos elementos <span class="codeph"> &lt;RichText/&gt;</span> están desbordados. </p> <p>Devuelve una lista xml de <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elementos que están desbordados para su procesamiento en el lado del cliente. Solo se devolverán los elementos <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> que están desbordados. <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> element es un  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> atributo requerido cuando se utiliza  <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. No se muestra ningún elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> desbordado sin <span class="+ topic/ph pr-d/codeph codeph"> s7:element</span>. Cada elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> de la lista tiene el elemento <span class="+ topic/ph pr-d/codeph codeph"> s7:element</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> y el cuadro delimitador del marco de texto desbordado. El atributo <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indica el índice de texto del artículo hasta el cual el texto se pudo ajustar en el marco. <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatussolamente se aplica a  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> los elementos del FXG solicitado. No lista ningún elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> de ningún FXG incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificador único de solicitud reqId </p> <p>Devuelve una sola propiedad denominada catalogRecord.exists. El valor de la propiedad se establece en "1" si la entrada de catálogo especificada existe en la imagen o en el catálogo predeterminado; de lo contrario, se establece en "0". las solicitudes req=exists en el contexto /is/content indican la presencia o ausencia de un registro especificado en el catálogo de contenido estático. </p> </td> 
  </tr> 
 </tbody> 
</table>

