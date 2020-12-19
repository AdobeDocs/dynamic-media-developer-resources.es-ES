---
description: Se admiten los siguientes comandos de formato de párrafo.
seo-description: Se admiten los siguientes comandos de formato de párrafo.
seo-title: Formato de párrafo
solution: Experience Manager
title: Formato de párrafo
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f9255b2-3a74-4c9a-80c5-d85b4627027e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 1%

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
   <td> <span class="codeph"> \pard  </span> </td> 
   <td> <p>Restablezca el formato de párrafo al formato predeterminado. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> solamente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql  </span> </td> 
   <td> <p>Alinea el texto a la izquierda. </p> </td> 
   <td> <p>Predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>Alinea el texto a la derecha. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>Centrar texto horizontalmente. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>Justificar texto horizontalmente. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> solamente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>Alinea a la izquierda la última línea de un párrafo. </p> </td> 
   <td> <p>Predeterminado; <span class="codeph"> textPs= </span> solamente; se omite si <span class="codeph"> \qj </span>no está activo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>Alinea a la derecha la última línea de un párrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; se omite si  <span class="codeph"> \qj no  </span> está activo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>Centra la última línea de un párrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; se omite si  <span class="codeph"> \qj no  </span>está activo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>Sustituya (estire) la última línea de un párrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; se omite si  <span class="codeph"> \qj no  </span>está activo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Sangría de primera línea. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Sangría izquierda. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Sangría derecha. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Espacio entre líneas. </p> </td> 
   <td> <p>0 (predeterminado) para interlineado automático; valores positivos para utilizar solo el valor si es mayor que el interlineado predeterminado; valor negativo para forzar el espaciado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Interlineado con varios indicadores. </p> </td> 
   <td> <p>Se establece en 0 (predeterminado) si <span class="codeph"> \sl </span> está en twips, en 1 si <span class="codeph"> \sl </span> está en múltiplos del espaciado predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Espacio adicional antes del párrafo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>aplica <span class="codeph"> \sb </span> al primer párrafo del cuadro de texto, <span class="codeph"> textPs= </span> no. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Espacio adicional después del párrafo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> aplica <span class="codeph"> \sa </span> al último párrafo del cuadro de texto, <span class="codeph"> textPs= </span> no. </p> </td> 
  </tr> 
 </tbody> 
</table>

