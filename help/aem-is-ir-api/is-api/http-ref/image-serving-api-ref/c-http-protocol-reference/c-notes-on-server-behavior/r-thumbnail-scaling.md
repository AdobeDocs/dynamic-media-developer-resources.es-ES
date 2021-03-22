---
description: El paso 2 de las transformaciones de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).
seo-description: El paso 2 de las transformaciones de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).
seo-title: Escalado de miniatura
solution: Experience Manager
title: Escalado de miniatura
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Escala de miniaturas{#thumbnail-scaling}

El paso 2 de las transformaciones de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).

* `2.` Si  `size=` se especifica, ajuste la imagen (recortada) al  `size=` recto mediante reglas de miniaturas. Si no se especifica `size=`, ajuste la escala basada en `res=` o, si no se especifica `res=`, ajuste la imagen (recortada) en el anillo del lienzo utilizando las reglas de miniaturas que se describen a continuación.

