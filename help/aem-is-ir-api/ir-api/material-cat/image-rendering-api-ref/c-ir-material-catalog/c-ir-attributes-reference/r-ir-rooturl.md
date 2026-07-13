---
title: RootUrl
description: URL raíz para URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imagen relativas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
TQID: 'https://experienceleague.adobe.com/1wKgvbd1t4HyDlz-CTDkp2gQuryBJYfMyDG7SmVgNwE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 3%

---

# RootUrl{#rooturl}

URL raíz para URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imagen relativas. Se usa `attribute::RootUrl` en lugar de `attribute::RootPath` cuando {curly braces} encierra un valor `src=`.

## Propiedades {#section-69cd0f71ea614770a8778c745d23197a}

Valor de cadena de texto. Ruta de acceso raíz de URL absoluta, incluido el identificador de protocolo inicial. Se admiten los siguientes protocolos: HTTP, HTTPS y FTP.

## Predeterminado {#section-7a81569728474725a70f3a2cc4d48e85}

Se hereda de `default::RootUrl` si no se define. Si se definen pero están vacías, las direcciones URL relativas no son compatibles con este catálogo de materiales.

## Véase también {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [atributo:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)

