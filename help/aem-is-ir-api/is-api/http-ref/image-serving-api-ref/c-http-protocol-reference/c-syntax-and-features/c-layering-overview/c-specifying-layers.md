---
description: En la secuencia de comandos URL o Modificador de catálogo, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la URL.
solution: Experience Manager
title: Especificación de capas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Especificación de capas{#specifying-layers}

En la secuencia de comandos URL o catalog::Modifier, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la URL.

Todos los comandos de la secuencia de definición de la capa se asocian a la capa.

El comando `layer=` especifica un número de capa, que debe ser un número entero 0 o superior. Todos los comandos de las secuencias de definición de capa con el mismo número de capa se aplican a la misma capa. Si el mismo comando se ejecuta más de una vez, prevalecerá la última instancia.
