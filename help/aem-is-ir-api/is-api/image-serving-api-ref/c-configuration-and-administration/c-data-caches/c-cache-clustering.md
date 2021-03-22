---
description: La agrupación en clúster de caché permite que varios servidores con equilibrio de carga intercambien entradas de caché en la caché de respuesta principal y la caché de datos secundaria (para solicitudes anidadas/incrustadas), con el potencial de aumentar significativamente la capacidad de respuesta del servidor eliminando la necesidad de generar la misma entrada de caché en varios servidores.
seo-description: La agrupación en clúster de caché permite que varios servidores con equilibrio de carga intercambien entradas de caché en la caché de respuesta principal y la caché de datos secundaria (para solicitudes anidadas/incrustadas), con el potencial de aumentar significativamente la capacidad de respuesta del servidor eliminando la necesidad de generar la misma entrada de caché en varios servidores.
seo-title: Clustering de caché
solution: Experience Manager
title: Clustering de caché
uuid: 347165d6-a9e7-406e-81a8-8a91f745ce27
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---


# Clustering de caché{#cache-clustering}

La agrupación en clúster de caché permite que varios servidores con equilibrio de carga intercambien entradas de caché en la caché de respuesta principal y la caché de datos secundaria (para solicitudes anidadas/incrustadas), con el potencial de aumentar significativamente la capacidad de respuesta del servidor eliminando la necesidad de generar la misma entrada de caché en varios servidores.

Si está configurado, cuando un servidor recibe una solicitud de un elemento que no está en la caché local, se pone en contacto con los servidores del mismo nivel del clúster. Comprueba si ya tienen ese elemento de datos antes de solicitar al servidor de imágenes que lo genere.

La agrupación en caché beneficia principalmente a las aplicaciones que implican contenido altamente almacenable en caché. Las cargas del servidor deben reducirse de forma significativa durante la implementación inicial y al utilizar contenido nuevo.

Los tiempos de espera y otras salvaguardias garantizan que el sistema siga funcionando a plena capacidad incluso cuando uno o más servidores del mismo nivel estén sin conexión.

El clúster de caché puede funcionar en una de las dos configuraciones básicas:

* Cuando `PS::cacheCluster.updateLocalCache` está habilitado (predeterminado), cualquier entrada de caché encontrada en un servidor del mismo nivel se copia en la caché local.

   Esta configuración reduce el tráfico entre los servidores del mismo nivel. También proporciona los tiempos de respuesta más rápidos al coste de tener todas las entradas de caché replicadas en todos los servidores del clúster. Esta es la configuración recomendada.

* Cuando `PS::cacheCluster.updateLocalCache` está deshabilitado, los datos de otros servidores no se copian en la caché local.

   Esto multiplica el espacio disponible en disco para los datos de caché. Sin embargo, aumenta el tráfico entre los servidores del mismo nivel y reduce los tiempos de respuesta generales. Utilice esta configuración solo cuando vea tasas de visitas de caché bajas.

