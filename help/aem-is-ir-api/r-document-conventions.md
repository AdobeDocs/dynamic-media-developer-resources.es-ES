---
description: Este documento utiliza las siguientes convenciones.
solution: Experience Manager
title: Convenciones de documentos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cc334766-544b-4d77-aa0e-4e509525cbaa
TQID: 'https://experienceleague.adobe.com/Zh--IKyCXWQJ9ZacS5zLFTmhXFa-3jCrSiU6PJULK-Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 282
ht-degree: 0%

---

# Convenciones de documentos{#document-conventions}

Este documento utiliza las siguientes convenciones.

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>literal </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> comando= </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con un "=" final hace referencia a un comando del protocolo HTTP del servicio de imágenes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> atributo::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> atributo: </span> hace referencia a un atributo de catálogo de imágenes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catálogo::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> del catálogo: </span> hace referencia a un campo de datos del catálogo de imágenes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> icc: </span> hace referencia a un campo en el mapa de perfiles de color ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> fuente::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> de fuente: </span> hace referencia a un campo en el mapa de fuentes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro: Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> macro: </span> hace referencia a un campo de la tabla de definición de macros. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conjunto de reglas::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> conjunto de reglas: </span> hace referencia a un elemento de un conjunto de reglas de procesamiento previo de URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> predeterminado::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nombre con el prefijo <span class="codeph"> predeterminado: </span> hace referencia a un atributo del catálogo de imágenes predeterminado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [ <span class="varname"> </span> opcional] </span> </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis opcionales están entre corchetes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[ <span class="varname"> </span> opcional] </span> </p> </td> 
  <td class="stentry"> <p>El elemento de sintaxis <span class="varname"> </span> opcional se puede repetir una o más veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> elemento1 </span>| <span class="varname"> elemento2 </span> </span> </p> </td> 
  <td class="stentry"> <p>Una barra vertical indica que se puede utilizar el único elemento de sintaxis a la izquierda o el elemento a la derecha. Se debe seleccionar exactamente un elemento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lbrace; <span class="varname"> grupo </span> </span> </p> </td> 
  <td class="stentry"> <p>Las llaves se utilizan para agrupar elementos de sintaxis. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{ <span class="varname"> grupo </span>} </span> </p> </td> 
  <td class="stentry"> <p>Los elementos de sintaxis dentro del grupo se pueden repetir una o más veces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>espacio en blanco </p> </td> 
  <td class="stentry"> <p>No se permiten espacios en blanco (espacios o pestañas) en las solicitudes HTTP. En ocasiones, este documento utiliza espacios en blanco entre elementos sintácticos solo para fines de claridad. </p> </td> 
 </tr> 
</table>
