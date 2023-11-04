---
description: Utilice esta configuración del servidor para configurar el sistema de supervisión y alertas.
solution: Experience Manager
title: Sistema de monitorización y alertas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Sistema de monitorización y alertas{#monitoring-and-alerting-system}

Utilice esta configuración del servidor para configurar el sistema de supervisión y alertas.

## AS::monitorAlertGenerator.enableGlobalAlerting: activación del sistema de alertas {#section-612f8ea61794426ab205e22e5f665fa9}

Habilite las notificaciones por correo electrónico estableciendo como &quot;true&quot; y configurando las opciones de notificaciones por correo electrónico. Estableciendo en `false` desactiva todas las alertas de correo electrónico: esto puede resultar útil cuando se desconecta un servidor para fines de mantenimiento. Booleano.

## AS::mailSender.host: host SMTP {#section-151df07e7b44446581339bb7abeeba7a}

La dirección IP del servidor de correo electrónico SMTP.

## AS::mailSender.port- Puerto SMTP {#section-4b25efca8fd84d5c92dafacd0555e99d}

El puerto de escucha para el servidor de correo electrónico SMTP.

## AS::monitorAlertGenerator.messageTo: Destinatario de mensajes {#section-0017bbaa15434117a70900c3f1163960}

Una o más direcciones de correo electrónico a las que se deben enviar alertas. Utilice punto y coma como separadores.

## AS::monitorAlertGenerator.messageFrom: remitente de mensajes {#section-db320cba4ac2438ca1cfe6abce4aed87}

La dirección de correo electrónico que debe usarse en la **[!UICONTROL Desde]** campo de correo electrónico.

## AS::monitorAlertGenerator.alertInterval: intervalo de monitorización {#section-99cb2e3380c1499e9d5aec3671ed73c7}

El sistema de monitorización acumula condiciones de alerta durante el intervalo de alerta y envía un correo electrónico de alerta que contiene todas las alertas acumuladas al final de cada intervalo. Milisegundos, valor entero, 60000 o mayor. Normalmente se establece en 5 o 10 minutos.

## AS::monitorAlertGenerator.heapSpaceResetInterval: Intervalo de alerta de espacio de pila {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Tiempo mínimo después de una alerta de espacio de pila antes de que se emita otra. Tiempo de intervalo en ms Valor entero, 0 o superior.

## AS::monitorAlertGenerator.minTrafficForAlerts: Tráfico mínimo para activar las alertas {#section-8b4db2d6f96642309ca35c49eb3ab230}

Solicitudes por segundo. No se emiten alertas de tiempo de respuesta y error si el tráfico cae por debajo de este umbral. Establezca el valor en 0 para enviar alertas de tiempo de respuesta y error independientemente del volumen de tráfico. Valor real 0 o superior.
