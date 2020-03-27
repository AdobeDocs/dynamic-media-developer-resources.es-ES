---
description: textPs= implementa un algoritmo propietario de ajuste de copia que automáticamente ajusta el tamaño o tamaños de fuente para llenar de forma óptima el área de texto con texto, minimizando el espacio adicional en la parte inferior y evitando el desbordamiento.
seo-description: textPs= implementa un algoritmo propietario de ajuste de copia que automáticamente ajusta el tamaño o tamaños de fuente para llenar de forma óptima el área de texto con texto, minimizando el espacio adicional en la parte inferior y evitando el desbordamiento.
seo-title: Ajuste de copia
solution: Experience Manager
title: Ajuste de copia
topic: Scene7 Image Serving - Image Rendering API
uuid: c3ddbf1f-c724-4436-96ff-2c616dfd355d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ajuste de copia{#copy-fitting}

textPs= implementa un algoritmo propietario de ajuste de copia que automáticamente ajusta el tamaño o tamaños de fuente para llenar de forma óptima el área de texto con texto, minimizando el espacio adicional en la parte inferior y evitando el desbordamiento.

El ajuste de copia se puede habilitar y controlar de forma colectiva para toda la capa de texto, en base a párrafos, incluso para un espacio de texto individual.

Especifique el tamaño mínimo de fuente con `\fs` y el tamaño máximo de fuente con `\copyfit`. Se permite cualquier número de intervalos en la misma cadena RTF. Los tamaños de todos los rangos varían proporcionalmente, lo que garantiza que se mantengan las proporciones de tamaño de fuente deseadas.

`\copyfit` se considera un comando de formato de caracteres y tiene reglas de ámbito como `\fs` y `\b`.

La conexión de copia se desactiva especificando `\copyfit` un tamaño igual o inferior al tamaño especificado con `\fs`.

## Limitar el número de líneas {#section-e5aee0f039e04842afc3d6884ed681ac}

Además de especificar el rango de tamaños de fuente, el comportamiento del algoritmo de ajuste de copia se puede controlar con los comandos `\copyfitlines` o `\copyfitmaxlines` , que limitan el número de líneas que generará el algoritmo. Ambos comandos aceptan un parámetro de recuento de líneas o 0, para no limitar el número de líneas en la región con copia.

`\copyfitlines` permite que el texto se desborde a líneas adicionales cuando no se ajusta al número especificado de líneas. Siempre se respetan los saltos de línea explícitos en el segmento de texto que se va a copiar.

`\copyfitmaxlines` siempre trunca las líneas de salida adicionales que exceden el límite especificado. El número especificado de líneas nunca se superará, aunque haya saltos de línea explícitos. Para esta versión del servicio de imágenes, no pueden estar presentes más de marcadores N-1 `\line` en el espacio de texto con copia. El comportamiento no está definido si se supera este límite.

## Ejemplos {#section-f4ddbbfade444560be30a813d90c2c1b}

Los siguientes ejemplos suponen que los cuerpos de texto tienen variables con nombres *[!DNL $A$]*, *[!DNL $B$]* y *[!DNL $C$]*.

**Mantenga la misma relación entre los tamaños de fuente en todo el rango:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* siempre se procesará el doble de grande que el resto del texto. Cuando se especifica mucho texto, *[!DNL $A$]* y *[!DNL $C$]* se procesa con `\fs10` y *[!DNL $B$]* con `\fs20`. Con poco texto, *[!DNL $A$]* y *[!DNL $C$]* utilizará `\fs100` y *[!DNL $B$]*`\fs200`.

**Convierta a un tamaño de fuente grande común si solo se dibuja una pequeña cantidad de texto:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

En el extremo más pequeño del rango, *[!DNL $B$]* se procesará con `\fs20`, el doble de grande *[!DNL $A$]* y *[!DNL $C$]* en `\fs10`. Todo el texto se dibujará en `\fs100` (50 puntos) en el extremo opuesto del rango.

**Convierta a un tamaño de fuente pequeño común si se va a representar mucho texto:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Todo el texto se dibuja con \fs10 en el extremo pequeño del rango, mientras que en el extremo mayor, *[!DNL $A$]* y *[!DNL $C$]* se procesa con `\fs100` y *[!DNL $B$]* con `\fs200`.

**Deshabilitar el ajuste de copia para un espacio de texto interno:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

El tamaño de fuente *[!DNL $A$]* y *[!DNL $C$]* puede variar entre 10 y 100, mientras que siempre *[!DNL $B$]* se procesa con `\fs50`.

**Limite el resultado a una sola línea, aunque haya más espacio vertical disponible, pero permita que se desborde a líneas adicionales si se especifica demasiado texto para que quepa en una sola línea en`\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limite el resultado a una sola línea, incluso si hay más espacio vertical disponible. Si se especifica demasiado texto para que quepa en una sola línea,`\fs10`se truncará:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
