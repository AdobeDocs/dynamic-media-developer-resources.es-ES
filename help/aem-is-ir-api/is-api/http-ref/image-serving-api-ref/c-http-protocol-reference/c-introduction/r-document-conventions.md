---
description: Este documento utiliza las siguientes convenciones.
solution: Experience Manager
title: Convenciones de los documentos
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# Convenciones de documento{#document-conventions}

Este documento utiliza las siguientes convenciones.

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>literal </p> </td> 
  <td class="stentry"> <p>En las secciones de sintaxis, el texto no en cursiva es literal. Esta regla no se aplica al espacio en blanco y a los símbolos [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>En las secciones descriptivas, el texto no cursiva entre comillas simples es literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parámetro </span> </p> </td> 
  <td class="stentry"> <p>La letra en cursiva indica una variable o parámetro que se va a sustituir por un valor real. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> command=  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con un final '=' hace referencia a un comando de protocolo HTTP de servicio de imágenes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> atributo::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> atributo: </span> hace referencia a un atributo de catálogo de imágenes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catálogo::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> catálogo: </span> hace referencia a un campo de datos del catálogo de imágenes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> icc: </span> hace referencia a un campo en el mapa de perfiles de color ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> font::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> font: </span> hace referencia a un campo del mapa de fuentes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro: Elemento  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> macro: </span> hace referencia a un campo de la tabla de definición de macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conjunto de reglas::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> conjunto de reglas: </span> hace referencia a un elemento de un conjunto de reglas de preprocesamiento de URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> predeterminado::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> predeterminado: </span> hace referencia a un atributo del catálogo de imágenes predeterminado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [  <span class="varname"> opcional  </span>]  </span> </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis opcionales se incluyen entre corchetes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[  <span class="varname"> opcional  </span>]  </span> </p> </td> 
  <td class="stentry"> <p>El elemento de sintaxis <span class="varname"> opcional </span> se puede repetir ninguna o más veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item1  </span>|  <span class="varname"> elemento2  </span> </span> </p> </td> 
  <td class="stentry"> <p>Una barra vertical indica que se puede utilizar el elemento de sintaxis único a la izquierda o el elemento a la derecha. Se debe seleccionar exactamente un elemento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> {  <span class="varname"> group  </span>}  </span> </p> </td> 
  <td class="stentry"> <p>Las llaves se utilizan para agrupar los elementos de sintaxis. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{  <span class="varname"> group  </span>}  </span> </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis del grupo se pueden repetir una o más veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>espacio en blanco </p> </td> 
  <td class="stentry"> <p>No se permiten espacios en blanco (espacios o pestañas) en las solicitudes HTTP. Este documento utiliza ocasionalmente espacios en blanco entre elementos sintácticos solo para mayor claridad. </p> </td> 
 </tr> 
</table>

