---
title: RootUrl
description: URL raíz para URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imagen relativas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# RootUrl{#rooturl}

URL raíz para URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imagen relativas. Se usa `attribute::RootUrl` en lugar de `attribute::RootPath` cuando un valor `src=` está entre { llaves }.

## Propiedades {#section-69cd0f71ea614770a8778c745d23197a}

Valor de cadena de texto. Ruta de acceso raíz de URL absoluta, incluido el identificador de protocolo inicial. Se admiten los siguientes protocolos: HTTP, HTTPS y FTP.

## Predeterminado {#section-7a81569728474725a70f3a2cc4d48e85}

Se hereda de `default::RootUrl` si no se define. Si se definen pero están vacías, las direcciones URL relativas no son compatibles con este catálogo de materiales.

## Véase también {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [atributo:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
