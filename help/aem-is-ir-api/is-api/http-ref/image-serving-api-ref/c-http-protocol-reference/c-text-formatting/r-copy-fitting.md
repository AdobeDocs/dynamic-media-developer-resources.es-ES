---
description: textPs= implementa un algoritmo de ajuste de copia patentado que ajustará automáticamente el tamaño de fuente para llenar de forma óptima el área de texto con texto, minimizando el espacio adicional en la parte inferior y evitando el desbordamiento.
seo-description: textPs= implementa un algoritmo de ajuste de copia patentado que ajustará automáticamente el tamaño de fuente para llenar de forma óptima el área de texto con texto, minimizando el espacio adicional en la parte inferior y evitando el desbordamiento.
seo-title: Ajuste de copia
solution: Experience Manager
title: Ajuste de copia
uuid: c3ddbf1f-c724-4436-96ff-2c616dfd355d
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 0%

---


# Ajuste de copia{#copy-fitting}

textPs= implementa un algoritmo de ajuste de copia patentado que ajustará automáticamente el tamaño de fuente para llenar de forma óptima el área de texto con texto, minimizando el espacio adicional en la parte inferior y evitando el desbordamiento.

El ajuste de copia se puede habilitar y controlar de forma colectiva para toda la capa de texto, en base a párrafos, incluso para un grupo de texto individual.

Especifique el tamaño mínimo de la fuente con `\fs` y el tamaño máximo de la fuente con `\copyfit`. Cualquier número de intervalos está permitido en la misma cadena RTF. Los tamaños de todos los rangos varían proporcionalmente, lo que garantiza que se mantengan las proporciones de tamaño de fuente deseadas.

`\copyfit` se considera un comando de formato de caracteres y tiene reglas de ámbito como  `\fs` y  `\b`.

La conexión de copia está deshabilitada al especificar `\copyfit` con un tamaño igual o menor que el tamaño especificado con `\fs`.

## Limitación del número de líneas {#section-e5aee0f039e04842afc3d6884ed681ac}

Además de especificar el rango de tamaños de fuente, el comportamiento del algoritmo de ajuste de copia se puede controlar aún más con los comandos `\copyfitlines` o `\copyfitmaxlines`, que limitan el número de líneas que generará el algoritmo. Ambos comandos aceptan un parámetro de recuento de líneas o 0, para no limitar el número de líneas en la región instalada en la copia.

`\copyfitlines` permite que el texto se desborde a líneas adicionales cuando no se ajusta al número especificado de líneas. Siempre se respetan los saltos de línea explícitos en el segmento de texto que se va a copiar.

`\copyfitmaxlines` siempre trunca las líneas de salida adicionales que exceden el límite especificado. El número especificado de líneas nunca se superará, aunque haya saltos de línea explícitos. Para esta versión de Image Serving, no pueden estar presentes más de marcadores N-1 `\line` en la extensión de texto instalada en la copia. El comportamiento no está definido si se supera este límite.

## Ejemplos {#section-f4ddbbfade444560be30a813d90c2c1b}

Los siguientes ejemplos suponen que los cuerpos de texto se proporcionan con variables denominadas *[!DNL $A$]*, *[!DNL $B$]* y *[!DNL $C$]*.

**Mantenga la misma relación entre los tamaños de fuente en todo el rango:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* siempre se procesa el doble de grande que el resto del texto. Cuando se especifica mucho texto, *[!DNL $A$]* y *[!DNL $C$]* se procesarán con `\fs10` y *[!DNL $B$]* con `\fs20`. Con poco texto, *[!DNL $A$]* y *[!DNL $C$]* utilizarán `\fs100` y *[!DNL $B$]* `\fs200`.

**Convierta a un tamaño de fuente grande común si solo se dibuja una pequeña cantidad de texto:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

En el extremo más pequeño del intervalo, *[!DNL $B$]* se procesará con `\fs20`, el doble de grande que *[!DNL $A$]* y *[!DNL $C$]* en `\fs10`. Todo el texto se dibuja en `\fs100` (50 puntos) en el extremo opuesto del rango.

**Convierta a un tamaño de fuente pequeño común si se va a procesar mucho texto:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Todo el texto se dibuja con \fs10 en el extremo pequeño del rango, mientras que en el extremo más grande, *[!DNL $A$]* y *[!DNL $C$]* se representan con `\fs100` y *[!DNL $B$]* con `\fs200`.

**Deshabilite el ajuste de copia para un intervalo de texto interno:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

El tamaño de fuente para *[!DNL $A$]* y *[!DNL $C$]* puede variar entre 10 y 100, mientras que *[!DNL $B$]* siempre se representa con `\fs50`.

**Limite el resultado a una sola línea, incluso si hay más espacio vertical disponible, pero permita que se desborde a líneas adicionales si se especifica demasiado texto para que quepa en una sola línea en  `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limite el resultado a una sola línea, incluso si hay más espacio vertical disponible. Si se especifica demasiado texto para que quepa en una sola línea en `\fs10`, se truncará:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
