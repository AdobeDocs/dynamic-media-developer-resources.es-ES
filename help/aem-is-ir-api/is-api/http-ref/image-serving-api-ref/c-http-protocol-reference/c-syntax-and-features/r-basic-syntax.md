---
description: 'La sintaxis básica del protocolo HTTP es la siguiente:'
solution: Experience Manager
title: Sintaxis básica del protocolo HTTP de servicio de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---

# Sintaxis básica del protocolo HTTP de servicio de imágenes{#image-serving-http-protocol-basic-syntax}

La sintaxis básica del protocolo HTTP es la siguiente:

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> solicitud</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> modificadores</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
  <td class="stentry"> <p>Especificador de objetos de origen (ruta de acceso de imagen o entrada de catálogo de imágenes). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificadores</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificador</span>*[&amp;<span class="varname"> modificador</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificador</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">comando|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> command</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}[=<span class="varname"> valor</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de una macro de comando.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> comment</span> </span> </p></td> 
  <td class="stentry"> <p>Cadena de comentarios (ignorada por el servidor).</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>Uno de los nombres de comandos o atributos admitidos.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de una variable personalizada.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>Comando o valor de variable. </p></td> 
 </tr> 
</table>

*`server_address`*,  *`cmdName`*,  *`macro`*, y  *`var`* distinguen entre mayúsculas y minúsculas. El servidor conserva las mayúsculas y minúsculas del resto de los valores de cadena.

*`value`* es específico para cada comando y puede constar de uno o más valores separados por comas. Consulte la descripción de los comandos individuales para obtener más detalles.

## Identificador de servidor {#section-926ae55ddba14b8d952147a5fd701e14}

El contexto raíz [!DNL /is/image] es necesario para todas las solicitudes HTTP al servicio de imágenes.

## Descodificación HTTP {#section-20922baccd804d2d986b44ce9a183a7d}

El servicio de imágenes extrae primero *`object`* y *`modifiers`* de la solicitud entrante. *`object`* a continuación, se separa en elementos de ruta que se decodifican individualmente con HTTP. La cadena *`modifiers`* se separa en pares *`command`*= *`value`* y *`value`* se decodifica HTTP antes del procesamiento específico del comando.

>[!NOTE]
>
>A menos que se indique lo contrario en la documentación, todos los caracteres no seguros deben codificarse según el estándar HTTP. Consulte la especificación HTTP para obtener más información.

## Comentarios {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Los comentarios se pueden incrustar en cadenas de solicitud en cualquier lugar y se identifican mediante un punto (.) inmediatamente después del comando separator(&amp;). El comentario termina con la siguiente incidencia de un separador de comandos (sin codificar). Esta función se puede utilizar para agregar información a la solicitud que no se utilice con el servicio de imágenes, como marcas de hora e ID de base de datos.

## Véase también {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Tipos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa) de datos, especificación  [HTTP/1.1](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
