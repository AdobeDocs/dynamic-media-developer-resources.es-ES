---
title: color
description: Color de capa. Especifica el color de primer plano y la opacidad de las capas de color sólido y efecto, así como el color de relleno del cuadro de texto de las capas de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---

# color{#color}

Color de capa. Especifica el color de primer plano y la opacidad de las capas de color sólido y efecto, así como el color de relleno del cuadro de texto de las capas de texto.

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de color gris, RGB o CMYK, con o sin alfa. </p> </td> 
 </tr> 
</table>

En el caso de las capas de imagen y texto, `color=` rellena las áreas transparentes y semiopacas dentro del rectángulo delimitador de la capa con el color especificado* antes* `rotate=` y `extend=` se aplican.

## Propiedades {#section-d6e74c36a49547849212e4db8927e678}

Atributo de capa. Se aplica a la capa actual o a la capa 0 si `layer=comp`.

*`color`* se supone que existe en el espacio de color de trabajo correspondiente al tipo de píxel de *`color`*. *`color`* se convierte con precisión si la imagen de capa tiene un tipo de píxel diferente en el momento de la combinación.

## Predeterminado {#section-60611c72876b4c45b5c85ce35608e5ec}

No hay valor predeterminado para capas de efectos y colores sólidos; se debe especificar un color. El valor predeterminado es 0,0,0,0 (completamente transparente) para las capas de imagen y texto.

## Ejemplo {#section-2d090493f4ec4e188bbc5565aa151a05}

En el siguiente fragmento de plantilla establecemos el fondo del texto en un color opaco del 50 % y utilizamos el mismo color para añadir un borde semitransparente de 10 píxeles alrededor de la imagen de capa 2:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Véase también {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Gestión de color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
