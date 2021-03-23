---
description: Utilice los siguientes comandos para codificar caracteres.
seo-description: Utilice los siguientes comandos para codificar caracteres.
seo-title: Codificación de caracteres
solution: Experience Manager
title: Codificación de caracteres
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 1%

---


# Codificación de caracteres{#character-encoding}

Utilice los siguientes comandos para codificar caracteres.

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> Comando </th> 
   <th class="entry"> Descripción </th> 
   <th class="entry"> Notas </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>Carácter sencillo de 8 bits. </p> </td> 
   <td> <p><span class="varname"> </span> Debe ser un valor hexadecimal de 2 dígitos. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>Carácter Unicode único. </p> </td> 
   <td> <p><span class="varname"> </span> Es un entero de 2 bytes con signo y, por lo tanto, un valor Unicode bueno a 32767 debe expresarse como un número negativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Tamaño de caracteres Unicode. </p> </td> 
   <td> <p>Número de bytes correspondientes a un carácter Unicode determinado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>A continuación se muestran los caracteres del área ANSI baja. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich  </span> </td> 
   <td> <p>A continuación se muestran los caracteres del área ANSI alta. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>A continuación se muestran los caracteres de doble byte. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

