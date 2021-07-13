---
description: Se envía una alerta de prioridad cuando el espacio libre en la pila de Java está por debajo del umbral especificado inmediatamente después de un ciclo de colección de residuos de Java.
solution: Experience Manager
title: Alerta de prioridad del espacio de montículos
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Alerta de prioridad del espacio de montículos{#heap-space-priority-alert}

Se envía una alerta de prioridad cuando el espacio libre en la pila de Java está por debajo del umbral especificado inmediatamente después de un ciclo de colección de residuos de Java.

Las alertas repetidas deben solucionarse aumentando el espacio de memoria de Java. Las incidencias posteriores de esta condición no dan como resultado una alerta por correo electrónico hasta que el periodo de retraso especificado con `AS::monitorAlertGenerator.heapSpaceResetInterval` haya caducado.
