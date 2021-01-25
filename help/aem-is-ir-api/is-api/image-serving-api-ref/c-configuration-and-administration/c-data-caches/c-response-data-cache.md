---
description: Platform Server almacena en caché en disco toda la imagen de respuesta y ciertos datos de texto, a menos que una solicitud se marque como no se puede almacenar en caché.
seo-description: Platform Server almacena en caché en disco toda la imagen de respuesta y ciertos datos de texto, a menos que una solicitud se marque como no se puede almacenar en caché.
seo-title: Caché de datos de respuesta
solution: Experience Manager
title: Caché de datos de respuesta
topic: Dynamic Media Image Serving - Image Rendering API
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Caché de datos de respuesta{#response-data-cache}

Platform Server almacena en caché en disco toda la imagen de respuesta y ciertos datos de texto, a menos que una solicitud se marque como no se puede almacenar en caché.

La ubicación de la caché de disco de Platform Server se establece con `PS::cache.rootPaths`.

Para las aplicaciones con altas tasas de visitas de caché, puede aumentar el rendimiento y la capacidad del servidor distribuyendo la caché de datos de respuesta entre varios dispositivos de disco. Para ello, debe crear una carpeta raíz de caché en cada disco y registrarla en `PS::cache.rootPaths`.

`PS::cache.maxSize` especifica el tamaño total de todas las entradas de caché, sin tener en cuenta la sobrecarga del sistema de archivos. La cantidad de espacio en disco que realmente se necesita depende de las propiedades del sistema de archivos (como el tamaño del bloque de disco) y el número de entradas de caché. Se recomienda reservar el doble de espacio en disco para la caché de disco HTTP que la cantidad especificada por `PS::cache.maxSize`. Se utiliza un algoritmo utilizado menos recientemente para mantener la cantidad de datos en caché dentro del límite.

Además de `PS::cache.maxSize`, la caché de respuesta también se administra limitando el número máximo de entradas de caché con `PS::cache.maxEntries`. En Linux, esta configuración debe especificar un valor no mayor que el número de nodos disponibles en la partición de caché.

>[!NOTE]
>
>Platform Server mantiene un índice de caché en memoria. El tamaño de este índice es 32 bytes por encima del valor de `PS::cache.maxEntries`. Es posible que tenga que aumentar el tamaño del montón del Servidor de plataformas para acomodar las cachés más grandes.

El sistema utiliza un archivo de índice de caché que se guarda en disco cuando el servidor se apaga de forma ordenada. En caso de eventos inesperados, como una falla de alimentación, es posible que este archivo no se guarde. Además, puede que el Servidor de plataformas tarde varios minutos en estar listo.
