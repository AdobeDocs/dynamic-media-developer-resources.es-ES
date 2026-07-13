---
description: Este documento describe el catálogo de materiales para el procesamiento de imágenes de Dynamic Media.
solution: Experience Manager
title: Introducción
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1cdb9c45-329d-44df-92c3-8cba5b2b1339
TQID: 'https://experienceleague.adobe.com/VGAiUARHzSeBN5fVSP-Gi752ZTWxS9LBzqXWoL8mKOM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 0%

---

# Introducción{#introduction}

Este documento describe el catálogo de materiales para el procesamiento de imágenes de Dynamic Media.

**Audiencia prevista**

Este documento está diseñado para programadores con experiencia y desarrolladores de sitios web que deseen aprovechar el procesamiento de imágenes de Dynamic Media para un sitio web o una aplicación personalizada.

Se da por hecho que el lector está familiarizado con la creación y el procesamiento de imágenes de Dynamic Media, las convenciones y los estándares generales del protocolo HTTP y la terminología básica de imágenes.

**Convenciones de documentos**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Literal </p> </td> 
  <td class="stentry"> <p>En las secciones de sintaxis, el texto sin cursiva es literal; esto no se aplica al espacio en blanco y a los símbolos [ ] { } | *. </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> atributo::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "attribute:::" hace referencia a un atributo de catálogo de imágenes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catálogo::Elemento </span> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> viñeta::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo "viñeta::" hace referencia a un campo del mapa de viñetas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> </span> opcional ] </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis opcionales están entre corchetes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> </span> opcional ] </p> </td> 
  <td class="stentry"> <p>El elemento de sintaxis opcional se puede repetir una o más veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> elemento1 </span>| <span class="varname"> elemento2 </span> </p> </td> 
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
  <td class="stentry"> <p>Espacio en blanco. </p> </td> 
  <td class="stentry"> <p>No se permiten espacios en blanco (espacios o pestañas) en las solicitudes HTTP. En ocasiones, este documento utiliza espacios en blanco entre elementos sintácticos solo para fines de claridad. </p> </td> 
 </tr> 
</table>

