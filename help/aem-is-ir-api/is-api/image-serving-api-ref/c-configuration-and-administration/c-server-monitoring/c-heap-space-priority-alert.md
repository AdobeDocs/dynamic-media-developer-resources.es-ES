---
description: Se envía una alerta de prioridad cuando el espacio libre en el montón de Java está por debajo del umbral especificado inmediatamente después de un ciclo de recolección de elementos no utilizados de Java.
seo-description: Se envía una alerta de prioridad cuando el espacio libre en el montón de Java está por debajo del umbral especificado inmediatamente después de un ciclo de recolección de elementos no utilizados de Java.
seo-title: Alerta de prioridad de espacio de pila
solution: Experience Manager
title: Alerta de prioridad de espacio de pila
topic: Scene7 Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Alerta de prioridad de espacio de pila{#heap-space-priority-alert}

Se envía una alerta de prioridad cuando el espacio libre en el montón de Java está por debajo del umbral especificado inmediatamente después de un ciclo de recolección de elementos no utilizados de Java.

Las alertas repetidas deben solucionarse aumentando el espacio de la pila Java. Las incidencias posteriores de esta condición no dan como resultado una alerta por correo electrónico hasta que el período de retraso especificado con `AS::monitorAlertGenerator.heapSpaceResetInterval` ha caducado.
