---
description: Este documento describe el catálogo de materiales para el procesamiento de imágenes de Dynamic Media.
seo-description: Este documento describe el catálogo de materiales para el procesamiento de imágenes de Dynamic Media.
seo-title: Introducción
solution: Experience Manager
title: Introducción
uuid: 38da0561-7730-4170-bf29-02de325b3ad9
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---


# Introducción{#introduction}

Este documento describe el catálogo de materiales para el procesamiento de imágenes de Dynamic Media.

**Audiencia prevista**

Esta documentación está dirigida a programadores experimentados y desarrolladores de sitios web que deseen aprovechar Dynamic Media Image Rendering para un sitio web o una aplicación personalizada.

Se da por hecho que el lector está familiarizado con la creación de imágenes y el procesamiento de imágenes de Dynamic Media, las normas y convenciones generales del protocolo HTTP y la terminología básica de las imágenes.

**Convenciones de los documentos**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Literal </p> </td> 
  <td class="stentry"> <p>En las secciones de sintaxis, el texto no en cursiva es literal; esto no se aplica al espacio en blanco y a los símbolos [ ] { } | *. </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> atributo::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo 'attribute::' hace referencia a un atributo de catálogo de imágenes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catálogo::Item  </span> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "catálogo::" hace referencia a un campo de datos de catálogo de material. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "icc::" hace referencia a un campo del mapa de perfiles de color ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "macro::" hace referencia a un campo de la tabla de definición de macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conjunto de reglas::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "conjunto de reglas::" hace referencia a un elemento de un conjunto de reglas de preprocesamiento de URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> predeterminado::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo 'default::' hace referencia a un atributo del catálogo de imágenes predeterminado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> viñeta:Elemento  </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "viñeta::" hace referencia a un campo del mapa de viñetas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> opcional </span> ] </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis opcionales se incluyen entre corchetes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> opcional </span> ] </p> </td> 
  <td class="stentry"> <p>El elemento de sintaxis opcional puede repetirse una o más veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> elemento2  </span> </p> </td> 
  <td class="stentry"> <p>Una barra vertical indica que se puede utilizar el elemento de sintaxis único a la izquierda o el elemento a la derecha. Se debe seleccionar exactamente un elemento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> grupo </span> } </p> </td> 
  <td class="stentry"> <p>Las llaves se utilizan para agrupar los elementos de sintaxis. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> grupo </span> } </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis del grupo se pueden repetir una o más veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Espacio en blanco. </p> </td> 
  <td class="stentry"> <p>No se permiten espacios en blanco (espacios o pestañas) en las solicitudes HTTP. Este documento utiliza ocasionalmente espacios en blanco entre elementos sintácticos solo para mayor claridad. </p> </td> 
 </tr> 
</table>

