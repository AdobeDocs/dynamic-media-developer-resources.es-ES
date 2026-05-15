---
title: color
description: Color de capa. Especifica el color de primer plano y la opacidad de las capas de color sólido y efecto, así como el color de relleno del cuadro de texto de las capas de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
TQID: 'https://experienceleague.adobe.com/tjiZfVTztBPgsIYS1SGtVeBxo0Wq1q8Ur-kq3Xtm6og'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 202
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

Si hay capas de imagen y texto, `color=` rellena áreas transparentes y semiopacas dentro del rectángulo delimitador de la capa con el color especificado* antes de* aplicar `rotate=` y `extend=`.

## Propiedades {#section-d6e74c36a49547849212e4db8927e678}

Atributo de capa. Se aplica a la capa actual o a la capa 0 si `layer=comp`.

Se supone que el modificador *`color`* existe en el espacio de color de trabajo correspondiente al tipo de píxel de *`color`*. Y *`color`* se convierte con precisión si la imagen de la capa tiene un tipo de píxel diferente en el momento de la combinación.

## Predeterminado {#section-60611c72876b4c45b5c85ce35608e5ec}

No hay valor predeterminado para capas de efectos y colores sólidos; se debe especificar un color. El valor predeterminado es 0,0,0,0 (completamente transparente) para las capas de imagen y texto.

## Ejemplo {#section-2d090493f4ec4e188bbc5565aa151a05}

En el siguiente fragmento de plantilla, el fondo del texto se establece en un color opaco del 50 % y se utiliza el mismo color para añadir un borde semitransparente de 10 píxeles alrededor de la imagen de capa 2:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Véase también {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Administración de color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
