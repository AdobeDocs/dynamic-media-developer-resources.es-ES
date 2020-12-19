---
description: Antes de utilizar el servicio de imágenes de Scene7, asegúrese de que el sistema cumple los requisitos del sistema.
seo-description: Antes de utilizar el servicio de imágenes de Scene7, asegúrese de que el sistema cumple los requisitos del sistema.
seo-title: Requisitos y requisitos previos del sistema
solution: Experience Manager
title: Requisitos y requisitos previos del sistema
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---


# Requisitos y requisitos previos del sistema{#system-requirements-and-prerequisites}

Antes de utilizar el servicio de imágenes de Scene7, asegúrese de que el sistema cumple los requisitos del sistema.

## Hardware de servidor {#section-f3c14a7bc1b745118602659628df779f}

El servidor debe cumplir los siguientes requisitos de hardware.

>[!NOTE]
>
>Los sistemas con procesadores con AMD64 e Intel® EM64T suelen configurarse como plataformas NUMA (Arquitectura de memoria no uniforme). Esto significa que el núcleo construye varios nodos de memoria en tiempo de arranque en lugar de construir un solo nodo de memoria. La construcción de varios nodos puede resultar en agotamiento de la memoria en uno o más nodos antes de agotarse otros nodos. Cuando ocurre el agotamiento de la memoria, el núcleo puede decidir eliminar procesos (por ejemplo, el Servidor de imágenes o el Servidor de plataformas) aunque haya memoria disponible. Por lo tanto, Adobe Systems recomienda que si está ejecutando un sistema de este tipo desactive NUMA. Utilice la opción de inicio `numa=off` para evitar que el núcleo detenga estos procesos.

**Windows**

* CPU Intel Xeon® o AMD® Opteron con al menos 4 núcleos.
* 16 GB de RAM como mínimo.
* Intercambiar espacio igual al menos al doble de la cantidad de memoria física (RAM).
* 2 GB de espacio disponible en el disco duro para la instalación y el funcionamiento básico; se necesita espacio adicional en disco para las imágenes de origen, los registros, las memorias caché de datos y los archivos de manifiesto.
* Tarjeta de interfaz de red Fast Ethernet.

**Linux**

* CPU Intel Xeon® o AMD® Opteron con al menos 4 núcleos.
* 16 GB de RAM como mínimo.
* Intercambio deshabilitado (recomendado).
* 2 GB de espacio disponible en el disco duro para la instalación y el funcionamiento básico; se necesita espacio adicional en disco para las imágenes de origen, los registros, las memorias caché de datos y los archivos de manifiesto.
* Tarjeta de interfaz de red Fast Ethernet.

**Nota (Linux):El servicio** de imágenes no funciona con SELinux activado. Esta opción está activada de forma predeterminada. Para deshabilitar SELinux, edite el archivo [!DNL /etc/selinux/config] y cambie el valor de SELinux de:

`SELINUX=enforcing`

a

`SELINUX=disabled`

**Nota (Linux):** Asegúrese de que el nombre de host del servidor se puede resolver en una dirección IP. Si esto no es posible, agregue el nombre de host completo y la dirección IP a [!DNL /etc/hosts] como en el siguiente ejemplo.

`<ip address> <fully qualified hostname>`

## Software de servidor {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

El servicio de imágenes de Scene7 requiere el siguiente software de servidor.

**Windows**

* Microsoft® Windows 2008 Server.
* Sistema operativo de 64 bits.

**Linux**

* Red Hat® Enterprise 5 o CentOS 5.5 y posterior, con los parches de corrección más recientes.
* Sistema operativo de 64 bits.

**Nota:** Para usar el servicio de imágenes en Windows, debe instalar el redistribuible de Microsoft Visual Studio 2010. El redistribuible está disponible en la siguiente ubicación:

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

