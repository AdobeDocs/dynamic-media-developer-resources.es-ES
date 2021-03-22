---
description: Utilice los siguientes comandos para aplicar formato de texto avanzado.
seo-description: Utilice los siguientes comandos para aplicar formato de texto avanzado.
seo-title: Formato de texto avanzado
solution: Experience Manager
title: Formato de texto avanzado
uuid: 340166a5-5aef-4081-9114-a715cde68891
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---


# Formato de texto avanzado{#advanced-text-formatting}

Utilice los siguientes comandos para aplicar formato de texto avanzado.

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> Comando </th> 
   <th class="entry"> Descripción </th> 
   <th class="entry"> Notas </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Subíndice sin cambio de tamaño de fuente. </p> </td> 
   <td> <p>Posición en puntos medios; el valor predeterminado es 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Superíndice sin cambio de tamaño de fuente. </p> </td> 
   <td> <p>Posición en puntos medios; el valor predeterminado es 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Deshabilite/habilite en un tamaño de fuente especificado. </p> </td> 
   <td> <p>Tamaño de fuente en puntos medios, por encima de los cuales aplicar interletraje; 0 para desactivar el interletraje; el valor predeterminado es 1 para interletraje de todos los tamaños de fuente en un punto y medio. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningóptico  </span> </td> 
   <td> <p>Seleccione el interletraje óptico. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric  </span> </td> 
   <td> <p>Seleccione el interletraje de métrica. </p> </td> 
   <td> <p>Predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Modificar el espaciado de caracteres. </p> </td> 
   <td> <p>los cuartos de trimestre positivos o negativos; el valor predeterminado es 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Modificar el espaciado de caracteres. </p> </td> 
   <td> <p>Giros positivos o negativos. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charescalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Escalado horizontal de caracteres. </p> </td> 
   <td> <p>Porcentaje positivo o negativo; el valor predeterminado es 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charescaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Escalado vertical de caracteres. </p> </td> 
   <td> <p>Porcentaje positivo o negativo; el valor predeterminado es 100; Extensión de Dynamic Media. </p> <p> <span class="codeph"> \charescaley  </span> también escala el interlineado cuando se aplica con  <span class="codeph"> text=  </span>. <span class="codeph"> textPs=  </span> siempre conserva el interlineado independientemente de la cantidad de escala vertical de caracteres. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>Seleccione el flujo de caracteres de izquierda a derecha. </p> </td> 
   <td> <p>Predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>Seleccione el flujo de caracteres de derecha a izquierda. </p> </td> 
   <td> <p> <span class="codeph"> text=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Habilite el ajuste de copia y establezca el tamaño de fuente permitido más grande. </p> </td> 
   <td> <p>Tamaño de fuente en puntos medios; <span class="codeph"> textPs= </span> solamente; Extensión de Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Máximo de líneas de ajuste de copia (límite suave). </p> </td> 
   <td> <p>0 sin limitación de líneas; <span class="codeph"> textPs= </span> solamente; Extensión de Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Máximo de líneas de ajuste de copia (truncamiento). </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; Extensión de Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Orientación de caracteres. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignorado para fuentes no romanas; ignorado cuando  <span class="codeph"> \stextflow1 no  </span> está en efecto. </p> <p>0 vertical (predeterminado). </p> <p>1 giró 90 grados en el sentido de las agujas del reloj. </p> </td> 
  </tr> 
 </tbody> 
</table>

