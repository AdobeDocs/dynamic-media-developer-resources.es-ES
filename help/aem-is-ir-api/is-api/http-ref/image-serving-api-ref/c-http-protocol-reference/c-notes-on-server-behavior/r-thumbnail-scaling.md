---
description: El paso 2 de la transformación de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).
solution: Experience Manager
title: Escala de miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# Escala de miniaturas{#thumbnail-scaling}

El paso 2 de la transformación de la capa de imagen se modifica de la siguiente manera para las miniaturas (es decir, si req=tmb).

* `2.` If `size=` se ha especificado, ajuste la imagen (recortada) en el `size=` corregir mediante reglas de miniaturas. If `size=` no especificado, escala basada en `res=`, o, si `res=` no se ha especificado, ajuste la imagen (recortada) en la derecha del lienzo según las reglas de miniaturas indicadas a continuación.
