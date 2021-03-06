---
title: Sintaxis básica del protocolo HTTP de renderización de imágenes
description: En esta sección se describe la sintaxis básica del protocolo HTTP de procesamiento de imágenes de Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 4%

---

# Sintaxis básica del protocolo HTTP de renderización de imágenes{#image-rendering-http-protocol-basic-syntax}

En esta sección se describe la sintaxis básica del protocolo HTTP de procesamiento de imágenes de Dynamic Media.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Elemento </p> </th> 
   <th colname="col2" class="entry"> <p>Definición </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> request</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> viñeta</span> ] [ ?<span class="varname"> modificadores</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> puerto</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> viñeta </span> </p> </td> 
   <td colname="col2"> <p>Especificador de viñetas (ruta de archivo relativa o entrada de catálogo de viñetas). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificadores </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modificador</span> *[ &amp; <span class="varname"> modificador</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificador </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $ <span class="varname"> macro</span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro </span> </p> </td> 
   <td colname="col2"> <p>Nombre de una macro de comando. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comment </span> </p> </td> 
   <td colname="col2"> <p>Cadena de comentarios (ignorada por el servidor). </p> </td> 
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
   <td colname="col1"> <p><span class="varname"> basado en IP </span> </p> </td> 
   <td colname="col2"> <p>Comando o valor de variable. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* y *`var`* no distinguen entre mayúsculas y minúsculas. El servidor conserva las mayúsculas y minúsculas del resto de los valores de cadena.

**Identificador de servidor**

El `/ir/render`&#39; el contexto raíz es necesario para todas las solicitudes HTTP de representación de imágenes.

**Comentarios**

Los comentarios pueden incrustarse en cadenas de solicitud en cualquier lugar y se identifican con un punto (.) inmediatamente después del separador de comandos (&amp;). El comentario termina con la siguiente incidencia de un separador de comandos (sin codificar). Esta función se puede utilizar para agregar información a la solicitud que no se utilice con el servicio de imágenes, como marcas de hora e identificadores de base de datos.

**Descodificación HTTP**

Extractos de primera representación de imágenes *`object`* y *`modifiers`* de la solicitud entrante. La variable *`object`* a continuación, se separa en elementos de ruta que se decodifican individualmente con HTTP. La variable *`modifiers`* la cadena se separa en *`command`*= *`value`* pares y *`value`* después se descodifica mediante HTTP antes del procesamiento específico del comando.
