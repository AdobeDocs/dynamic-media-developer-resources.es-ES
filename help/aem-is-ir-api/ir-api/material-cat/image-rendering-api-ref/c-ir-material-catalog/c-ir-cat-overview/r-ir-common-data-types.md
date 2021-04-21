---
description: Los atributos y campos del catálogo pueden contener datos de uno de los siguientes tipos.
solution: Experience Manager
title: Tipos de datos comunes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 1%

---


# Tipos de datos comunes{#common-data-types}

Los atributos y campos del catálogo pueden contener datos de uno de los siguientes tipos.

**Color**

Valor de color. Valor RGB hexadecimal empaquetado, opcionalmente precedido de 0x. Por ejemplo, el valor RGB `128,255,0` se puede especificar como `0x80ff00` o `80ff00`.

**Indicador**

`0`=false,  `1`=true, cualquier otro valor significa desconocido o no especificado.

**Enum**

0 indica un valor desconocido o no especificado, igual que un campo vacío. Los valores válidos `enum` son números enteros consecutivos, que comienzan por 1.

**Número entero**

Valor entero firmado (por ejemplo, 0, -12, 34). 0 o los valores negativos pueden tener un significado especial.

**Número real**

Valor de coma flotante firmado (p. ej. `0, 12.5, 245 , -2.34e4`). 0 o los valores negativos pueden tener un significado especial.

**Cadena de texto**

Los delimitadores de cadena son opcionales, a menos que la cadena contenga caracteres `<CR>`, `<LF>` o `<TAB>`. Las comillas simples y dobles pueden utilizarse como delimitadores. Si se utilizan comillas, cualquier comillas de este tipo incrustadas en la cadena debe omitirse utilizando dos comillas consecutivas (por ejemplo, &#39; `This month''s Special`&#39;).
