---
title: DigimarcInfo
description: Información de imagen de Digimarc. Habilita la incrustación de Digimarc y especifica el tipo de marca de agua y los datos específicos de imagen asociados.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 87f4d8f0-02b9-4511-9151-89c58116c78d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---

# DigimarcInfo{#digimarcinfo}

Información de imagen de Digimarc. Habilita la incrustación de Digimarc y especifica el tipo de marca de agua y los datos específicos de imagen asociados.

## Propiedades {#section-62af219e8bac422b8541841221c9ce4f}

Cuatro valores enteros, separados por comas.

`*`type`*, *`flags`*, *`val1`*, *`val2`*`

`*`type`*` habilita la incrustación de Digimarc y especifica el tipo de marca de agua:

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> tipo</span> </span> </p> </th> 
   <th class="entry"> <p><b>Tipo de filigrana</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Básico. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>ID de imagen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>ID de transacción. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Años de copyright. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`flags`*` es un campo de bits con tres valores. Establezca el bit 0 para indicar contenido protegido contra copia, el bit 1 para indicar contenido restringido y el bit 2 para indicar contenido adulto:

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> indicadores</span> </span> </p> </th> 
   <th class="entry"> <p><b>Descripción</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Protegido contra copia. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Restringido. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Protegido contra copias, restringido. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Contenido adulto. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>Contenido para adultos protegido por copia. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>Contenido restringido para adultos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>Contenido maduro, restringido y protegido contra copias. </p> </td> 
  </tr> 
 </tbody> 
</table>

La interpretación de `*`val1`*` y `*`val2`*` depende de `*`type`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> tipo</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1 </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2 </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>No se usa. </p> </td> 
   <td> <p>No se usa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>No se usa. </p> </td> 
   <td> <p>No se usa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>ID de imagen. </p> </td> 
   <td> <p>No se usa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>ID de transacción. </p> </td> 
   <td> <p>No se usa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Primer año de copyright. </p> </td> 
   <td> <p>Segundo año de copyright. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Predeterminado {#section-4bb97e5f79074be89cc691e73449eb43}

Se hereda de attribute::DigimarcInfo si el campo no está presente o si está vacío.

## Ejemplos {#section-0f14727a0a2a408781c9df71fed7f42d}

&quot;0,0,0,0&quot; desactiva la marca de agua Digimarc para esta imagen.

&quot;1,5,0,0&quot; especifica una marca de agua básica con el indicador de contenido para adultos y protegido contra copias establecido.

&quot;2,0,4567,0&quot; especifica una marca de agua con un ID de imagen.

&quot;3,2,56483,0&quot; especifica una marca de agua con un ID de transacción y el indicador de contenido restringido establecido.

&quot;4,0,1998,2001&quot; especifica una marca de agua con años de copyright.

## Véase también {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) , [attribute::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
