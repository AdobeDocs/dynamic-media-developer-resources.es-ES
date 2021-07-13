---
description: Los componentes del servicio de imágenes son administrados por el Supervisor del servidor, que es un daemon de Linux o un servicio de Windows (S7Supervisor.exe, listado como 'Servicio de imágenes de Dynamic Media' en el Panel de control de Campaign de servicios).
solution: Experience Manager
title: Supervisor del servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Supervisor del servidor{#server-supervisor}

Los componentes del servicio de imágenes son administrados por el Supervisor del servidor, que es un daemon de Linux o un servicio de Windows (S7Supervisor.exe, listado como &#39;Servicio de imágenes de Dynamic Media&#39; en el Panel de control de Campaign de servicios).

Además de iniciar y detener otros componentes de servicio de imágenes, el Supervisor del servidor es responsable de garantizar el estado de estos otros componentes. Si un componente se bloquea, se reinicia automáticamente para minimizar las interrupciones del servicio.

## Inicio y parada {#section-061d28d74e034a30adc39ea3e2031cd0}

El Supervisor del servidor se inicia, se detiene y se reinicia con el script de utilidad del servicio de imágenes. Consulte la [Documentación de utilidades](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) para obtener más información.

Al iniciar y detener el Supervisor del servidor, se inicia y detiene automáticamente todos los demás componentes de Image Serving.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
