---
description: En esta sección se describe la sintaxis básica del protocolo HTTP de procesamiento de imágenes de Dynamic Media.
seo-description: En esta sección se describe la sintaxis básica del protocolo HTTP de procesamiento de imágenes de Dynamic Media.
seo-title: Sintaxis básica del protocolo HTTP de renderización de imágenes
solution: Experience Manager
title: Sintaxis básica del protocolo HTTP de renderización de imágenes
uuid: e01314f0-6aaa-41ca-8c05-d5db3148a071
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 3%

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
   <td colname="col2"> <p>http://<span class="varname"> servidor</span>/ir/renderizar[/<span class="varname"> viñeta</span> ] [ ?<span class="varname"> modificadores</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [:<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> viñeta  </span> </p> </td> 
   <td colname="col2"> <p>Especificador de viñetas (ruta de archivo relativa o entrada de catálogo de viñetas). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificadores </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modificador</span> *[ &amp;  <span class="varname"> modificador</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificador </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> comando</span> | { $  <span class="varname"> macro</span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> valor</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro  </span> </p> </td> 
   <td colname="col2"> <p>Nombre de una macro de comando. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comment  </span> </p> </td> 
   <td colname="col2"> <p>Cadena de comentarios (ignorada por el servidor). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName  </span> </p> </td> 
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

*`server`*,  *`cmdName`*,  *`macro`*, y  *`var`* distinguen entre mayúsculas y minúsculas. El servidor conserva las mayúsculas y minúsculas del resto de los valores de cadena.

**Identificador de servidor**

El contexto raíz &#39; `/ir/render`&#39; es necesario para todas las solicitudes HTTP de renderización de imágenes.

**Comentarios**

Los comentarios pueden incrustarse en cadenas de solicitud en cualquier lugar y se identifican con un punto (.) inmediatamente después del separador de comandos (&amp;). El comentario termina con la siguiente incidencia de un separador de comandos (descodificado). Esta función se puede utilizar para añadir información a la solicitud que no se utilice con el servicio de imágenes, como marcas de hora, ID de base de datos, etc.

**Descodificación HTTP**

El procesamiento de imágenes primero extrae *`object`* y *`modifiers`* de la solicitud entrante. *`object`* a continuación, se separa en elementos de ruta que se decodifican individualmente con HTTP. La cadena *`modifiers`* se separa en pares *`command`*= *`value`* y *`value`* se decodifica HTTP antes del procesamiento específico del comando.
