---
description: Ángulo de rotación del material. Define el ángulo de giro de los materiales.
seo-description: Ángulo de rotación del material. Define el ángulo de giro de los materiales.
seo-title: rotar
solution: Experience Manager
title: rotar
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 7%

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
