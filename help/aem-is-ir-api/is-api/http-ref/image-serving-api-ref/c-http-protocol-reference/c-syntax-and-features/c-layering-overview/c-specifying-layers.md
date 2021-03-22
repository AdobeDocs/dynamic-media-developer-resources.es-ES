---
description: En la secuencia de comandos del modificador de la dirección URL o del catálogo, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la dirección URL.
seo-description: En la secuencia de comandos del modificador de la dirección URL o del catálogo, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la dirección URL.
seo-title: Especificación de capas
solution: Experience Manager
title: Especificación de capas
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Especificación de capas{#specifying-layers}

En la secuencia de comandos URL o catalog::Modifier, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la dirección URL.

Todos los comandos de la secuencia de definición de capa están asociados a la capa.

El comando `layer=` especifica un número de capa, que debe ser un número entero 0 o mayor. Todos los comandos de las secuencias de definición de capa con el mismo número de capa se aplican a la misma capa. Si el mismo comando ocurre más de una vez, prevalecerá la última instancia.
