---
description: Utilice esta configuración del servidor para configurar el sistema de supervisión y alerta.
solution: Experience Manager
title: Monitorización y sistema de alertas
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Monitorización y alerta del sistema{#monitoring-and-alerting-system}

Utilice esta configuración del servidor para configurar el sistema de supervisión y alerta.

## AS::monitorAlertGenerator.enableGlobalAlerting - Sistema de alertas habilitado {#section-612f8ea61794426ab205e22e5f665fa9}

Habilite la notificación por correo electrónico estableciendo en &quot;true&quot; y configurando la configuración de notificación por correo electrónico. Si se establece en `false`, se desactivan todas las alertas de correo electrónico. Esto puede resultar útil cuando se extrae un servidor de la línea para mantenimiento. Booleano.

## AS::mailSender.host - Host SMTP {#section-151df07e7b44446581339bb7abeeba7a}

La dirección IP del servidor de correo electrónico SMTP.

## AS::mailSender.port- Puerto SMTP {#section-4b25efca8fd84d5c92dafacd0555e99d}

Puerto de escucha para el servidor de correo electrónico SMTP.

## AS::monitorAlertGenerator.messageTo - Destinatario de mensajes {#section-0017bbaa15434117a70900c3f1163960}

Una o más direcciones de correo electrónico a las que se deben enviar alertas. Utilice punto y coma como separadores.

## AS::monitorAlertGenerator.messageFrom - Remitente de mensajes {#section-db320cba4ac2438ca1cfe6abce4aed87}

La dirección de correo electrónico que debe utilizarse en el campo de correo electrónico **[!UICONTROL From]**.

## AS::monitorAlertGenerator.alertInterval - Intervalo de monitorización {#section-99cb2e3380c1499e9d5aec3671ed73c7}

El sistema de monitorización acumulará las condiciones de alerta durante el intervalo de alerta y enviará un correo electrónico de alerta con todas las alertas acumuladas al final de cada intervalo. Milisegundos, valor entero, 60000 o más. Generalmente se establece en 5 o 10 minutos.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Intervalo de alerta de espacio en montículo {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Tiempo mínimo después de emitir una alerta de espacio en pilas antes de otra. Tiempo de intervalo en ms. Valor entero, 0 o mayor.

## AS::monitorAlertGenerator.minTrafficForAlerts - Tráfico mínimo para habilitar alertas {#section-8b4db2d6f96642309ca35c49eb3ab230}

Solicitudes por segundo. No se emitirán alertas de error ni tiempo de respuesta si el tráfico se encuentra por debajo de este umbral. Establézcalo en 0 para enviar alertas de error y tiempo de respuesta independientemente del volumen de tráfico. Valor real 0 o mayor.
