---
description: 'La sintaxis básica del protocolo HTTP es la siguiente:'
solution: Experience Manager
title: Sintaxis básica del protocolo HTTP del servicio de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# Sintaxis básica del protocolo HTTP del servicio de imágenes{#image-serving-http-protocol-basic-syntax}

La sintaxis básica del protocolo HTTP es la siguiente:

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> solicitud</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> servidor</span>/es/imagen[/<span class="varname"> objeto</span>][?<span class="varname"> modificadores</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> servidor </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dirección_servidor</span>[:<span class="varname"> puerto</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objeto</span> </span> </p></td> 
  <td class="stentry"> <p>especificador de objeto de Source (ruta de imagen o entrada de catálogo de imágenes). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificadores</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificador</span>*[&amp;<span class="varname"> modificador</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificador</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">comando|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comentario</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> comando</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de una macro de comando.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> comentario</span> </span> </p></td> 
  <td class="stentry"> <p>Cadena de comentario (ignorada por el servidor).</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>Uno de los nombres de comando o atributo admitidos.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de una variable personalizada.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> valor</span> </span> </p></td> 
  <td class="stentry"> <p>Comando o valor de variable. </p></td> 
 </tr> 
</table>

*`server_address`*, *`cmdName`*, *`macro`* y *`var`* no distinguen entre mayúsculas y minúsculas. El servidor conserva las mayúsculas y minúsculas de todos los demás valores de cadena.

*`value`* es específico del comando y puede constar de uno o más valores separados por comas. Consulte la descripción de los comandos individuales para obtener más información.

## Identificador del servidor {#section-926ae55ddba14b8d952147a5fd701e14}

El contexto raíz [!DNL /is/image] es necesario para todas las solicitudes HTTP al servicio de imágenes.

## Descodificación HTTP {#section-20922baccd804d2d986b44ce9a183a7d}

El servicio de imágenes primero extrae *`object`* y *`modifiers`* de la solicitud entrante. *`object`* se separa en elementos de ruta que se descodifican individualmente en HTTP. La cadena *`modifiers`* está separada en pares *`command`*= *`value`* y *`value`* se descodifica en HTTP antes del procesamiento específico del comando.

>[!NOTE]
>
>A menos que se indique lo contrario en la documentación, todos los caracteres no seguros deben codificarse según el estándar HTTP. Consulte la especificación HTTP para obtener más información.

## Comentarios {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Los comentarios se pueden incrustar en cadenas de solicitud en cualquier lugar y se identifican con un punto (.) inmediatamente después del separador de comandos (&amp;). El comentario termina con la siguiente aparición de un separador de comandos (no codificado). Esta función se puede utilizar para agregar información a la solicitud que no sea para uso del servicio de imágenes, como marcas de tiempo e ID de bases de datos.

## Véase también {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Tipos de datos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [Especificación HTTP/1.1](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
