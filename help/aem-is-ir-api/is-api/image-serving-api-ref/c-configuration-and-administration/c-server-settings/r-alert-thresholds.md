---
description: Utilice esta configuración del servidor para configurar los umbrales de alerta.
solution: Experience Manager
title: Umbrales de alerta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Umbrales de alerta{#alert-thresholds}

Utilice esta configuración del servidor para configurar los umbrales de alerta.

## AS: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS:: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

Se emite una alerta de tiempo de respuesta cuando el tiempo medio para procesar una solicitud durante el intervalo de muestreo supera el umbral establecido aquí. Se expresa en milisegundos; entero 0 o mayor. Los valores habituales están entre 100 y 1000 ms, según la complejidad de las operaciones.

>[!NOTE]
>
>Las solicitudes que resultan en un estado de respuesta 4xx o 5xx no se consideran para esta alerta.

## AS::monitorAlertGenerator.maxErrorRate - Error Response Rate ThresholdAS::monitorAlertGenerator.maxErrorRate - Error Response Rate {#section-76ba77fd3102419395e0f86719a1f3ec}

Se emite una alerta de error cuando la proporción de respuestas de error HTTP respecto al total de respuestas durante el intervalo de muestreo supera el umbral especificado.

Valor real entre 0,0 y 1,0. Normalmente se establece entre 0,005 y 0,1. Establezca el valor en 1 para deshabilitar las alertas de error.

## AS::monitorAlertGenerator.minRequestRate: umbral de tráfico bajo {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Se envía una alerta de tráfico mínimo cuando el número promedio de solicitudes por segundo recibidas durante el intervalo de muestreo actual cae por debajo de este umbral. Deshabilite la alerta estableciendo este valor en 0. Se expresa en solicitudes por segundo. Valor real 0 o superior.

## AS::monitorAlertGenerator.minFreeHeapSpace: umbral de espacio libre en la pila {#section-ce6705045f6842769030ccb1894594cc}

Especifica el espacio mínimo disponible en la pila de Java. Se envía una alerta de prioridad inmediatamente después de un ciclo de recolección de elementos no utilizados de Java cuando el espacio libre en la pila está por debajo de este umbral. Se recomiendan 50 MB para un funcionamiento seguro del [!DNL Platform Server]. Mantener el espacio libre en la pila por encima de este valor reduce la frecuencia de los ciclos de recolección de elementos no utilizados, lo que puede mejorar el rendimiento general del servidor. Valor entero en bytes, 0 o superior.

## AS::monitorAlertGenerator.maxOverlap: número máximo de solicitudes simultáneas {#section-ddc6925bff944758ab19bcc9cf3f2589}

Se activa una alerta de superposición cuando el número promedio de solicitudes procesadas simultáneamente durante el intervalo de promedio supera este umbral. Una superposición alta puede indicar una posible condición de sobrecarga del servidor.

Valor entero 1 o mayor. El intervalo típico es de 20 a 50, según la tasa de visitas a la caché y la complejidad de la solicitud.

## AS::monitorAlertGenerator.lockedThreshold - Umbral de solicitud bloqueado {#section-012a1c9937d445708380339279c62d80}

Especifica el número de segundos que una solicitud debe estar pendiente antes de que se considere bloqueada o bloqueada. Se emite una alerta de solicitud bloqueada si al final de un intervalo de promedio al menos una solicitud ha estado pendiente durante más tiempo que el período de tiempo especificado. Valor entero positivo en ms.

Para tener en cuenta solicitudes de procesamiento complejas y solicitudes que implican la obtención de datos de servidores HTTP externos, se recomienda establecer este valor en al menos 30 segundos (a menos que esta alerta detecte una condición de este tipo).
