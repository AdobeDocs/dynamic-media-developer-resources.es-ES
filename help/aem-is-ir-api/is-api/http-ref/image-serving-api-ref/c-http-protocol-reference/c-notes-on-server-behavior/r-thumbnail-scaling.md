---
description: El paso 2 de las transformaciones de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).
solution: Experience Manager
title: Escalado de miniatura
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Escala de miniaturas{#thumbnail-scaling}

El paso 2 de las transformaciones de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).

* `2.` Si  `size=` se especifica, ajuste la imagen (recortada) al  `size=` recto mediante reglas de miniaturas. Si no se especifica `size=`, ajuste la escala basada en `res=` o, si no se especifica `res=`, ajuste la imagen (recortada) en el anillo del lienzo utilizando las reglas de miniaturas que se describen a continuación.

