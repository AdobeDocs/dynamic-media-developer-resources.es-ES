---
description: La agrupación en clústeres de caché permite que varios servidores con equilibrio de carga intercambien entradas de caché en la caché de respuesta principal y en la caché de datos secundaria (para solicitudes anidadas/incrustadas), con el potencial de aumentar significativamente la capacidad de respuesta del servidor al eliminar la necesidad de generar la misma entrada de caché en varios servidores.
solution: Experience Manager
title: Clúster de caché
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
TQID: 'https://experienceleague.adobe.com/J1QtNEy9i67oveb1oS2V6-fagqrrlC30oih8AS1g-N4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 0%

---

# Clúster de caché{#cache-clustering}

La agrupación en clústeres de caché permite que varios servidores con equilibrio de carga intercambien entradas de caché en la caché de respuesta principal y en la caché de datos secundaria (para solicitudes anidadas/incrustadas), con el potencial de aumentar significativamente la capacidad de respuesta del servidor al eliminar la necesidad de generar la misma entrada de caché en varios servidores.

Si se configura así, cuando un servidor recibe una solicitud de un elemento que no está en la caché local, se pone en contacto con los servidores del mismo nivel del clúster. Comprueba si ya tienen ese elemento de datos antes de solicitar al servidor de imágenes que genere el elemento.

La agrupación en clúster de caché beneficia principalmente a las aplicaciones que incluyen contenido altamente almacenable en caché. Las cargas del servidor deben reducirse significativamente durante la implementación inicial y al publicar nuevo contenido.

Los tiempos de espera y otras medidas de seguridad garantizan que el sistema siga funcionando a plena capacidad incluso cuando uno o más de los servidores del mismo nivel están sin conexión.

El clúster de caché puede funcionar en una de las dos configuraciones básicas:

* Cuando `PS::cacheCluster.updateLocalCache` está habilitado (predeterminado), cualquier entrada de caché encontrada en un servidor del mismo nivel se copia en la caché local.

  Esta configuración reduce el tráfico entre los servidores del mismo nivel. También proporciona los tiempos de respuesta más rápidos a costa de replicar todas las entradas de caché en todos los servidores del clúster. Esta es la configuración recomendada.

* Cuando `PS::cacheCluster.updateLocalCache` está deshabilitado, los datos de otros servidores no se copian en la caché local.

  Esto multiplica el espacio disponible en disco para los datos de la caché. Sin embargo, aumenta el tráfico entre los servidores del mismo nivel y reduce los tiempos de respuesta generales. Utilice esta configuración solo cuando vea tasas bajas de visitas a la caché.
