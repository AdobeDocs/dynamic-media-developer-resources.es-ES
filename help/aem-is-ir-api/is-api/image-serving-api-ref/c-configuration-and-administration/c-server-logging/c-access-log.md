---
description: Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a Platform Server. Image Rendering, si está habilitado, escribe sus datos de registro de acceso en el mismo archivo.
solution: Experience Manager
title: Registro de acceso
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Registro de acceso{#access-log}

Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a Platform Server. Image Rendering, si está habilitado, escribe sus datos de registro de acceso en el mismo archivo.

El registro de acceso está configurado en server.xml.

>[!NOTE]
>
>Además del tráfico del cliente para Image Serving ( [!DNL /is/image/*]) y Image Rendering ( [!DNL /ir/render/*]), el registro de acceso puede incluir cierto tráfico interno: acceso al sistema de catálogo de Platform Server ( [!DNL /is-catalog/*]), uso compartido de la caché y solicitudes de redireccionamiento de errores ( [!DNL /is/cache/*]), acceso a otros paquetes implementados en Platform Server, como los visores de Dynamic Media ( [!DNL /is-viewers/*]), tráfico estático y solicitudes de contenido estático atendidas por Platform Server (por ejemplo, [!DNL /is-docs/*]).

Las solicitudes con [!DNL /is-catalog] y [!DNL /is/cache] rutas raíz siempre deben excluirse de cualquier análisis de tráfico del cliente.
