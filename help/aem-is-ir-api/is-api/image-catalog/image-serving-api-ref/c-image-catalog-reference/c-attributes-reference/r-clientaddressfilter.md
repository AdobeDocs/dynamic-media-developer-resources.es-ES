---
description: Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o intervalos de direcciones.
seo-description: Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o intervalos de direcciones.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a557795-0caf-4b5f-974e-fb4c1481a83c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o intervalos de direcciones.

Cuando se especifique, se rechazarán las solicitudes a este catálogo de imágenes que procedan de un cliente en una dirección IP no incluida en la lista.

## Propiedades {#section-d785265988324af68835410c9ba54147}

lista separada por comas de direcciones IP con máscaras de red opcionales (se utiliza notación CIDR):

`*`ipAddress`*` `[`/ *`netmask`*`]`*`[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>Dirección IP en <span class="varname"> formato ddd.ddd.ddd</span> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmask</span> </p></td> 
  <td class="stentry"> <p>Máscara de red (0...32). </p></td> 
 </tr> 
</table>

Este atributo se omite cuando se aplica una regla de preprocesamiento con un `<addressfilter>` elemento.

## Predeterminado {#section-de26e8c9225745e985e4beac1f03f4f6}

Se hereda de `default::AddressFilter` si no está definida o si está vacía.

## Ejemplos {#section-a955314d2b6a4213a16c12a8b18d8627}

Sin restricciones de acceso: `0.0.0.0/0`

Conceder acceso a todas las direcciones a partir de 192: `192.0.0.0/8`

Conceder acceso a los 512 hosts con direcciones entre 192.168.12.0 y 192.168.13.255: `192.168.12.0/23`

Conceder acceso a una sola dirección IP: `192.168.2.117` o `192.168.2.117/32`

## Véase también {#section-4ea89a7d82e14a4a800487d2d8801465}

[direcsfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
