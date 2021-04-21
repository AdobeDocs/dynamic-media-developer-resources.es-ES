---
description: URL raíz para direcciones URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imágenes relativas. se usa el atributo RootUrl en lugar del atributo RootPath cuando { curly braces } incluye un valor src=.
solution: Experience Manager
title: RootUrl *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# RootUrl *{#rooturl}

URL raíz para direcciones URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imágenes relativas. attribute::RootUrl se utiliza en lugar de attribute::RootPath cuando { curly braces } incluye un valor src=.

## Propiedades {#section-69cd0f71ea614770a8778c745d23197a}

Valor de cadena de texto. Ruta raíz de URL absoluta, incluido el identificador de protocolo inicial. Se admiten los siguientes protocolos: HTTP, HTTPS y FTP.

## Predeterminado {#section-7a81569728474725a70f3a2cc4d48e85}

Se hereda de `default::RootUrl` si no se define. Si se define pero está vacío, las direcciones URL relativas no son compatibles con este catálogo de materiales.

## Véase también {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [attribute:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
