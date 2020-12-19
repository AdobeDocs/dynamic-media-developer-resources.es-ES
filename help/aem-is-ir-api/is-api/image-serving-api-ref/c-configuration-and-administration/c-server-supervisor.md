---
description: Los componentes del servicio de imágenes son administrados por el Supervisor del servidor, que es un demonio de Linux o un servicio de Windows (S7Supervisor.exe, que aparece como 'Servicio de imágenes de Scene7' en el Panel de control de Campaign de servicios).
seo-description: Los componentes del servicio de imágenes son administrados por el Supervisor del servidor, que es un demonio de Linux o un servicio de Windows (S7Supervisor.exe, que aparece como 'Servicio de imágenes de Scene7' en el Panel de control de Campaign de servicios).
seo-title: Supervisor de servidor
solution: Experience Manager
title: Supervisor de servidor
topic: Scene7 Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Supervisor del servidor{#server-supervisor}

Los componentes del servicio de imágenes son administrados por el Supervisor del servidor, que es un demonio de Linux o un servicio de Windows (S7Supervisor.exe, que aparece como &#39;Servicio de imágenes de Scene7&#39; en el Panel de control de Campaign de servicios).

Además de iniciar y detener otros componentes de servicio de imágenes, el Supervisor del servidor es responsable de garantizar el estado de estos otros componentes. Si un componente se bloquea, se reinicia automáticamente para minimizar cualquier interrupción del servicio.

## Inicio y parada {#section-061d28d74e034a30adc39ea3e2031cd0}

El Supervisor del servidor se inicia, se detiene y se reinicia con la secuencia de comandos de la utilidad de servicio de imágenes. Consulte la [documentación de utilidades](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) para obtener más información.

Al iniciar y detener el Supervisor del servidor, automáticamente se inicio y detiene todos los demás componentes del servicio de imágenes.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
