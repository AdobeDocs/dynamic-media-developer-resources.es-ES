---
title: Escala de miniaturas
description: El paso 2 de la transformación de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Escala de miniaturas{#thumbnail-scaling}

El paso 2 de la transformación de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).

* `2.` Si se especifica `size=`, ajuste la imagen (recortada) a la derecha `size=` mediante reglas de miniaturas. Si no se especifica `size=`, escale en función de `res=` o, si no se especifica `res=`, ajuste la imagen (recortada) a la derecha del lienzo según las reglas de miniaturas descritas a continuación.
