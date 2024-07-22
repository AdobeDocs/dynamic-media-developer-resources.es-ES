---
description: textPs= implementa un algoritmo patentado de ajuste de copia que ajusta automáticamente los tamaños de fuente para llenar de forma óptima el área de texto con texto, minimizando el espacio adicional en la parte inferior y evitando el desbordamiento.
solution: Experience Manager
title: Copiado
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Copiado{#copy-fitting}

textPs= implementa un algoritmo patentado de ajuste de copia que ajusta automáticamente los tamaños de fuente para llenar de forma óptima el área de texto con texto, minimizando el espacio adicional en la parte inferior y evitando el desbordamiento.

El ajuste de copia se puede activar y controlar colectivamente para toda la capa de texto, en base a párrafo, incluso para un intervalo de texto individual.

Especifique el tamaño de fuente mínimo con `\fs` y el tamaño de fuente máximo con `\copyfit`. Se permite cualquier número de intervalos en la misma cadena RTF. Los tamaños de todos los rangos varían proporcionalmente, lo que garantiza que se mantengan las relaciones de tamaño de fuente deseadas.

`\copyfit` se considera un comando de formato de caracteres y tiene reglas de ámbito como `\fs` y `\b`.

Se deshabilitó el ajuste de copia al especificar `\copyfit` con un tamaño igual o menor que el especificado con `\fs`.

## Limitación del número de líneas {#section-e5aee0f039e04842afc3d6884ed681ac}

Además de especificar el intervalo de tamaños de fuente, el comportamiento del algoritmo de ajuste de copia se puede controlar aún más con los comandos `\copyfitlines` o `\copyfitmaxlines`, que limitan el número de líneas que genera el algoritmo. Ambos comandos aceptan un parámetro de recuento de líneas o 0, para no limitar el número de líneas en la región de ajuste de copia.

`\copyfitlines` permite que el texto se desborde a líneas adicionales cuando no cabe en el número de líneas especificado. Siempre se respetan los saltos de línea explícitos en el segmento de texto que se va a copiar.

`\copyfitmaxlines` siempre trunca las líneas de salida adicionales que exceden el límite especificado. Nunca se supera el número de líneas especificado, aunque haya saltos de línea explícitos. Para esta versión del servicio de imágenes, no puede haber más de marcadores N-1 `\line` en la extensión de texto ajustada a la copia. El comportamiento es indefinido si se supera este límite.

## Ejemplos {#section-f4ddbbfade444560be30a813d90c2c1b}

En los ejemplos siguientes se supone que los cuerpos de texto se proporcionan con variables denominadas *[!DNL $A$]*, *[!DNL $B$]* y *[!DNL $C$]*.

**Mantenga la misma relación entre los tamaños de fuente en todo el intervalo:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* siempre se representa el doble de grande que el resto del texto. Cuando se especifica mucho texto, *[!DNL $A$]* y *[!DNL $C$]* se representan con `\fs10` y *[!DNL $B$]* con `\fs20`. Con poco texto, *[!DNL $A$]* y *[!DNL $C$]* utilizan `\fs100` y *[!DNL $B$]* `\fs200`.

**Converge a un tamaño de fuente grande común si solo se dibuja una pequeña cantidad de texto:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

En el extremo más pequeño del intervalo, *[!DNL $B$]* se representa con `\fs20`, el doble de grande que *[!DNL $A$]* y *[!DNL $C$]* en `\fs10`. Todo el texto se dibuja en `\fs100` (50 puntos) en el extremo opuesto del intervalo.

**Cambiar a un tamaño de fuente pequeño común si se va a representar mucho texto:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Todo el texto se dibuja con \fs10 en el extremo pequeño del intervalo, mientras que en el mayor, *[!DNL $A$]* y *[!DNL $C$]* se representan con `\fs100` y *[!DNL $B$]* con `\fs200`.

**Deshabilitar el ajuste de copia para un intervalo de texto interno:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

El tamaño de fuente de *[!DNL $A$]* y *[!DNL $C$]* puede variar entre 10 y 100, mientras que *[!DNL $B$]* siempre se representa con `\fs50`.

**Limitar el resultado a una sola línea, incluso si hay más espacio vertical disponible, pero permitir que se desborde a líneas adicionales si se especifica demasiado texto para caber en una sola línea en `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limita el resultado a una sola línea, incluso si hay más espacio vertical disponible. Si se especifica demasiado texto para caber en una sola línea en `\fs10`, se trunca:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
