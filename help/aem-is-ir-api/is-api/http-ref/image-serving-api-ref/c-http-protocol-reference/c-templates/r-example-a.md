---
title: Ejemplo A
description: Cree una plantilla de tamaño fijo con una imagen de fondo estática, una imagen variable que esté alineada con el fondo en el centro izquierdo y escalada para no superar el 80 % de la anchura y altura del fondo. Y finalmente, una capa de texto con texto vertical centrado en el borde derecho del lienzo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Ejemplo A{#example-a}

Cree una plantilla de tamaño fijo con una imagen de fondo estática, una imagen variable que esté alineada con el fondo en el centro izquierdo y escalada para no superar el 80 % de la anchura y altura del fondo. Y finalmente, una capa de texto con texto vertical centrado en el borde derecho del lienzo.

![Ejemplo: Una imagen](assets/examplea.png)

## El registro de plantilla {#section-32f54710593e438fa0622224c89380af}

Insertar objeto

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catálogo::Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catálogo::Modificador </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text+gues+here&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0 </span> </p> </td> 
 </tr> 
</table>

Los valores `origin=` de todas las capas se especifican explícitamente en la plantilla para controlar estrictamente la colocación y alineación de las capas. Cada origen de capa se define para que coincida con la alineación deseada para esa capa. `origin=` para el fondo (capa 0) está establecido en el centro; este valor es arbitrario porque la imagen de fondo no cambia en tiempo de ejecución; se podría utilizar cualquier valor para el origen de capa 0.

Los valores `pos=` proporcionan los desplazamientos necesarios entre los puntos de origen de la capa para lograr la posición deseada de la capa.

El anclaje de la imagen de capa 1 se coloca en el centro izquierdo, con el valor `pos=`. Este ajuste logra la alineación centro-izquierda entre el fondo y la imagen de la capa 1, independientemente de la proporción de aspecto de la imagen de la capa 1.

Del mismo modo, el anclaje de la capa de texto se coloca en el centro derecho del cuadro de texto de tamaño automático, con el valor `pos=`. Esta configuración logra la alineación deseada del centro derecho para el texto girado, independientemente del tamaño de fuente y la longitud de la cadena.

El texto que se va a mostrar se proporciona en tiempo de ejecución, por lo que se utiliza una variable para separar el texto del sobre de formato rtf. La variable predeterminada `$object` se usa para la imagen de capa 1. Esta variable permite especificar esta imagen en la ruta de solicitud.

Se puede utilizar cualquier imagen para la imagen de fondo y la imagen de capa 1. Si la imagen de fondo tiene una máscara, las áreas sin máscara se rellenarán con el color de fondo predeterminado (`attribute::BkgColor`) o se dejarán transparentes cuando `fmt=png-alpha` o `fmt=tif-alpha`. Si la imagen de fondo tiene una relación de aspecto no cuadrada, se centrará en la imagen de respuesta y el espacio adicional se rellenará con `attribute::BkgColor`. Si la imagen de la capa 1 tiene datos alfa o una máscara, la imagen de fondo (o el color de fondo) permanece visible en las áreas transparentes. Si la imagen no tiene máscara, rellena todo el rectángulo asignado.

## Uso de la plantilla {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`servidor`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

La siguiente imagen muestra el resultado compuesto para diferentes proporciones de aspecto de la imagen de capa 1 y diferentes cadenas de texto.

![Ejemplo: Una imagen de resultado compuesta](assets/exampleausing.png)
