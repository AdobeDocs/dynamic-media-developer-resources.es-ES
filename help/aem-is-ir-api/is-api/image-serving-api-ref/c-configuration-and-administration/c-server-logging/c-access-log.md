---
description: Este es el registro principal que rastrea todas las solicitudes HTTP realizadas al servidor de plataforma. El procesamiento de imágenes, si está activado, escribe sus datos de registro de acceso en el mismo archivo.
seo-description: Este es el registro principal que rastrea todas las solicitudes HTTP realizadas al servidor de plataforma. El procesamiento de imágenes, si está activado, escribe sus datos de registro de acceso en el mismo archivo.
seo-title: Registro de acceso
solution: Experience Manager
title: Registro de acceso
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Registro de acceso{#access-log}

Este es el registro principal que rastrea todas las solicitudes HTTP realizadas al servidor de plataforma. El procesamiento de imágenes, si está activado, escribe sus datos de registro de acceso en el mismo archivo.

El registro de acceso está configurado en server.xml.

>[!NOTE]
>
>Además del tráfico del cliente para el servicio de imágenes ( [!DNL /is/image/*]) y el procesamiento de imágenes ( [!DNL /ir/render/*]), el registro de acceso puede incluir cierto tráfico interno: acceso al sistema de catálogo de Platform Server ( [!DNL /is-catalog/*]), uso compartido de la caché y solicitudes de redireccionamiento de errores ( [!DNL /is/cache/*]), acceso a otros paquetes implementados en Platform Server, como los visores de Scene7 ( [!DNL /is-viewers/*]), tráfico estático y solicitudes de contenido estático atendidas por Platform Server (por ejemplo: [!DNL /is-docs/*]).

Las solicitudes con [!DNL /is-catalog] y [!DNL /is/cache] rutas raíz siempre deben excluirse de cualquier análisis de tráfico de cliente.
