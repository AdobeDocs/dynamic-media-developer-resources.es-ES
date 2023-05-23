---
description: Utilice los siguientes comandos para codificar caracteres.
solution: Experience Manager
title: Codificación de caracteres
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
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
   <td> <p>Carácter único de 8 bits. </p> </td> 
   <td> <p><span class="varname"> HH</span> debe tener un valor hexadecimal de 2 dígitos. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Carácter Unicode único. </p> </td> 
   <td> <p><span class="varname"> N</span> es un entero de 2 bytes con signo y, por lo tanto, un valor Unicode bueno a 32767 debe expresarse como un número negativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Tamaño de carácter Unicode. </p> </td> 
   <td> <p>Número de bytes correspondientes a un carácter Unicode determinado. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>A continuación aparecen caracteres del área ANSI inferior. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>A continuación aparecen caracteres del área ANSI superior. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>A continuación aparecen caracteres de doble byte. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
