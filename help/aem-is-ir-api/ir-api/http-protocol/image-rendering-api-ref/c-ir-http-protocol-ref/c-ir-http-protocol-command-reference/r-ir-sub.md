---
title: sub
description: Subselección. Permite aplicar diferentes materiales a diferentes áreas del objeto o grupo seleccionado y eliminar los materiales aplicados previamente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 7%

---

# sub{#sub}

Subselección. Permite aplicar diferentes materiales a diferentes áreas del objeto o grupo seleccionado y eliminar los materiales aplicados previamente.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Seleccionar toda la pared. </p> </td> 
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
  <td class="stentry"> <p>Seleccione el área del borde de la pared superior. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Seleccione el área del borde de la pared central. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Seleccione el área del borde de la pared inferior. </p> </td> 
 </tr> 
</table>

Actualmente solo es compatible con objetos de pared. Termina un MSS anterior e inicia un MSS nuevo para el material que se va a aplicar a la subselección especificada.

Un material especificado para la pared superior o inferior se aplica a toda la pared a menos que también se haya especificado un material diferente para la otra mitad de la pared.

## Propiedades {#section-b202139d6d0847cc8d520a154104ab9d}

Comando de selección; delimitador SMS.

## Predeterminado {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Véase también {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
