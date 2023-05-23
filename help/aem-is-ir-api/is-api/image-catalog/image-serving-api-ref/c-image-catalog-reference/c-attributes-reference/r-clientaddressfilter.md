---
description: Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o rangos de direcciones.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o rangos de direcciones.

Cuando se especifica, se rechazan las solicitudes a este catálogo de imágenes que se originan desde un cliente con una dirección IP no incluida.

## Propiedades {#section-d785265988324af68835410c9ba54147}

Lista separada por comas de direcciones IP con máscaras de red opcionales (se utiliza la notación CIDR):

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>Dirección IP en <span class="varname"> ddd.ddd.ddd.ddd</span> formato. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> máscara de red</span> </p></td> 
  <td class="stentry"> <p>Máscara de red (0...32). </p></td> 
 </tr> 
</table>

Este atributo se ignora cuando una regla de preprocesamiento con un `<addressfilter>` se aplica el elemento.

## Predeterminado {#section-de26e8c9225745e985e4beac1f03f4f6}

Heredado de `default::AddressFilter` si no se define o si está vacío.

## Ejemplos {#section-a955314d2b6a4213a16c12a8b18d8627}

Sin restricciones de acceso: `0.0.0.0/0`

Conceder acceso a todas las direcciones a partir de 192: `192.0.0.0/8`

Conceder acceso a los 512 hosts con direcciones entre 192.168.12.0 y 192.168.13.255: `192.168.12.0/23`

Conceder acceso a una sola dirección IP: `192.168.2.117` o `192.168.2.117/32`

## Véase también {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
