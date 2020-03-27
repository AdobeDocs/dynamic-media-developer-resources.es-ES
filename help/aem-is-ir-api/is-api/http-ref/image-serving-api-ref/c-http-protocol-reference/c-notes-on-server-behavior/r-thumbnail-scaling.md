---
description: El paso 2 de las transformaciones de la capa de imagen se modifica como se indica a continuación para las miniaturas (es decir, si req=tmb).
seo-description: El paso 2 de las transformaciones de la capa de imagen se modifica como se indica a continuación para las miniaturas (es decir, si req=tmb).
seo-title: Escala de miniaturas
solution: Experience Manager
title: Escala de miniaturas
topic: Scene7 Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# Escala de miniaturas{#thumbnail-scaling}

El paso 2 de las transformaciones de la capa de imagen se modifica como se indica a continuación para las miniaturas (es decir, si req=tmb).

* `2.` Si `size=` se especifica, ajuste la imagen (recortada) al `size=` rectángulo con las reglas de miniatura. Si no `size=` se especifica, la escala basada en `res=`o, si no `res=` se especifica, ajuste la imagen (recortada) en el rectángulo del lienzo utilizando las reglas de miniaturas que se describen a continuación.

