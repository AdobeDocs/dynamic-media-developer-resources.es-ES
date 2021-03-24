---
description: En la secuencia de comandos del modificador de la dirección URL o del catálogo, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la dirección URL.
solution: Experience Manager
title: Especificación de capas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Especificación de capas{#specifying-layers}

En la secuencia de comandos URL o catalog::Modifier, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la dirección URL.

Todos los comandos de la secuencia de definición de capa están asociados a la capa.

El comando `layer=` especifica un número de capa, que debe ser un número entero 0 o mayor. Todos los comandos de las secuencias de definición de capa con el mismo número de capa se aplican a la misma capa. Si el mismo comando ocurre más de una vez, prevalecerá la última instancia.
