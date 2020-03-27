---
description: La sintaxis básica del protocolo HTTP es la siguiente.
seo-description: La sintaxis básica del protocolo HTTP es la siguiente.
seo-title: Sintaxis básica del protocolo HTTP de servicio de imágenes
solution: Experience Manager
title: Sintaxis básica del protocolo HTTP de servicio de imágenes
topic: Scene7 Image Serving - Image Rendering API
uuid: 3269c2f2-df0f-4b62-ae9c-a267acae8071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Sintaxis básica del protocolo HTTP de servicio de imágenes{#image-serving-http-protocol-basic-syntax}

La sintaxis básica del protocolo HTTP es la siguiente.

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> solicitud</span></span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> modificadores</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> puerto</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objeto</span></span> </p></td> 
  <td class="stentry"> <p>Especificador de objetos de origen (ruta de acceso de imagen o entrada de catálogo de imágenes). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificadores</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificador</span>*[&amp;<span class="varname"> modificador</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificador</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">comando|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> , comando</span></span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> valor</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span></span> </p> </td> 
  <td class="stentry"> <p>Nombre de una macro de comando. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> comentario</span></span> </p></td> 
  <td class="stentry"> <p>Cadena de comentarios (ignorada por el servidor). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span></span> </p></td> 
  <td class="stentry"> <p>Uno de los nombres de comando o atributo admitidos. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span></span> </p> </td> 
  <td class="stentry"> <p>Nombre de una variable personalizada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span></span> </p></td> 
  <td class="stentry"> <p>Comando o valor de variable. </p></td> 
 </tr> 
</table>

*`server_address`*, *`cmdName`*, *`macro`* y *`var`* no distinguen entre mayúsculas y minúsculas. El servidor conserva las mayúsculas y minúsculas de todos los demás valores de cadena.

*`value`* es específico para cada comando y puede constar de uno o más valores separados por comas. Consulte la descripción de los comandos individuales para obtener más detalles.

## Identificador del servidor {#section-926ae55ddba14b8d952147a5fd701e14}

El contexto [!DNL /is/image] raíz es necesario para todas las solicitudes HTTP al servicio de imágenes.

## Descodificación HTTP {#section-20922baccd804d2d986b44ce9a183a7d}

El servicio de imágenes primero extrae *`object`* y *`modifiers`* de la solicitud entrante. *`object`* a continuación se separa en elementos de ruta que se descodifican individualmente en HTTP. La *`modifiers`* cadena se separa en pares *`command`*= *`value`* y *`value`* se descodifica mediante HTTP antes del procesamiento específico del comando.

>[!NOTE]
>
>A menos que se indique lo contrario en la documentación, todos los caracteres no seguros deben codificarse según el estándar HTTP. Consulte la especificación HTTP para obtener más detalles.

## Comentarios {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Los comentarios pueden incrustarse en cadenas de solicitud en cualquier lugar y se identifican mediante un punto (.) inmediatamente después del comando separator(&amp;). El comentario termina con la siguiente aparición de un separador de comandos (no codificado). Esta función se puede utilizar para agregar información a la solicitud que no se utiliza para el servicio de imágenes, como marcas de hora, ID de base de datos, etc.

## Véase también {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Tipos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa)de datos, especificación [HTTP/1.1](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
