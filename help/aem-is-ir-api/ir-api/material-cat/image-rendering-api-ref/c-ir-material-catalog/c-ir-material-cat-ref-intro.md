---
description: En este documento se describe el catálogo de materiales para el procesamiento de imágenes de Scene7.
seo-description: En este documento se describe el catálogo de materiales para el procesamiento de imágenes de Scene7.
seo-title: Introducción
solution: Experience Manager
title: Introducción
topic: Scene7 Image Serving - Image Rendering API
uuid: 38da0561-7730-4170-bf29-02de325b3ad9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Introducción{#introduction}

En este documento se describe el catálogo de materiales para el procesamiento de imágenes de Scene7.

**audiencia prevista**

Este documento está dirigido a programadores y desarrolladores de sitios web experimentados que deseen aprovechar el procesamiento de imágenes de Scene7 para un sitio web o una aplicación personalizada.

Se da por hecho que el lector está familiarizado con la creación de imágenes y el procesamiento de imágenes de Scene7, las normas y convenciones generales del protocolo HTTP y la terminología básica de creación de imágenes.

**Convenciones de Documento**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Literal </p> </td> 
  <td class="stentry"> <p>En las secciones de sintaxis, el texto no cursiva es literal; esto no se aplica al espacio en blanco y a los símbolos [ ] { }| *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>En las secciones descriptivas, el texto sin cursiva entre comillas simples es literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parámetro </span> </p> </td> 
  <td class="stentry"> <p>La cursiva indica una variable o parámetro que se va a sustituir por un valor real. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo 'attribute::' hace referencia a un atributo de catálogo de imágenes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catálogo::Item </span> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo 'catálogo::' hace referencia a un campo de datos de catálogo de material. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo 'icc::' hace referencia a un campo en el mapa de perfiles de color ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo 'macro::' hace referencia a un campo de la tabla de definición de macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conjunto de reglas::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo 'ruleset::' hace referencia a un elemento de un conjunto de reglas de preprocesamiento de URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> predeterminado::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo 'default::' hace referencia a un atributo del catálogo de imágenes predeterminado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> viñeta::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo 'vignette::' hace referencia a un campo del mapa de viñetas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis opcionales se encierran entre corchetes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>El elemento de sintaxis opcional puede repetirse una o varias veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> elemento2 </span> </p> </td> 
  <td class="stentry"> <p>Una barra vertical indica que se puede utilizar el elemento de sintaxis único a la izquierda o el elemento a la derecha. Se debe seleccionar exactamente un elemento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> grupo </span> } </p> </td> 
  <td class="stentry"> <p>Las llaves se utilizan para agrupar los elementos de sintaxis. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> grupo </span> } </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis dentro del grupo pueden repetirse una o varias veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Espacio en blanco. </p> </td> 
  <td class="stentry"> <p>En las solicitudes HTTP no se permiten espacios en blanco (espacios o fichas). Este documento utiliza ocasionalmente espacios en blanco entre elementos sintácticos para obtener una mayor claridad. </p> </td> 
 </tr> 
</table>

