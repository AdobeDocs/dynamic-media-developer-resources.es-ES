---
description: Utilice esta configuración del servidor para configurar el servidor.
solution: Experience Manager
title: Servidores
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---

# Servidores{#server}

Utilice esta configuración del servidor para configurar el servidor.

## SV::ImageServerMode: modo de servidor de imágenes {#section-991b287f2dde4f77a24fc69d5b32cabd}

Linux dispone de una versión de 32 y 64 bits del servidor de imágenes. Especifique ImageServer64 cuando esté instalado en servidores Linux de 64 bits, o ImageServer32 (predeterminado) cuando esté instalado en servidores de 32 bits.

>[!NOTE]
>
>La versión de 64 bits del servidor de imágenes no admite archivos de origen FlashPix.

>[!NOTE]
>
>Windows no admite el modo de 64 bits. Solo se puede especificar `ImageServer32`. De lo contrario, el servicio de imágenes no se inicia.

## SV::PsHeapSize - [!DNL Platform Server] tamaño de pila {#section-fd83715948764aeda58d6b3a9f9f8be9}

Tamaño de la pila Java para [!DNL Platform Server]. El valor predeterminado es &quot; `512m`&quot; (512 Mbytes).

## IS::TcpPort, PS::isConnection.port: Puerto de escucha del servidor de imágenes {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Especifica el puerto utilizado para la comunicación entre [!DNL Platform Server] y el servidor de imágenes. Asegúrese de especificar un número de puerto que no se utilice en caso contrario en el sistema host.

>[!NOTE]
>
>Para que el servicio de imágenes funcione correctamente, se debe establecer el mismo valor para `IS::TcpPort` y `PS::isConnection.port`.

## IS::PhysicalMemory: límite de memoria del servidor de imágenes {#section-85e37aa2ac6e456eb698da716dd3247d}

Límite aproximado de datos de imagen en memoria, expresado como porcentaje de memoria física. El intervalo válido es del 10 % al 90 %. El servidor de imágenes intenta restringir el uso de la memoria de imágenes a la cantidad especificada, si es posible. El límite puede superarse temporalmente durante una intensa actividad de procesamiento.

## IS::WorkerThreads: número de Image Server Worker Threads {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Número máximo de subprocesos que utiliza el servidor de imágenes para procesar los datos de imagen. El valor predeterminado es 0, lo que permite al servidor de imágenes optimizar el recuento de subprocesos automáticamente.

Algunos sistemas operativos tienen modelos de subprocesos con una alta sobrecarga de conmutación de contexto. En tales circunstancias, el rendimiento general del servidor puede mejorar cuando se selecciona un recuento de hilos específico (por ejemplo, un hilo por CPU). Es posible que se requiera cierta experimentación para encontrar el escenario óptimo. Consulte las notas de la versión del servicio de imágenes y la documentación del sistema operativo para obtener más información.

## IS::NumberOfTextServers: número de instancias de servidor de texto {#section-971e20a90c1a473598fba738ed95671a}

Número máximo de procesadores de texto que se activarán simultáneamente. 0 (predeterminado) equivale a 1,5 veces el número de núcleos de CPU disponibles.

## IS::TextServerTcpPortRange: puertos de comunicación del servidor de texto {#section-a13465de88ed4df09931e5ba840c1942}

Los puertos que se utilizarán para las comunicaciones del servidor de texto. Especifique el primer y el último número de puerto, separados con &#39;-&#39;.
