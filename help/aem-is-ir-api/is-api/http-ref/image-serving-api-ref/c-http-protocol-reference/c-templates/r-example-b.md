---
description: Requisitos similares a los del ejemplo A, pero utilizando un fondo de color sólido y permitiendo que la altura del compuesto varíe, para dar cabida a imágenes con diferentes proporciones de aspecto.
solution: Experience Manager
title: Ejemplo B
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Ejemplo B{#example-b}

Requisitos similares a los del ejemplo A, pero utilizando un fondo de color sólido y permitiendo que la altura del compuesto varíe, para dar cabida a imágenes con diferentes proporciones de aspecto.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;extension=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf..$text$..rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

La imagen se coloca en la capa 0 y el valor de altura de `size=` se establece en 0, lo que hace que la altura real se determine por la altura de la imagen después de escalarla a 800 píxeles de ancho.

`extend=` añade 100 píxeles a la parte superior e inferior y 200 píxeles a la derecha.

Los orígenes de la capa 0 y de la capa 1 se colocan en el centro-derecho del área de composición, para conseguir la posición de texto deseada.

La siguiente ilustración muestra el resultado compuesto para diferentes proporciones de aspecto de la imagen y diferentes cadenas de texto.

![](assets/exampleb.png)
