---
description: La variable de sustitución se utiliza para transferir valores de la dirección URL de la solicitud a las plantillas FXG almacenadas en el servidor.
seo-description: La variable de sustitución se utiliza para transferir valores de la dirección URL de la solicitud a las plantillas FXG almacenadas en el servidor.
seo-title: Variables de sustitución
solution: Experience Manager
title: Variables de sustitución
topic: Scene7 Image Serving - Image Rendering API
uuid: 87cd9594-ba3b-429d-aa57-399902ef3abe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# Variables de sustitución{#substitution-variables}

La variable de sustitución se utiliza para transferir valores de la dirección URL de la solicitud a las plantillas FXG almacenadas en el servidor.

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de la variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor en el que se va a establecer la variable (cadena). </p> </td> 
 </tr> 
</table>

* Las definiciones y referencias de variables pueden producirse en la parte de consulta de la dirección URL de la solicitud.
* Las variables se definen como se indica arriba, de forma similar a otros comandos IS; el &#39;$&#39; inicial identifica el comando como una definición de variable.
* El nombre de la variable ` *`var`*` distingue entre mayúsculas y minúsculas y puede constar de cualquier combinación de letras, números, &#39;-&#39; y &#39;_&#39;.
* El valor importante debe tener una codificación de dirección URL de paso único para la transmisión HTTP segura.

