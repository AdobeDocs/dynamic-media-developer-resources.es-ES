---
description: Se envía una alerta de prioridad cuando el espacio libre en la pila de Java está por debajo del umbral especificado inmediatamente después de un ciclo de colección de residuos de Java.
seo-description: Se envía una alerta de prioridad cuando el espacio libre en la pila de Java está por debajo del umbral especificado inmediatamente después de un ciclo de colección de residuos de Java.
seo-title: Alerta de prioridad del espacio de montículos
solution: Experience Manager
title: Alerta de prioridad del espacio de montículos
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Alerta de prioridad del espacio de montículos{#heap-space-priority-alert}

Se envía una alerta de prioridad cuando el espacio libre en la pila de Java está por debajo del umbral especificado inmediatamente después de un ciclo de colección de residuos de Java.

Las alertas repetidas deben solucionarse aumentando el espacio de memoria de Java. Las incidencias posteriores de esta condición no dan como resultado una alerta por correo electrónico hasta que el periodo de retraso especificado con `AS::monitorAlertGenerator.heapSpaceResetInterval` haya caducado.
