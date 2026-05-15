---
description: Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a  [!DNL Platform Server]. El procesamiento de imágenes, si está activado, escribe sus datos de registro de acceso en el mismo archivo.
solution: Experience Manager
title: Registro de acceso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
TQID: 'https://experienceleague.adobe.com/PXdlJ0gBGbq4FFhoG6gtmG3hrWVWsXIPelL9xXy5ESk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 0%

---

# Registro de acceso{#access-log}

Este es el registro principal que realiza un seguimiento de todas las solicitudes HTTP realizadas a [!DNL Platform Server]. El procesamiento de imágenes, si está activado, escribe sus datos de registro de acceso en el mismo archivo.

El registro de acceso está configurado en server.xml.

>[!NOTE]
>
>Además del tráfico de cliente para el servicio de imágenes ([!DNL /is/image/*]) y el procesamiento de imágenes ([!DNL /ir/render/*]), el registro de acceso puede incluir cierto tráfico interno: acceso al sistema de catálogos [!DNL Platform Server] ([!DNL /is-catalog/*]), solicitudes de redirección de error y uso compartido de caché ([!DNL /is/cache/*]), acceso a otros paquetes implementados en [!DNL Platform Server], como los visores de Dynamic Media ([!DNL /is-viewers/*]), tráfico estático y solicitudes de contenido estático atendidas por [!DNL Platform Server] (por ejemplo, [!DNL /is-docs/*]).

Las solicitudes con [!DNL /is-catalog] y [!DNL /is/cache] rutas de acceso raíz siempre deben excluirse de cualquier análisis de tráfico de cliente.
