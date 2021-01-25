---
description: En la secuencia de comandos URL o Modificador de catálogo, una secuencia de definición de capa inicio con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la dirección URL.
seo-description: En la secuencia de comandos URL o Modificador de catálogo, una secuencia de definición de capa inicio con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la dirección URL.
seo-title: Especificación de capas
solution: Experience Manager
title: Especificación de capas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# Especificación de capas{#specifying-layers}

En la secuencia de comandos URL o catálogo::Modifier, una secuencia de definición de capa inicio con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la URL.

Todos los comandos de la secuencia de definición de capa están asociados a la capa.

El comando `layer=` especifica un número de capa, que debe ser un número entero 0 o mayor. Todos los comandos de las secuencias de definición de capa con el mismo número de capa se aplican a la misma capa. Si el mismo comando se produce más de una vez, prevalecerá la última instancia.
