---
description: Se envía una alerta de prioridad cuando el espacio libre en la pila de Java está por debajo del umbral especificado inmediatamente después de un ciclo de recolección de elementos no utilizados de Java.
solution: Experience Manager
title: Alerta de prioridad de espacio de pila
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# Alerta de prioridad de espacio de pila{#heap-space-priority-alert}

Se envía una alerta de prioridad cuando el espacio libre en la pila de Java está por debajo del umbral especificado inmediatamente después de un ciclo de recolección de elementos no utilizados de Java.

Las alertas repetidas deben solucionarse aumentando el espacio de la pila de Java. Las ocurrencias posteriores de esta condición no dan como resultado una alerta por correo electrónico hasta que el período de retraso especificado con `AS::monitorAlertGenerator.heapSpaceResetInterval` haya caducado.
