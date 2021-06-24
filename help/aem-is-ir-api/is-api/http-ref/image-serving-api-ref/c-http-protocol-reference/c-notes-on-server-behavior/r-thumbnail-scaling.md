---
description: El paso 2 de las transformaciones de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).
solution: Experience Manager
title: Escalado de miniatura
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Escalado de miniatura{#thumbnail-scaling}

El paso 2 de las transformaciones de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).

* `2.` Si  `size=` se especifica, ajuste la imagen (recortada) al  `size=` recto mediante reglas de miniaturas. Si no se especifica `size=`, ajuste la escala basada en `res=` o, si no se especifica `res=`, ajuste la imagen (recortada) en el anillo del lienzo utilizando las reglas de miniaturas que se describen a continuación.
