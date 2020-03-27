---
description: Utilice esta configuración del servidor para configurar el servidor.
seo-description: Utilice esta configuración del servidor para configurar el servidor.
seo-title: Servidores
solution: Experience Manager
title: Servidores
topic: Scene7 Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Servidores{#server}

Utilice esta configuración del servidor para configurar el servidor.

## SV::ImageServerMode - Modo de servidor de imágenes {#section-991b287f2dde4f77a24fc69d5b32cabd}

Tanto una versión de 32 bits como una versión de 64 bits del servidor de imágenes están disponibles para Linux. Especifique ImageServer64 cuando se instale en servidores Linux de 64 bits o ImageServer32 (predeterminado) cuando se instale en servidores de 32 bits.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>La versión de 64 bits del servidor de imágenes no admite archivos de origen FlashPix.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Windows no admite el modo de 64 bits. Solo `ImageServer32` se puede especificar. De lo contrario, el servicio de imágenes no se inicio.

## SV::PsHeapSize - Tamaño del montón del servidor de plataforma {#section-fd83715948764aeda58d6b3a9f9f8be9}

El tamaño del montón de Java para el servidor de plataforma. El valor predeterminado es &quot; `512m`&quot; (512 Mbytes).

## IS::TcpPort, PS::isConnection.port - Puerto de escucha del servidor de imágenes {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Especifica el puerto utilizado para la comunicación entre el servidor de plataformas y el servidor de imágenes. Asegúrese de especificar un número de puerto que no se utilice de otro modo en el sistema host.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Para que el servicio de imágenes funcione correctamente, se debe establecer el mismo valor para `IS::TcpPort` y `PS::isConnection.port`.

## IS::PhysicalMemory - Límite de memoria del servidor de imágenes {#section-85e37aa2ac6e456eb698da716dd3247d}

Límite aproximado para los datos de imagen en memoria, expresado como porcentaje de memoria física. El intervalo válido es del 10 % al 90 %. El servidor de imágenes intenta restringir el uso de la memoria de imagen a la cantidad especificada si es posible. El límite puede superarse temporalmente durante la actividad de procesamiento pesado.

## IS::WorkerThwords - Número de subprocesos de trabajo de Image Server {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Número máximo de subprocesos que utiliza el servidor de imágenes para procesar datos de imagen. El valor predeterminado es 0, lo que permite al servidor de imágenes optimizar automáticamente el recuento de subprocesos.

Algunos sistemas operativos tienen modelos de subprocesos con una sobrecarga de conmutación de contexto alta. En este caso, el rendimiento general del servidor puede mejorar cuando se selecciona un recuento de subprocesos específico (por ejemplo, un subproceso por CPU). Es posible que se requiera cierta experimentación para encontrar la configuración óptima. Consulte las notas de la versión del servicio de imágenes y la documentación del sistema operativo para obtener información adicional.

## IS::NumberOfTextServers - Número de instancias del servidor de texto {#section-971e20a90c1a473598fba738ed95671a}

El número máximo de procesadores de texto que se activan al mismo tiempo. 0 (predeterminado) equivale a 1,5 veces el número de núcleos de CPU disponibles.

## IS::TextServerTcpPortRange - Puertos de comunicación del servidor de texto {#section-a13465de88ed4df09931e5ba840c1942}

Puertos que se utilizarán para las comunicaciones con servidores de texto. Especifique el primer y el último número de puerto, separados por &#39;-&#39;.
