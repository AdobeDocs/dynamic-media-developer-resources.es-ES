---
description: Utilice los siguientes comandos para aplicar formato de texto avanzado.
solution: Experience Manager
title: Formato de texto avanzado
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
TQID: 'https://experienceleague.adobe.com/ZTUWB5N6T-I3DnokCqX--dj9g-807-D9Fv8l20opVkg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 0%

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
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>Subíndice sin cambio de tamaño de fuente. </p> </td> 
   <td> <p>Posición en medios puntos; el valor predeterminado es 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>Superíndice sin cambio de tamaño de fuente. </p> </td> 
   <td> <p>Posición en medios puntos; el valor predeterminado es 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span> </span> </td> 
   <td> <p>Deshabilitar/habilitar en el tamaño de fuente especificado. </p> </td> 
   <td> <p>Tamaño de fuente en puntos medios, por encima del cual aplicar kerning; 0 para deshabilitar kerning; el valor predeterminado es 1 para kerning en todos los tamaños de fuente en punto medio. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>Seleccione kerning óptico. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>Seleccione el kerning métrico. </p> </td> 
   <td> <p>Predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>Modifique el espaciado entre caracteres. </p> </td> 
   <td> <p>Puntos de trimestre positivos o negativos; el valor predeterminado es 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>Modifique el espaciado entre caracteres. </p> </td> 
   <td> <p>twips positivos o negativos. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>Escala de caracteres horizontal. </p> </td> 
   <td> <p>Porcentaje positivo o negativo; el valor predeterminado es 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>Escala de caracteres vertical. </p> </td> 
   <td> <p>Porcentaje positivo o negativo; el valor predeterminado es 100; extensión de Dynamic Media. </p> <p> <span class="codeph"> \charscaley </span> también escala el interlineado al aplicar <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> conserva siempre el interlineado independientemente de la escala vertical de caracteres. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Seleccione el flujo de caracteres de izquierda a derecha. </p> </td> 
   <td> <p>Predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Seleccione el flujo de caracteres de derecha a izquierda. </p> </td> 
   <td> <p> <span class="codeph"> text= </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>Active el ajuste de copia y defina el tamaño de fuente más grande permitido. </p> </td> 
   <td> <p>Tamaño de fuente en medios puntos; <span class="codeph"> textPs= </span> solamente; extensión de Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Máximo de líneas de ajuste de copia (límite suave). </p> </td> 
   <td> <p>0 para la limitación sin líneas; solo <span class="codeph"> textPs= </span>; extensión de Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Máximo de líneas de ajuste de copia (truncado). </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente; extensión de Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>Orientación de caracteres. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente; omitido para fuentes no romanas; omitido cuando <span class="codeph"> \stextflow1 </span> no está en vigor. </p> <p>0 vertical (valor predeterminado). </p> <p>1 girado 90 grados a la derecha. </p> </td> 
  </tr> 
 </tbody> 
</table>
