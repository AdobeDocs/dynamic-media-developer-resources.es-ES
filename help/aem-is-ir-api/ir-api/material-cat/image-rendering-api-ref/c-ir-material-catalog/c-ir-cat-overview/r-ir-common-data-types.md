---
title: Tipos de datos comunes
description: Los atributos y campos del catálogo pueden contener datos de uno de los siguientes tipos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# Tipos de datos comunes{#common-data-types}

Los atributos y campos del catálogo pueden contener datos de uno de los siguientes tipos.

**Color**

Valor de color. Valor de RGB hexadecimal empaquetado, opcionalmente precedido de 0x. Por ejemplo, el valor de RGB `128,255,0` se puede especificar como `0x80ff00` o `80ff00`.

**Indicador**

`0`=false, `1`=true, cualquier otro valor significa desconocido o no especificado.

**Enum**

`0` indica un valor desconocido o no especificado, igual que un campo vacío. Válido `enum` son números enteros consecutivos, comenzando por 1.

**Número entero**

Valor entero firmado (por ejemplo `0, -12, 34`). `0` o los valores negativos pueden tener un significado especial.

**Número real**

Valor de coma flotante firmado (por ejemplo, `0, 12.5, 245 , -2.34e4`). 0 o los valores negativos pueden tener un significado especial.

**Cadena de texto**

Los delimitadores de cadena son opcionales, a menos que la cadena contenga `<CR>`, `<LF>`o `<TAB>` caracteres. Las comillas simples y dobles pueden utilizarse como delimitadores. Si se utilizan comillas, cualquier comillas de este tipo incrustadas en la cadena debe omitirse utilizando dos comillas consecutivas (por ejemplo, &#39; `This month''s Special`&quot;).
