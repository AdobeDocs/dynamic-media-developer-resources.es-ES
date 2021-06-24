---
description: Utilice los siguientes comandos para codificar caracteres.
solution: Experience Manager
title: Codificación de caracteres
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

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
