---
description: Se envía una alerta de prioridad cuando el espacio libre en la pila de Java está por debajo del umbral especificado inmediatamente después de un ciclo de colección de residuos de Java.
solution: Experience Manager
title: Alerta de prioridad del espacio de montículos
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Alerta de prioridad del espacio de montículos{#heap-space-priority-alert}

Se envía una alerta de prioridad cuando el espacio libre en la pila de Java está por debajo del umbral especificado inmediatamente después de un ciclo de colección de residuos de Java.

Las alertas repetidas deben solucionarse aumentando el espacio de memoria de Java. Las incidencias posteriores de esta condición no dan como resultado una alerta por correo electrónico hasta que el periodo de retraso especificado con `AS::monitorAlertGenerator.heapSpaceResetInterval` haya caducado.
