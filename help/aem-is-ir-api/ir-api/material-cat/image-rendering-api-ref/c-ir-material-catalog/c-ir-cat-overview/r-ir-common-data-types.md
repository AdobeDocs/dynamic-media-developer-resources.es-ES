---
description: Los atributos y campos del catálogo pueden contener datos de uno de los siguientes tipos.
seo-description: Los atributos y campos del catálogo pueden contener datos de uno de los siguientes tipos.
seo-title: Tipos de datos comunes
solution: Experience Manager
title: Tipos de datos comunes
topic: Scene7 Image Serving - Image Rendering API
uuid: b36cf09d-dee2-4e8b-9500-e8fa4c5c112f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Tipos de datos comunes{#common-data-types}

Los atributos y campos del catálogo pueden contener datos de uno de los siguientes tipos.

**Color**

Valor de color. Valor RGB hexadecimal y empaquetado, opcionalmente precedido por 0x. Por ejemplo, el valor RGB `128,255,0` se puede especificar como `0x80ff00` o `80ff00`.

**Indicador**

`0`=false,  `1`=true, cualquier otro valor significa desconocido o no especificado.

**Enum**

0 indica un valor desconocido o no especificado, igual que un campo vacío. Los valores válidos `enum` son números enteros consecutivos, comenzando por 1.

**Número entero**

Valor entero firmado (por ejemplo: 0, -12, 34). 0 o valores negativos pueden tener un significado especial.

**Número real**

Valor de coma flotante firmado (p. ej. `0, 12.5, 245 , -2.34e4`). 0 o valores negativos pueden tener un significado especial.

**Cadena de texto**

Los delimitadores de cadena son opcionales, a menos que la cadena contenga caracteres `<CR>`, `<LF>` o `<TAB>`. Las comillas simples y las comillas de doble pueden utilizarse como delimitadores. Si se utilizan comillas, las comillas de este tipo incrustadas dentro de la cadena deben separarse mediante dos comillas consecutivas (p. ej. &#39; `This month''s Special`&#39;).
