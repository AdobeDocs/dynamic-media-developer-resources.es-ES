---
description: Requisitos similares a los del ejemplo A, pero utilice un fondo de color sólido y permita que la altura del compuesto varíe, para dar cabida a imágenes con diferentes proporciones de aspecto.
seo-description: Requisitos similares a los del ejemplo A, pero utilice un fondo de color sólido y permita que la altura del compuesto varíe, para dar cabida a imágenes con diferentes proporciones de aspecto.
seo-title: Ejemplo B
solution: Experience Manager
title: Ejemplo B
topic: Scene7 Image Serving - Image Rendering API
uuid: 13120562-9201-4733-bd9d-4a54eac913e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Ejemplo B{#example-b}

Requisitos similares a los del ejemplo A, pero utilice un fondo de color sólido y permita que la altura del compuesto varíe, para dar cabida a imágenes con diferentes proporciones de aspecto.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Modificador</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;extension=0,100,200,100&amp;src=$object$&amp;ourceN=.5,0&amp; layer=1&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;sourceN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

La imagen se coloca en la capa 0 y el valor de altura de `size=` se establece en 0, lo que hace que la altura real se determine por la altura de la imagen después de escalarla a 800 píxeles de ancho.

`extend=` agrega 100 píxeles a la parte superior e inferior y 200 píxeles a la derecha.

Los orígenes para la capa 0 y la capa 1 se colocan en el centro-derecha del área de composición, para conseguir la posición deseada del texto.

En la siguiente ilustración se muestra el resultado compuesto para diferentes proporciones de aspecto de la imagen y diferentes cadenas de texto.

![](assets/exampleb.png)

