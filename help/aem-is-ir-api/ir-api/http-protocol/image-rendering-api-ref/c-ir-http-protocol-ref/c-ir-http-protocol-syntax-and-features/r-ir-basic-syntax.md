---
title: Sintaxis básica del protocolo HTTP de procesamiento de imágenes
description: En esta sección se describe la sintaxis básica del protocolo HTTP del procesamiento de imágenes de Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Sintaxis básica del protocolo HTTP de procesamiento de imágenes{#image-rendering-http-protocol-basic-syntax}

En esta sección se describe la sintaxis básica del protocolo HTTP del procesamiento de imágenes de Dynamic Media.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Elemento </p> </th> 
   <th colname="col2" class="entry"> <p>Definición </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> solicitud</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> modificadores</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> servidor </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> dirección_servidor</span> [ :<span class="varname"> puerto</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> viñeta </span> </p> </td> 
   <td colname="col2"> <p>Especificador de viñeta (ruta relativa de archivo o entrada de catálogo de viñetas). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificadores </span> </p> </td> 
   <td colname="col2"> <p>Modificador <span class="varname"></span> *[ &amp; <span class="varname"> modificador</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Modificador <span class="varname"> </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> comando</span> | { $ <span class="varname"> macro</span> $ } | { .<span class="varname"> comentario</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">, comando </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> valor</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro </span> </p> </td> 
   <td colname="col2"> <p>Nombre de una macro de comando. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comentario </span> </p> </td> 
   <td colname="col2"> <p>Cadena de comentario (ignorada por el servidor). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>Nombre de un comando o atributo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Nombre de una variable personalizada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> valor </span> </p> </td> 
   <td colname="col2"> <p>Comando o valor de variable. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* y *`var`* no distinguen entre mayúsculas y minúsculas. El servidor conserva las mayúsculas y minúsculas de todos los demás valores de cadena.

**Identificador de servidor**

El contexto raíz &#39; `/ir/render`&#39; es necesario para todas las solicitudes HTTP a Image Rendering.

**Comentarios**

Los comentarios pueden incrustarse en las cadenas de solicitud en cualquier lugar y se identifican con un punto (.) inmediatamente después del separador de comandos (&amp;). El comentario termina con la siguiente aparición de un separador de comandos (no codificado). Esta función se puede utilizar para agregar información a la solicitud que no sea para uso del servicio de imágenes, como marcas de tiempo e id de base de datos.

**Descodificación HTTP**

El procesamiento de imágenes primero extrae *`object`* y *`modifiers`* de la solicitud entrante. A continuación, *`object`* se separa en elementos de ruta que se descodifican individualmente en HTTP. La cadena *`modifiers`* está separada en pares *`command`*= *`value`* y *`value`* se descodifica en HTTP antes del procesamiento específico del comando.
