---
description: En la secuencia de comandos del modificador de la dirección URL o del catálogo, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la dirección URL.
solution: Experience Manager
title: Especificación de capas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Especificación de capas{#specifying-layers}

En la secuencia de comandos URL o catalog::Modifier, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la dirección URL.

Todos los comandos de la secuencia de definición de capa están asociados a la capa.

El comando `layer=` especifica un número de capa, que debe ser un número entero 0 o mayor. Todos los comandos de las secuencias de definición de capa con el mismo número de capa se aplican a la misma capa. Si el mismo comando ocurre más de una vez, prevalecerá la última instancia.
