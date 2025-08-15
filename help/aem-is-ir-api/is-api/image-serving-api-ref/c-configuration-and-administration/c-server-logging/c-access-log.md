---
description: Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a  [!DNL Platform Server]. El procesamiento de imágenes, si está activado, escribe sus datos de registro de acceso en el mismo archivo.
solution: Experience Manager
title: Registro de acceso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Registro de acceso{#access-log}

Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a [!DNL Platform Server]. El procesamiento de imágenes, si está activado, escribe sus datos de registro de acceso en el mismo archivo.

El registro de acceso está configurado en server.xml.

>[!NOTE]
>
>Además del tráfico de cliente para el servicio de imágenes ([!DNL /is/image/*]) y el procesamiento de imágenes ([!DNL /ir/render/*]), el registro de acceso puede incluir cierto tráfico interno: acceso al sistema de catálogos [!DNL Platform Server] ([!DNL /is-catalog/*]), solicitudes de redirección de error y uso compartido de caché ([!DNL /is/cache/*]), acceso a otros paquetes implementados en [!DNL Platform Server], como los visores de Dynamic Media ([!DNL /is-viewers/*]), tráfico estático y solicitudes de contenido estático atendidas por [!DNL Platform Server] (por ejemplo, [!DNL /is-docs/*]).

Las solicitudes con [!DNL /is-catalog] y [!DNL /is/cache] rutas de acceso raíz siempre deben excluirse de cualquier análisis de tráfico de cliente.
