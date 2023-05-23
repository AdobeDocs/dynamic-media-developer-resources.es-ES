---
description: Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a [!DNL Platform Server]. El procesamiento de imágenes, si está activado, escribe sus datos de registro de acceso en el mismo archivo.
solution: Experience Manager
title: Registro de acceso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Registro de acceso{#access-log}

Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a [!DNL Platform Server]. El procesamiento de imágenes, si está activado, escribe sus datos de registro de acceso en el mismo archivo.

El registro de acceso está configurado en server.xml.

>[!NOTE]
>
>Además del tráfico de cliente para el servicio de imágenes ( [!DNL /is/image/*]) y procesamiento de imágenes ( [!DNL /ir/render/*]), el registro de acceso puede incluir cierto tráfico interno: acceso a [!DNL Platform Server] sistema de catálogo ( [!DNL /is-catalog/*]), uso compartido de caché y solicitudes de redirección de errores ( [!DNL /is/cache/*]), acceso a otros paquetes implementados en [!DNL Platform Server], como los visores de Dynamic Media ( [!DNL /is-viewers/*]), tráfico estático y solicitudes de contenido estático atendidas por [!DNL Platform Server] (p. ej., [!DNL /is-docs/*]).

Solicitudes con [!DNL /is-catalog] y [!DNL /is/cache] las rutas raíz siempre deben excluirse de cualquier análisis de tráfico de cliente.
