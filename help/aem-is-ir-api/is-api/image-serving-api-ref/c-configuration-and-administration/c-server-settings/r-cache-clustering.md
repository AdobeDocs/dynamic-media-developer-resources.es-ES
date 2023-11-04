---
description: Utilice esta configuración de servidor para la agrupación en clúster de caché.
solution: Experience Manager
title: Clúster de caché
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Clúster de caché{#cache-clustering}

Utilice esta configuración de servidor para la agrupación en clúster de caché.

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Lista de direcciones IP, separadas por punto y coma. Incluya las direcciones IP de todos los servidores del mismo nivel desde los que este host debe obtener datos de caché. La dirección IP del host local se puede incluir para mayor comodidad; esto permite los mismos ajustes de configuración para todos los servidores del clúster.

## PS::cacheCluster.updateLocalCache: actualizar caché local {#section-154c2c0af4544200a3499232bb130dde}

Se establece en &#39;Yes&#39; si una entrada de caché proporcionada por un servidor del mismo nivel se debe copiar en la caché de respuestas local.

## PS::cacheCluster.queryTimeout: tiempo de espera de consulta {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Al solicitar una entrada de caché de servidores del mismo nivel, el servidor espera hasta que un servidor responda que tiene este elemento de datos concreto, hasta que todos los servidores del mismo nivel hayan respondido que no tienen el elemento de datos o hasta que la hora especificada con esta configuración (en ms) haya caducado.

## PS::cacheCluster.fetchTimeout: tiempo de espera de recuperación {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Especifica el número máximo de ms que el servidor espera a que los datos de caché reales se envíen desde el servidor del mismo nivel. Si no se han entregado todos los datos antes de que expire el tiempo de espera, el servidor asume que el interlocutor no está disponible. A continuación, la entrada de caché se genera localmente.
