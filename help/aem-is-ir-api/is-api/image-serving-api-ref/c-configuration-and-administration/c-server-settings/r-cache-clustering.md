---
description: Utilice esta configuración de servidor para la agrupación en clúster de caché.
seo-description: Utilice esta configuración de servidor para la agrupación en clúster de caché.
seo-title: Clustering de caché
solution: Experience Manager
title: Clustering de caché
uuid: ed6335d7-26c9-45d8-95f6-6c05e788e449
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Clustering de caché{#cache-clustering}

Utilice esta configuración de servidor para la agrupación en clúster de caché.

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Lista de direcciones IP separadas por punto y coma. Incluya las direcciones IP de todos los servidores del mismo nivel desde los que este host debe obtener datos de caché. La dirección IP del host local se puede incluir para mayor comodidad; esto permite los mismos ajustes de configuración para todos los servidores del clúster.

## PS::cacheCluster.updateLocalCache - Actualizar caché local {#section-154c2c0af4544200a3499232bb130dde}

Se establece en &quot;Sí&quot; si una entrada de caché proporcionada por un servidor del mismo nivel se debe copiar en la caché de respuestas local.

## PS::cacheCluster.queryTimeout - Tiempo de espera de consulta {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Al solicitar una entrada de caché de los servidores del mismo nivel, el servidor esperará hasta que un servidor responda que tiene este elemento de datos en particular, o hasta que todos los servidores del mismo nivel hayan respondido que no tienen el elemento de datos o hasta que el tiempo especificado con esta configuración (en msec) haya caducado.

## PS::cacheCluster.fetchTimeout - Tiempo de espera de recuperación {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Especifica el número máximo de ms que el servidor esperará para que los datos de caché reales se entreguen desde el servidor del mismo nivel. Si los datos completos no se han entregado antes de que caduque el tiempo de espera, el servidor supone que el par ya no está disponible. A continuación, la entrada de caché se genera localmente.
