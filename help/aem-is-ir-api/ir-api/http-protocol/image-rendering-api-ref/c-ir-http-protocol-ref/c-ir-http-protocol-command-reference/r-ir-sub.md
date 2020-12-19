---
description: Subselección. Permite aplicar diferentes materiales a diferentes áreas del objeto o grupo seleccionado, así como eliminar materiales aplicados anteriormente.
seo-description: Subselección. Permite aplicar diferentes materiales a diferentes áreas del objeto o grupo seleccionado, así como eliminar materiales aplicados anteriormente.
seo-title: sub
solution: Experience Manager
title: sub
topic: Scene7 Image Serving - Image Rendering API
uuid: cb9f4dc5-9d89-483a-ae72-b9076b27c57e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 7%

---


# sub{#sub}

Subselección. Permite aplicar diferentes materiales a diferentes áreas del objeto o grupo seleccionado, así como eliminar materiales aplicados anteriormente.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Seleccione toda la pared. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Seleccione la mitad superior de la pared. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Seleccione la mitad inferior de la pared. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Seleccione el área del borde superior de la pared. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Seleccione el área del borde central de la pared. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Seleccione el área del borde de la pared inferior. </p> </td> 
 </tr> 
</table>

Actualmente solo se admite para objetos de pared. Termina un MSS anterior y inicio un nuevo MSS para el material que se va a aplicar a la subselección especificada.

Un material especificado para la pared superior o inferior se aplicará a toda la pared a menos que se haya especificado un material diferente para la otra mitad de la pared.

## Propiedades {#section-b202139d6d0847cc8d520a154104ab9d}

Selección, comando; delimitador MSS.

## Predeterminado {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Véase también {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
