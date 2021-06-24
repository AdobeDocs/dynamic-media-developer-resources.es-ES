---
description: Antes de usar Dynamic Media Image Serving, asegúrese de que su sistema cumpla los requisitos del sistema.
solution: Experience Manager
title: Requisitos y requisitos previos del sistema
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Requisitos y requisitos previos del sistema{#system-requirements-and-prerequisites}

Antes de usar Dynamic Media Image Serving, asegúrese de que su sistema cumpla los requisitos del sistema.

## Hardware del servidor {#section-f3c14a7bc1b745118602659628df779f}

Su servidor debe cumplir los siguientes requisitos de hardware.

>[!NOTE]
>
>Los sistemas con procesadores AMD64 e Intel® EM64T suelen configurarse como plataformas NUMA (Arquitectura de memoria no uniforme). Esto significa que el núcleo construye varios nodos de memoria en el momento del arranque en lugar de construir un solo nodo de memoria. La construcción de varios nodos puede provocar el agotamiento de la memoria en uno o varios nodos antes de que otros se agoten. Cuando ocurre el agotamiento de la memoria, el núcleo puede decidir matar procesos (por ejemplo, Image Server o Platform Server) aunque haya memoria disponible. Por lo tanto, Adobe Systems recomienda que, si está ejecutando un sistema de este tipo, desactive NUMA. Utilice la opción `numa=off` start para evitar que el núcleo detenga estos procesos.

**Windows**

* CPU Intel Xeon® o AMD® Opteron con al menos 4 núcleos.
* 16 GB de RAM como mínimo.
* Intercambie el espacio igual al menos al doble de la memoria física (RAM).
* 2 GB de espacio disponible en disco duro para la instalación y el funcionamiento básico, se requiere espacio adicional en disco para imágenes de origen, registros, cachés de datos y archivos de manifiesto.
* Tarjeta de interfaz de red Fast Ethernet.

**Linux**

* CPU Intel Xeon® o AMD® Opteron con al menos 4 núcleos.
* 16 GB de RAM como mínimo.
* Intercambio desactivado (recomendado).
* 2 GB de espacio disponible en disco duro para la instalación y el funcionamiento básico, se requiere espacio adicional en disco para imágenes de origen, registros, cachés de datos y archivos de manifiesto.
* Tarjeta de interfaz de red Fast Ethernet.

**Nota (Linux):**  El servicio de imágenes no funciona con SELinux activado. Esta opción está activada de forma predeterminada. Para desactivar SELinux, edite el archivo [!DNL /etc/selinux/config] y cambie el valor de SELinux de:

`SELINUX=enforcing`

a

`SELINUX=disabled`

**Nota (Linux):** Asegúrese de que el nombre de host del servidor se puede resolver en una dirección IP. Si no es posible, añada el nombre de host completo y la dirección IP a [!DNL /etc/hosts] como en el siguiente ejemplo.

`<ip address> <fully qualified hostname>`

## Software de servidor {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Serving requiere el siguiente software de servidor.

**Windows**

* Microsoft® Windows 2008 Server.
* Sistema operativo de 64 bits.

**Linux**

* Red Hat® Enterprise 5 o CentOS 5.5 y posteriores, con los parches de corrección más recientes.
* Sistema operativo de 64 bits.

**Nota:** Para usar Image Serving en Windows, debe instalar Microsoft Visual Studio 2010 redistribuible. El redistribuible está disponible en la siguiente ubicación:

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)
