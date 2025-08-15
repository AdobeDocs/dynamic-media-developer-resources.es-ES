---
description: Las siguientes propiedades de documento son compatibles con los cuadros de texto.
solution: Experience Manager
title: Propiedades del documento (cuadro de texto)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Propiedades del documento (cuadro de texto){#document-text-box-properties}

Las siguientes propiedades de documento son compatibles con los cuadros de texto.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Comando</b> </th> 
   <th class="entry"> <b>Descripción</b> </th> 
   <th class="entry"> <b>Notas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl </span> </td> 
   <td> <p>Tabla de fuentes. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>Conjunto de caracteres para la fuente <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>Tabla de color de RGB. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>Tabla de color CMYK. </p> </td> 
   <td> <p>Extensión de Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>Tabla de colores para los colores del servicio de imágenes. </p> </td> 
   <td> <p>Extensión de Dynamic Media; <span class="codeph"> textPs= </span> solamente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de color rojo. </p> </td> 
   <td> <p>Puede aparecer solamente en <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de color verde. </p> </td> 
   <td> <p>Puede aparecer solamente en <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de color azul. </p> </td> 
   <td> <p>Puede aparecer solamente en <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cian <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de color cian. </p> </td> 
   <td> <p>Extensión de Dynamic Media; solo puede aparecer en <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de color magenta. </p> </td> 
   <td> <p>Extensión de Dynamic Media; solo puede aparecer en <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \amarillo <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de color amarillo. </p> </td> 
   <td> <p>Extensión de Dynamic Media; solo puede aparecer en <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de color negro. </p> </td> 
   <td> <p>Extensión de Dynamic Media; solo puede aparecer en <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>Margen izquierdo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> solamente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>Margen derecho. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> solamente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>Margen superior. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> solamente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>Margen inferior. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> solamente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>Alinear texto arriba en el cuadro de texto. </p> </td> 
   <td> <p>Predeterminado </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>Alinear texto en el cuadro de texto. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>Centrar texto en el cuadro de texto. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>Orientación del flujo de texto. </p> </td> 
   <td> <p>Flujo de texto específico del idioma; <span class="codeph"> textPs= </span> solamente 0 (predeterminado) left-right, top-bottom (europeo) 1 top-bottom, right-left (extremo oriental) </p> </td> 
  </tr> 
 </tbody> 
</table>
