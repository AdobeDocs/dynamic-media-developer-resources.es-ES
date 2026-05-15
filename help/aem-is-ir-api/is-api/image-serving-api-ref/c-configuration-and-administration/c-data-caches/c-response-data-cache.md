---
title: Caché de datos de respuesta
description: ' [!DNL Platform Server] almacena en caché todas las imágenes de respuesta y ciertos datos de texto en el disco a menos que se marque una solicitud como no almacenable en caché.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
TQID: 'https://experienceleague.adobe.com/zxZqRHFCMKKDxOBb35IEZWEhTFhknDgCKcYatA6lqGs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 282
ht-degree: 0%

---

# Caché de datos de respuesta{#response-data-cache}

El [!DNL Platform Server] almacena en caché todas las imágenes de respuesta y ciertos datos de texto en el disco a menos que se marque una solicitud como no almacenable en caché.

La ubicación de la caché de disco de [!DNL Platform Server] está establecida con `PS::cache.rootPaths`.

En el caso de las aplicaciones que tienen tasas altas de aciertos de caché, puede aumentar el rendimiento y la capacidad del servidor mediante la distribución de la caché de datos de respuesta entre varios dispositivos de disco. Para ello, cree una carpeta raíz de caché en cada disco y regístrela en `PS::cache.rootPaths`.

`PS::cache.maxSize` especifica el tamaño total de todas las entradas de caché, sin tener en cuenta la sobrecarga del sistema de archivos. La cantidad de espacio en disco necesaria depende de las propiedades del sistema de archivos (como el tamaño del bloque de disco) y del número de entradas de caché. Reserve el doble de espacio en disco para la caché de disco HTTP que la cantidad especificada por `PS::cache.maxSize`. Se utiliza un algoritmo utilizado menos recientemente para mantener la cantidad de datos en caché dentro del límite.

Además de `PS::cache.maxSize`, la caché de respuestas también se administra limitando el número máximo de entradas de caché con `PS::cache.maxEntries`. En Linux®, esta configuración debe especificar un valor no mayor que el número de nodos disponibles en la partición de caché.

>[!NOTE]
>
>[!DNL Platform Server] mantiene un índice de caché en memoria. El tamaño de este índice es de 32 bytes veces el valor de `PS::cache.maxEntries`. Aumente el tamaño de la pila [!DNL Platform Server] para acomodar cachés más grandes, si es necesario.

El sistema utiliza un archivo de índice de caché que se guarda en el disco cuando el servidor se apaga de forma ordenada. Si hay eventos inesperados, como un corte de energía, es posible que este archivo no se guarde. Además, [!DNL Platform Server] puede tardar varios minutos en estar listo.
