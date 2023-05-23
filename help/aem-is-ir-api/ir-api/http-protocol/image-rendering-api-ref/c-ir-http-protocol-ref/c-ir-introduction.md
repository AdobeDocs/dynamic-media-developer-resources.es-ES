---
title: Introducción
description: Este documento describe el protocolo HTTP para el procesamiento de imágenes de Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---

# Introducción{#introduction}

Este documento describe el protocolo HTTP para el procesamiento de imágenes de Dynamic Media.

Solo se describen los aspectos del protocolo que están a disposición del público. El servidor puede admitir comandos adicionales reservados para su uso por el software cliente de Dynamic Media.

**Destinatarios previstos**

Este documento está dirigido a programadores y desarrolladores de sitios web experimentados que deseen utilizar el procesamiento de imágenes de Dynamic Media para un sitio web o una aplicación personalizada.

Se da por hecho que el lector está familiarizado con la creación y el procesamiento de imágenes de Dynamic Media, las convenciones y los estándares generales del protocolo HTTP y la terminología básica de las imágenes.

**Convenciones de documentos**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>literal </p> </td> 
  <td class="stentry"> <p>En las secciones de sintaxis, el texto que no está en cursiva es literal; no se aplica al espacio en blanco ni a los símbolos [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>En las secciones descriptivas, el texto sin cursiva entre comillas simples es literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parámetro </span> </p> </td> 
  <td class="stentry"> <p>La cursiva indica una variable o un parámetro que se va a sustituir por un valor real. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "attribute:::" hace referencia a un atributo de catálogo de imágenes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "catalog::" hace referencia a un campo de datos del catálogo de materiales. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "icc::" hace referencia a un campo del mapa de perfiles de color ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "macro::" hace referencia a un campo de la tabla de definición de macros. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conjunto de reglas::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "ruleset::" hace referencia a un elemento de un conjunto de reglas de preprocesamiento de URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> predeterminado::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "default::" hace referencia a un atributo del catálogo de imágenes predeterminado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> viñeta::Item </span> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "viñeta::" hace referencia a un campo del mapa de viñetas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> opcional </span> ] </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis opcionales están entre corchetes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> opcional </span> ] </p> </td> 
  <td class="stentry"> <p>El elemento de sintaxis opcional se puede repetir una o más veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
  <td class="stentry"> <p>Una barra vertical indica que se puede utilizar el único elemento de sintaxis a la izquierda o el elemento a la derecha. Se debe seleccionar exactamente un elemento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> grupo </span> } </p> </td> 
  <td class="stentry"> <p>Las llaves se utilizan para agrupar elementos de sintaxis. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> grupo </span> } </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis dentro del grupo se pueden repetir una o más veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>espacio en blanco </p> </td> 
  <td class="stentry"> <p>No se permiten espacios en blanco (espacios o pestañas) en las solicitudes HTTP. En ocasiones, este documento utiliza espacios en blanco entre elementos sintácticos solo para fines de claridad. </p> </td> 
 </tr> 
</table>

**Términos comunes**

** *`MSS`* Segmento de Especificación de Material **: un conjunto de atributos de material entre dos comandos de selección de la solicitud.

** *`vignette`* ** Imagen preparada en Dynamic Media Image Authoring para su uso con Image Rendering.
