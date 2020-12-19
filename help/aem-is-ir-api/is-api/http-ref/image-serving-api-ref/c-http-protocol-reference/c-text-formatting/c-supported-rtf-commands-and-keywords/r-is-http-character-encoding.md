---
description: Utilice los siguientes comandos para codificar caracteres.
seo-description: Utilice los siguientes comandos para codificar caracteres.
seo-title: Codificación de caracteres
solution: Experience Manager
title: Codificación de caracteres
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
   <td> <p>Carácter único de 8 bits. </p> </td> 
   <td> <p><span class="varname"> </span> El valor hexadecimal debe ser de 2 dígitos. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>Carácter Unicode único. </p> </td> 
   <td> <p><span class="varname"> </span> Nis es un entero de 2 bytes con signo y, por lo tanto, un valor Unicode bueno a 32767 debe expresarse como un número negativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Tamaño de caracteres Unicode. </p> </td> 
   <td> <p>Número de bytes correspondientes a un carácter Unicode determinado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>A continuación se muestran los caracteres de área ANSI baja. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich  </span> </td> 
   <td> <p>A continuación se muestran los caracteres de área ANSI alta. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>A continuación se muestran los caracteres de byte de doble. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

