---
description: Las variables de sustitución se utilizan para transferir valores desde la dirección URL de la solicitud a las plantillas FXG almacenadas en el servidor.
solution: Experience Manager
title: Variables de sustitución
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# Variables de sustitución{#substitution-variables}

Las variables de sustitución se utilizan para transferir valores desde la dirección URL de la solicitud a las plantillas FXG almacenadas en el servidor.

` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor en el que se va a establecer la variable (cadena). </p> </td> 
 </tr> 
</table>

* Las definiciones y referencias de variables pueden producirse en la parte de consulta de la dirección URL de la solicitud.
* Las variables se definen como se ha indicado anteriormente, de forma similar a otros comandos IS; el &#39;$&#39; inicial identifica el comando como una definición de variable.
* El nombre de variable `*`var`*` distingue entre mayúsculas y minúsculas y puede constar de cualquier combinación de letras, números, &#39;-&#39; y &#39;_&#39;.
* El valor importante debe tener codificación URL de un solo paso para la transmisión HTTP segura.
