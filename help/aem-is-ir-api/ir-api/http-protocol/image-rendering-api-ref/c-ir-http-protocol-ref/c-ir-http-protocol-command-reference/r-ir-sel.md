---
title: sel
description: Seleccionar objeto por ubicación de píxeles.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 1%

---

# sel{#sel}

Seleccionar objeto por ubicación de píxeles.

` sel= *`x`*, *`y`*[, *`nivel`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>Elija las coordenadas de ubicación en píxeles (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nivel </span> </p> </td> 
  <td class="stentry"> <p>Nivel de grupo (int). </p> </td> 
 </tr> 
</table>

Selecciona el grupo u objeto en las coordenadas de píxel especificadas por *`x, y`* e inicia un nuevo MSS. Si no hay ningún objeto seleccionable en la ubicación de picking, o si la ubicación de picking no es válida, se realiza la acción especificada por `attribute::OnFailSel`.

*`level`* Especifica si se selecciona el grupo exterior o se profundiza en un grupo u objeto anidado. Si no se especifica *`level`*, se selecciona el grupo exterior. Establezca el valor en 1 para seleccionar un nivel de grupo por debajo del grupo exterior. Defina un número elevado (por ejemplo, 99) para seleccionar el objeto o grupo que se pueda seleccionar más íntimamente.

## Propiedades {#section-8f27e84d88734a62a5e398e0c9972bdc}

Comando de selección; delimitador SMS. La selección de objetos es persistente hasta que se selecciona otro objeto, ya sea con `obj=` o `sel=`.

*`x, y`* debe estar en el rango de 0, 0 (esquina superior izquierda de la imagen) a *`wid`*-1, *`hei`*-1 (esquina inferior derecha de la imagen), donde *`wid`* y *`hei`* es el tamaño de la vista de viñeta sin escalar.

Si se especifica, *`level`* debe ser 0 o mayor.

## Predeterminado {#section-e13c705a3e76468894b4ec190ed8a893}

Ninguno para *`x, y`*. *`level`* toma el valor predeterminado de 0.

## Véase también {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [atributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [atributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
