---
description: Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a Platform Server. Image Rendering, si está habilitado, escribe sus datos de registro de acceso en el mismo archivo.
seo-description: Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a Platform Server. Image Rendering, si está habilitado, escribe sus datos de registro de acceso en el mismo archivo.
seo-title: Registro de acceso
solution: Experience Manager
title: Registro de acceso
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# Registro de acceso{#access-log}

Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a Platform Server. Image Rendering, si está habilitado, escribe sus datos de registro de acceso en el mismo archivo.

El registro de acceso está configurado en server.xml.

>[!NOTE]
>
>Además del tráfico del cliente para Image Serving ( [!DNL /is/image/*]) y Image Rendering ( [!DNL /ir/render/*]), el registro de acceso puede incluir cierto tráfico interno: acceso al sistema de catálogo de Platform Server ( [!DNL /is-catalog/*]), uso compartido de la caché y solicitudes de redireccionamiento de errores ( [!DNL /is/cache/*]), acceso a otros paquetes implementados en Platform Server, como los visores de Dynamic Media ( [!DNL /is-viewers/*]), tráfico estático y solicitudes de contenido estático atendidas por Platform Server (por ejemplo, [!DNL /is-docs/*]).

Las solicitudes con [!DNL /is-catalog] y [!DNL /is/cache] rutas raíz siempre deben excluirse de cualquier análisis de tráfico del cliente.
