---
description: En la secuencia de comandos URL o Modificador de catálogo, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la URL.
solution: Experience Manager
title: Especificación de capas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
TQID: 'https://experienceleague.adobe.com/jNFpOYrBFWWc53JvzwENSjpM-SkIpenxxWPUgGX-p0Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# Especificación de capas{#specifying-layers}

En la secuencia de comandos URL o catalog::Modifier, una secuencia de definición de capa comienza con el comando layer= y termina con otro comando layer=, un comando effect= o el final de la URL.

Todos los comandos de la secuencia de definición de la capa se asocian a la capa.

El comando `layer=` especifica un número de capa, que debe ser un número entero 0 o superior. Todos los comandos de las secuencias de definición de capa con el mismo número de capa se aplican a la misma capa. Si el mismo comando se ejecuta más de una vez, prevalecerá la última instancia.
