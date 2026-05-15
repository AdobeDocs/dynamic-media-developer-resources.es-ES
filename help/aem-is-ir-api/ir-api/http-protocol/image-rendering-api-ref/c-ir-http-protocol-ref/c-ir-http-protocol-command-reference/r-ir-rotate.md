---
title: rotar
description: Ángulo de rotación del material. Define el ángulo de rotación de los materiales.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
TQID: 'https://experienceleague.adobe.com/prSGGMuV4SpFfhd8uCVzMRGpr-VBpowxE-UagKtpnqI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 4%

---

# rotar{#rotate}

Ángulo de rotación del material. Define el ángulo de rotación de los materiales.

` rotate= *`ángulo`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> ángulo </span> </p> </td> 
  <td class="stentry"> <p>Ángulo de rotación en grados (real). </p> </td> 
 </tr> 
</table>

Rotar los materiales de textura repetibles (excepto los fondos de pantalla) por múltiplos de 45° cuando se aplican a objetos planos o objetos planos.

Rotar los materiales de textura repetibles en ángulos arbitrarios cuando se aplican a los objetos de línea de flujo y esbozo.

Rotar los materiales de la calcomanía por ángulos arbitrarios.

Los ángulos positivos giran en sentido horario. La textura o la calcomanía giran alrededor del punto de anclaje (`anchor=`); el punto de anclaje permanece alineado con el origen del objeto de destino.

## Propiedades {#section-ad4d07897ca24f63af1a4062f8618e36}

Atributo de material. Ignorado por los materiales de tratamiento de color sólido, papel tapiz, gabinete y ventana. *`angle`* Debe ser un múltiplo de 45 para texturas repetibles, a menos que se aplique a objetos de línea de flujo o boceto.

## Predeterminado {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, sin rotación.

## Véase también {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
