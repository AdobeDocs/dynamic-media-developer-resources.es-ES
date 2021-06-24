---
description: Tipo de solicitud. Especifica el tipo de solicitud.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 3%

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
   <td colname="col2"> <p> Devuelve cualquier error relacionado con la renderización del fxg con los modificadores de url proporcionados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contenido</span> </p> </td> 
   <td colname="col2"> <p> Devuelve una lista xml de todos los elementos con un valor de atributo <span class="codeph"> s7:element</span> y una lista de todas las páginas del documento fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Devuelve la lista XML de los elementos <span class="codeph"> &lt;RichText/&gt;</span> que están desbordados. </p> <p>Devuelve una lista xml de elementos <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> que se han desbordado para su procesamiento en el lado del cliente. Solo se devolverán los elementos <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> que estén desbordados. <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> elemento es un  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> atributo obligatorio al utilizar  <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. No aparece en la lista ningún elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> desbordado que no tenga <span class="+ topic/ph pr-d/codeph codeph"> s7:element</span>. Cada elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> de la lista tiene el elemento <span class="+ topic/ph pr-d/codeph codeph"> s7:element</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> y el cuadro delimitador del marco de texto desbordado. El atributo <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indica el índice de texto del artículo hasta el cual el texto pudo ajustarse en el marco. <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatusonly se aplica a los  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos del FXG solicitado. No enumerará ningún elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> de ningún FXG incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=existe[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificador único de solicitud reqId </p> <p>Devuelve una sola propiedad denominada catalogRecord.exists. El valor de la propiedad se establece en "1" si la entrada de catálogo especificada existe en la imagen o en el catálogo predeterminado; de lo contrario, se establece en "0". las solicitudes req=exists en el contexto /is/content indicarán la presencia o ausencia de un registro especificado en el catálogo de contenido estático. </p> </td> 
  </tr> 
 </tbody> 
</table>
