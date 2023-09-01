---
title: req
description: Tipo de solicitud. Especifica el tipo de solicitud.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '243'
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
   <td colname="col2"> <p> Devuelve cualquier error al procesar el fxg con los modificadores de URL proporcionados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contenido</span> </p> </td> 
   <td colname="col2"> <p> Devolver lista xml de todos los elementos con una <span class="codeph"> s7:elemento</span> y una lista de todas las páginas del documento de fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> estado de superposición</span> </p> </td> 
   <td colname="col2"> <p>Devuelve una lista XML de la cual <span class="codeph"> &lt;richtext /&gt;</span> elementos están desbordados. </p> <p>Devuelve una lista xml de <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos que se desbordan para procesarse en el lado del cliente. Solo <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> se devuelven los elementos desbordados. El <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> es un obligatorio <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> atributo al usar <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Cualquier desbordamiento <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos sin un <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> no aparece en la lista. Cada <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> de la lista tiene el <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>y el cuadro delimitador del marco de texto desbordado. El <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> El atributo indica el índice de texto en el artículo hasta el cual el texto cabía en el marco. El <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> solo se aplica a <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos en el FXG solicitado. No se muestra ninguna <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos de cualquier FXG incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificador único de solicitud reqId </p> <p>Devuelve una sola propiedad denominada catalogRecord.exists. El valor de la propiedad se establece en "1" si la entrada de catálogo especificada existe en la imagen o en el catálogo predeterminado; de lo contrario, se establece en "0". req=exists indica la presencia o ausencia de un registro especificado en el catálogo de contenido estático. </p> </td> 
  </tr> 
 </tbody> 
</table>
