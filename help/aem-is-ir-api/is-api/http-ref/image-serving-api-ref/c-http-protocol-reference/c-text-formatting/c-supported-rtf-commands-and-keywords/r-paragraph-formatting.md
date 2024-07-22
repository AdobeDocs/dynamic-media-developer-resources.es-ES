---
description: Se admiten los siguientes comandos de formato de párrafo.
solution: Experience Manager
title: Formato de párrafo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Formato de párrafo{#paragraph-formatting}

Se admiten los siguientes comandos de formato de párrafo.

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Comando </p> </th> 
   <th class="entry"> <p>Descripción </p> </th> 
   <th class="entry"> <p>Notas </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>Restablecer el formato de párrafo al valor predeterminado. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>Alinear texto a la izquierda. </p> </td> 
   <td> <p>Predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>Alinear texto a la derecha. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>Centrar texto horizontalmente. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>Justificar el texto horizontalmente. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>Alinear a la izquierda la última línea de un párrafo. </p> </td> 
   <td> <p>Predeterminado; solo <span class="codeph"> textPs= </span>; se omitirá si <span class="codeph"> \qj </span> no está activo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>Alinee a la derecha la última línea de un párrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente; se omitirá si <span class="codeph"> \qj </span> no está activo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>Centrar la última línea de un párrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente; se omitirá si <span class="codeph"> \qj </span> no está activo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>Sustituir (estirar) la última línea de un párrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente; se omitirá si <span class="codeph"> \qj </span> no está activo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>Sangría de primera línea. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>Sangría izquierda. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>Sangría derecha. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>Espacio entre líneas. </p> </td> 
   <td> <p>0 (valor predeterminado) para el interlineado automático; valores positivos para utilizar únicamente valores mayores que el interlineado predeterminado; valores negativos para forzar el interlineado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>Indicador múltiple de interlineado. </p> </td> 
   <td> <p>Establezca como 0 (predeterminado) si <span class="codeph"> \sl </span> está en twips, como 1 si <span class="codeph"> \sl </span> está en múltiplos del espaciado predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>Espacio adicional antes del párrafo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>aplica <span class="codeph"> \sb </span> al primer párrafo del cuadro de texto, <span class="codeph"> textPs= </span> no. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>Espacio adicional después del párrafo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> aplica <span class="codeph"> \sa </span> al último párrafo del cuadro de texto, <span class="codeph"> textPs= </span> no. </p> </td> 
  </tr> 
 </tbody> 
</table>
