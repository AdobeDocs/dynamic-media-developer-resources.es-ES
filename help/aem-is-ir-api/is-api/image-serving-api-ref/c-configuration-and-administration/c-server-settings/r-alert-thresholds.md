---
description: Utilice esta configuración del servidor para configurar los umbrales de alerta.
seo-description: Utilice esta configuración del servidor para configurar los umbrales de alerta.
seo-title: Umbrales de alerta
solution: Experience Manager
title: Umbrales de alerta
topic: Scene7 Image Serving - Image Rendering API
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# Alert thresholds{#alert-thresholds}

Utilice esta configuración del servidor para configurar los umbrales de alerta.

## AS: monitorAlertGenerator.maxAverageResponseTime -Umbral de tiempo de respuestaAS: monitorAlertGenerator.maxAverageResponseTime -Tiempo de respuesta {#section-35111039ac6c4a63ba23fc2c828ab726}

Se emite una alerta de tiempo de respuesta cuando el tiempo promedio para procesar una solicitud durante el intervalo de muestreo supera el umbral establecido aquí. Expresado en ms; entero 0 o mayor. Los valores típicos están entre 100 y 1000 ms, según la complejidad de las operaciones.

>[!NOTE]
>
>Las solicitudes que dan como resultado un estado de respuesta 4xx o 5xx no se tienen en cuenta para esta alerta.

## AS::monitorAlertGenerator.maxErrorRate - Umbral de tasa de respuesta de errorAS::monitorAlertGenerator.maxErrorRate - Tasa de respuesta de error {#section-76ba77fd3102419395e0f86719a1f3ec}

Se emite una alerta de error cuando la proporción de respuestas de error HTTP con respecto a las respuestas totales durante el intervalo de muestreo supera el umbral especificado.

Valor real entre 0,0 y 1,0. Normalmente se establece entre 0,005 y 0,1. Establezca en 1 para deshabilitar las alertas de error.

## AS::monitorAlertGenerator.minRequestRate - Umbral de poco tráfico {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Se envía una alerta de tráfico mínima cuando el número medio de solicitudes por segundo recibidas durante el intervalo de muestreo actual se sitúa por debajo de este umbral. Deshabilite la alerta estableciendo este valor en 0. Se expresa en solicitudes por segundo. Valor real 0 o superior.

## AS::monitorAlertGenerator.minFreeHeapSpace -Umbral de espacio de montón libre {#section-ce6705045f6842769030ccb1894594cc}

Especifica el espacio mínimo libre en la pila de Java. Una alerta de prioridad se envía inmediatamente después de un ciclo de recolección de elementos no utilizados de Java cuando el espacio libre del montón está por debajo de este umbral. Se recomiendan 50 MB para el funcionamiento seguro del servidor Platform. Mantener el espacio libre en el montón por encima de este valor reduce la frecuencia de los ciclos de recolección de elementos no utilizados, lo que puede mejorar el rendimiento general del servidor. Valor entero en bytes, 0 o más.

## AS::monitorAlertGenerator.maxOverlap - Número máximo de solicitudes simultáneas {#section-ddc6925bff944758ab19bcc9cf3f2589}

Se activa una alerta de superposición cuando el número medio de solicitudes procesadas simultáneamente durante el intervalo de promedios supera este umbral. Una superposición alta puede indicar una posible condición de sobrecarga del servidor.

Valor entero 1 o superior. El intervalo típico es de 20 a 50, según la velocidad de visitas de la caché y la complejidad de la solicitud.

## AS::monitorAlertGenerator.lockedThreshold - Umbral de solicitud bloqueada {#section-012a1c9937d445708380339279c62d80}

Especifica el número de segundos que una solicitud debe estar pendiente antes de que se considere bloqueada o bloqueada. Se emite una alerta de solicitud bloqueada si al final de un intervalo de promedio al menos una solicitud ha estado pendiente durante más tiempo que el período de tiempo especificado. Valor entero positivo en mseg.

Para dar cuenta de solicitudes de procesamiento complejas y solicitudes que implican la obtención de datos de servidores HTTP extranjeros, se recomienda establecer este valor en al menos 30 segundos (a menos que esta alerta detecte una condición de este tipo).
