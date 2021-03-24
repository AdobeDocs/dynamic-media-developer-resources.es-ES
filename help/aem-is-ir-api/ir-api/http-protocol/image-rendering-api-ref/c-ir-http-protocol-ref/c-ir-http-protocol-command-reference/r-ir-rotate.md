---
description: Ángulo de rotación del material. Define el ángulo de giro de los materiales.
solution: Experience Manager
title: rotar
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 6%

---


# rotate{#rotate}

Ángulo de rotación del material. Define el ángulo de giro de los materiales.

` rotate= *`Ángulo`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Ángulo </span> </p> </td> 
  <td class="stentry"> <p>Ángulo de rotación en grados (real). </p> </td> 
 </tr> 
</table>

Gire los materiales de textura repetibles (excepto los fondos de pantalla) por múltiplos de 45 grados cuando se apliquen a objetos planos u objetos planos.

Girar los materiales de textura repetibles por ángulos arbitrarios cuando se aplican a objetos de línea de flujo y esbozo.

Rotar los materiales de calco por ángulos arbitrarios.

Los ángulos positivos rotan en el sentido de las agujas del reloj. La textura o calcomanía gira alrededor del punto de ancla ( `anchor=`); el punto de ancla permanece alineado con el origen del objeto de destino.

## Propiedades {#section-ad4d07897ca24f63af1a4062f8618e36}

Atributo de material. Ignorado por materiales de color sólido, papel tapiz, gabinete y tratamiento de ventanas. *`angle`* debe ser un múltiplo de 45 para texturas repetibles, a menos que se aplique a los objetos de línea de flujo o de esbozo.

## Predeterminado {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, sin rotación.

## Véase también {#section-f73c00e9368b478dac1fd15bb4367a12}

[delimitador=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
