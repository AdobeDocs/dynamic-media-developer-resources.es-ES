---
title: Caché de datos de respuesta
description: El [!DNL Platform Server] almacena en caché todas las imágenes de respuesta y ciertos datos de texto en el disco a menos que una solicitud se marque como no almacenable en caché.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Caché de datos de respuesta{#response-data-cache}

El [!DNL Platform Server] almacena en caché todas las imágenes de respuesta y ciertos datos de texto en el disco a menos que una solicitud se marque como no almacenable en caché.

La ubicación del [!DNL Platform Server]La caché de disco de está configurada con `PS::cache.rootPaths`.

En el caso de las aplicaciones que tienen tasas altas de aciertos de caché, puede aumentar el rendimiento y la capacidad del servidor mediante la distribución de la caché de datos de respuesta entre varios dispositivos de disco. Para ello, cree una carpeta raíz de caché en cada disco y regístrela en `PS::cache.rootPaths`.

El `PS::cache.maxSize` especifica el tamaño total de todas las entradas de caché, sin tener en cuenta la sobrecarga del sistema de archivos. La cantidad de espacio en disco necesaria depende de las propiedades del sistema de archivos (como el tamaño del bloque de disco) y del número de entradas de caché. Reserve el doble de espacio en disco para la caché de disco HTTP que la cantidad especificada por `PS::cache.maxSize`. Se utiliza un algoritmo utilizado menos recientemente para mantener la cantidad de datos en caché dentro del límite.

Además de `PS::cache.maxSize`, la caché de respuestas también se administra limitando el número máximo de entradas de caché con `PS::cache.maxEntries`. En Linux®, esta configuración debe especificar un valor no mayor que el número de nodos disponibles en la partición de caché.

>[!NOTE]
>
>El [!DNL Platform Server] mantiene un índice de caché en memoria. El tamaño de este índice es 32 bytes veces el valor de `PS::cache.maxEntries`. Aumente el [!DNL Platform Server] tamaño de pila para admitir cachés más grandes, si es necesario.

El sistema utiliza un archivo de índice de caché que se guarda en el disco cuando el servidor se apaga de forma ordenada. Si hay eventos inesperados, como un corte de energía, es posible que este archivo no se guarde. Además, el proceso puede tardar varios minutos en [!DNL Platform Server] para estar listo.
