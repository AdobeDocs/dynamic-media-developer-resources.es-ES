---
description: La variable de sustitución se utiliza para transferir valores de la dirección URL de la solicitud a plantillas FXG almacenadas en el servidor.
solution: Experience Manager
title: Variables de sustitución
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Variables de sustitución{#substitution-variables}

La variable de sustitución se utiliza para transferir valores de la dirección URL de la solicitud a plantillas FXG almacenadas en el servidor.

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de la variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor al que se debe configurar la variable (cadena). </p> </td> 
 </tr> 
</table>

* Las definiciones y referencias de variables pueden producirse en la parte de consulta de la dirección URL de la solicitud.
* Las variables se definen como se indica arriba, de forma similar a otros comandos IS; el elemento principal &#39;$&#39; identifica el comando como una definición de variable.
* El nombre de la variable `*`var`*` distingue entre mayúsculas y minúsculas y puede constar de cualquier combinación de letras, números, &#39;-&#39; y &#39;_&#39;.
* El valor importante debe tener codificación de dirección URL de paso único para la transmisión HTTP segura.

