---
title: rotar
description: Ángulo de rotación del material. Define el ángulo de rotación de los materiales.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# rotar{#rotate}

Ángulo de rotación del material. Define el ángulo de rotación de los materiales.

` rotate= *`Ángulo`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Ángulo </span> </p> </td> 
  <td class="stentry"> <p>Ángulo de rotación en grados (real). </p> </td> 
 </tr> 
</table>

Rotar los materiales de textura repetibles (excepto los fondos de pantalla) por múltiplos de 45° cuando se aplican a objetos planos o objetos planos.

Rotar los materiales de textura repetibles en ángulos arbitrarios cuando se aplican a los objetos de línea de flujo y esbozo.

Rotar los materiales de la calcomanía por ángulos arbitrarios.

Los ángulos positivos giran en sentido horario. La textura o calcomanía gira alrededor del punto de anclaje ( `anchor=`); el punto de ancla permanece alineado con el origen del objeto de destino.

## Propiedades {#section-ad4d07897ca24f63af1a4062f8618e36}

Atributo de material. Ignorado por los materiales de tratamiento de color sólido, papel tapiz, gabinete y ventana. *`angle`* Debe ser un múltiplo de 45 para texturas repetibles, a menos que se aplique a objetos de línea de flujo o boceto.

## Predeterminado {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, sin rotación.

## Véase también {#section-f73c00e9368b478dac1fd15bb4367a12}

[delimitador=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
