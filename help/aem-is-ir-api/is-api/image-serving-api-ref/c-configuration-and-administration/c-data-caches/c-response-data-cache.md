---
description: Platform Server almacena en caché toda la imagen de respuesta y ciertos datos de texto en el disco a menos que una solicitud esté marcada como no almacenable en caché.
solution: Experience Manager
title: Caché de datos de respuesta
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Caché de datos de respuesta{#response-data-cache}

Platform Server almacena en caché toda la imagen de respuesta y ciertos datos de texto en el disco a menos que una solicitud esté marcada como no almacenable en caché.

La ubicación de la caché de disco de Platform Server se configura con `PS::cache.rootPaths`.

Para las aplicaciones que tienen altas tasas de visitas en la caché, puede aumentar el rendimiento y la capacidad del servidor mediante la distribución de la caché de datos de respuesta entre varios dispositivos de disco. Para ello, debe crear una carpeta raíz de caché en cada disco y registrarla en `PS::cache.rootPaths`.

`PS::cache.maxSize` especifica el tamaño total de todas las entradas de caché, sin tener en cuenta la sobrecarga del sistema de archivos. La cantidad de espacio en disco que realmente se necesita depende de las propiedades del sistema de archivos (como el tamaño del bloque de disco) y el número de entradas de caché. Se recomienda reservar el doble de espacio en disco para la caché de disco HTTP que la cantidad especificada por `PS::cache.maxSize`. Se utiliza un algoritmo utilizado menos recientemente para mantener la cantidad de datos en caché dentro del límite.

Además de `PS::cache.maxSize`, la caché de respuesta también se administra limitando el número máximo de entradas de caché con `PS::cache.maxEntries`. En Linux, esta configuración debe especificar un valor no mayor que el número de nodos disponibles en la partición de caché.

>[!NOTE]
>
>Platform Server mantiene un índice de caché en memoria. El tamaño de este índice es 32 bytes veces el valor de `PS::cache.maxEntries`. Es posible que tenga que aumentar el tamaño de pila de Platform Server para admitir cachés más grandes.

El sistema utiliza un archivo de índice de caché que se guarda en disco cuando el servidor se apaga de forma ordenada. En caso de eventos inesperados como un error de alimentación, es posible que este archivo no se guarde. Además, puede tardar varios minutos en que Platform Server esté listo.
