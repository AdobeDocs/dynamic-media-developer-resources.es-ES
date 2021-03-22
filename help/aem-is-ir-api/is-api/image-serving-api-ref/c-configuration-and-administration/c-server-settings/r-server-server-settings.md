---
description: Utilice esta configuración del servidor para configurar el servidor.
seo-description: Utilice esta configuración del servidor para configurar el servidor.
seo-title: Servidores
solution: Experience Manager
title: Servidores
uuid: 50db98cc-8354-4884-9416-00808828061b
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---


# Servidores{#server}

Utilice esta configuración del servidor para configurar el servidor.

## SV::ImageServerMode - Modo de servidor de imágenes {#section-991b287f2dde4f77a24fc69d5b32cabd}

Tanto una versión de 32 y 64 bits del Image Server están disponibles para Linux. Especifique ImageServer64 cuando se instala en servidores Linux de 64 bits o ImageServer32 (predeterminado) cuando se instala en servidores de 32 bits.

>[!NOTE]
>
>La versión de 64 bits del servidor de imágenes no admite archivos de origen FlashPix.

>[!NOTE]
>
>El modo de 64 bits no es compatible con Windows. Solo se puede especificar `ImageServer32`. De lo contrario, el servicio de imágenes no se iniciará.

## SV::PsHeapSize - Tamaño de pila del servidor de plataforma {#section-fd83715948764aeda58d6b3a9f9f8be9}

El tamaño de pila de Java para Platform Server. El valor predeterminado es &quot; `512m`&quot; (512 Mbytes).

## IS::TcpPort, PS::isConnection.port - Puerto de escucha del servidor de imágenes {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Especifica el puerto utilizado para la comunicación entre Platform Server y Image Server. Asegúrese de especificar un número de puerto que no se utilice de otro modo en el sistema host.

>[!NOTE]
>
>Para que el servicio de imágenes funcione correctamente, se debe configurar el mismo valor para `IS::TcpPort` y `PS::isConnection.port`.

## IS::PhysicalMemory - Límite de memoria del servidor de imágenes {#section-85e37aa2ac6e456eb698da716dd3247d}

Límite aproximado para los datos de imagen en memoria, expresado como un porcentaje de memoria física. El rango válido es de 10% a 90%. El servidor de imágenes intenta restringir su uso de memoria de imagen a la cantidad especificada si es posible. El límite puede superarse temporalmente durante una actividad de procesamiento intensiva.

## IS::WorkerThreads - Número de subprocesos de trabajo del servidor de imágenes {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Número máximo de subprocesos que utiliza el servidor de imágenes para procesar los datos de imágenes. El valor predeterminado es 0, lo que permite al servidor de imágenes optimizar el recuento de subprocesos automáticamente.

Algunos sistemas operativos tienen modelos de subprocesos con una sobrecarga de conmutación de contexto alta. En tal caso, el rendimiento general del servidor puede mejorar cuando se selecciona un recuento de subprocesos específico (por ejemplo, un subproceso por CPU). Es posible que se necesite cierta experimentación para encontrar la configuración óptima. Consulte las notas de la versión de Image Serving y la documentación del sistema operativo para obtener información adicional.

## IS::NumberOfTextServers - Número de instancias de servidor de texto {#section-971e20a90c1a473598fba738ed95671a}

El número máximo de procesadores de texto que deben estar activos simultáneamente. 0 (predeterminado) equivale a 1,5 veces el número de núcleos de CPU disponibles.

## IS::TextServerTcpPortRange - Puertos de comunicación del servidor de texto {#section-a13465de88ed4df09931e5ba840c1942}

Los puertos que se utilizarán para las comunicaciones con el servidor de texto. Especifique el primer y el último número de puerto, separados por &#39;-&#39;.
