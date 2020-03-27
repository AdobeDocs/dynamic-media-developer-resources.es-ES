---
description: Utilice esta configuración de servidor para la agrupación en clúster de caché.
seo-description: Utilice esta configuración de servidor para la agrupación en clúster de caché.
seo-title: Agrupamiento de caché
solution: Experience Manager
title: Agrupamiento de caché
topic: Scene7 Image Serving - Image Rendering API
uuid: ed6335d7-26c9-45d8-95f6-6c05e788e449
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Agrupamiento de caché{#cache-clustering}

Utilice esta configuración de servidor para la agrupación en clúster de caché.

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Lista de direcciones IP, separadas por punto y coma. Incluya las direcciones IP de todos los servidores del mismo nivel desde los que este host debe obtener datos de caché. La dirección IP del host local puede incluirse por conveniencia; esto permite la misma configuración para todos los servidores del clúster.

## PS::cacheCluster.updateLocalCache: actualizar caché local {#section-154c2c0af4544200a3499232bb130dde}

Se establece en &#39;Sí&#39; si una entrada de caché proporcionada por un servidor del mismo nivel debe copiarse en la caché de respuesta local.

## PS::cacheCluster.queryTimeout: tiempo de espera de Consulta {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Al solicitar una entrada de caché desde servidores del mismo nivel, el servidor esperará hasta que un servidor responda que tiene este elemento de datos en particular, o hasta que todos los servidores del mismo nivel hayan respondido que no tienen el elemento de datos o hasta que haya caducado el tiempo especificado con este ajuste (en msec).

## PS::cacheCluster.fetchTimeout - Tiempo de espera de recuperación {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Especifica el número máximo de ms que el servidor esperará para que los datos reales de la caché se entreguen desde el servidor del mismo nivel. Si los datos completos no se han entregado antes de que caduque el tiempo de espera, el servidor asume que el par no está disponible. La entrada de caché se genera localmente.
