---
description: Utilice esta configuración del servidor para configurar los umbrales de alerta.
seo-description: Utilice esta configuración del servidor para configurar los umbrales de alerta.
seo-title: Umbrales de alerta
solution: Experience Manager
title: Umbrales de alerta
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---


# Umbrales de alerta{#alert-thresholds}

Utilice esta configuración del servidor para configurar los umbrales de alerta.

## AS: monitorAlertGenerator.maxAverageResponseTime -Umbral de tiempo de respuestaAS: monitorAlertGenerator.maxAverageResponseTime -Tiempo de respuesta {#section-35111039ac6c4a63ba23fc2c828ab726}

Se emite una alerta de tiempo de respuesta cuando el tiempo promedio para procesar una solicitud durante el intervalo de muestreo supera el umbral establecido aquí. Expresado en msec; entero 0 o mayor. Los valores típicos están entre 100 y 1000 ms, dependiendo de la complejidad de las operaciones.

>[!NOTE]
>
>Las solicitudes que dan como resultado un estado de respuesta 4xx o 5xx no se consideran para esta alerta.

## AS::monitorAlertGenerator.maxErrorRate - Error Response Rate ThresholdAS::monitorAlertGenerator.maxErrorRate - Error Response Rate {#section-76ba77fd3102419395e0f86719a1f3ec}

Se genera una alerta de error cuando la proporción de respuestas de error HTTP con respecto a las respuestas totales durante el intervalo de muestreo supera el umbral especificado.

Valor real entre 0,0 y 1,0. Normalmente se establece entre 0,005 y 0,1. Se establece en 1 para deshabilitar las alertas de error.

## AS::monitorAlertGenerator.minRequestRate - Umbral de tráfico bajo {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Se envía una alerta de tráfico mínima cuando el número promedio de solicitudes por segundo recibidas durante el intervalo de muestreo actual se encuentra por debajo de este umbral. Deshabilite la alerta estableciendo este valor en 0. Se expresa en solicitudes por segundo. Valor real 0 o mayor.

## AS::monitorAlertGenerator.minFreeHeapSpace -Umbral de espacio libre en pilas {#section-ce6705045f6842769030ccb1894594cc}

Especifica el espacio mínimo libre en la pila de Java. Se envía una alerta de prioridad inmediatamente después de un ciclo de recopilación de residuos de Java cuando el espacio libre en pilas está por debajo de este umbral. Se recomiendan 50 MB para el funcionamiento seguro de Platform Server. Mantener el espacio libre en montículos por encima de este valor reduce la frecuencia de los ciclos de recolección de residuos, lo que puede mejorar el rendimiento general del servidor. Valor entero en bytes, 0 o más.

## AS::monitorAlertGenerator.maxOverap: Número máximo de solicitudes concurrentes {#section-ddc6925bff944758ab19bcc9cf3f2589}

Se activa una alerta de superposición cuando el número promedio de solicitudes procesadas simultáneamente durante el intervalo de promedio supera este umbral. Una superposición alta puede indicar una posible condición de sobrecarga del servidor.

Valor entero 1 o mayor. El rango típico es de 20 a 50, según la tasa de visitas de la caché y la complejidad de la solicitud.

## AS::monitorAlertGenerator.lockedThreshold - Umbral de solicitud bloqueado {#section-012a1c9937d445708380339279c62d80}

Especifica el número de segundos que una solicitud debe estar pendiente antes de que se considere bloqueada o colgada. Se emite una alerta de solicitud bloqueada si al final de un intervalo de promedio al menos una solicitud ha estado pendiente durante más tiempo que el período de tiempo especificado. Valor entero positivo en msec.

Para tener en cuenta las solicitudes de procesamiento complejas y las solicitudes que implican la obtención de datos de servidores HTTP externos, se recomienda establecer este valor en al menos 30 segundos (a menos que esta alerta detecte tal condición).
