---
title: Requisitos y requisitos previos del sistema
description: Antes de usar el servicio de imágenes de Dynamic Media, asegúrese de que el sistema cumpla los requisitos del sistema.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
TQID: 'https://experienceleague.adobe.com/SKAe9OsVsSkTRR5E3s5lBcPct4CgG1h1uIh7ayIpINA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 390
ht-degree: 0%

---

# Requisitos y requisitos previos del sistema{#system-requirements-and-prerequisites}

Antes de usar el servicio de imágenes de Dynamic Media, asegúrese de que el sistema cumpla los requisitos del sistema.

## Hardware del servidor {#section-f3c14a7bc1b745118602659628df779f}

El servidor debe cumplir los siguientes requisitos de hardware.

>[!NOTE]
>
>Los sistemas con procesadores con AMD64 e Intel® EM64T suelen configurarse como plataformas NUMA (arquitectura de memoria no uniforme). Esto significa que el núcleo construye varios nodos de memoria en el momento del arranque en lugar de construir un solo nodo de memoria. La construcción de varios nodos puede causar agotamiento de la memoria en uno o más de los nodos antes de que otros nodos se agoten. Cuando se agota la memoria, el núcleo puede decidir matar procesos (por ejemplo, el servidor de imágenes o [!DNL Platform Server]) aunque haya memoria disponible. Por lo tanto, Adobe recomienda que si está ejecutando un sistema de este tipo, desactive NUMA. Utilice la opción de inicio `numa=off` para evitar que el núcleo detenga estos procesos.

**Windows**

* Intel Xeon® o AMD® Opteron CPU con al menos cuatro núcleos.
* 1 GB de RAM como mínimo.
* El espacio de intercambio es igual al menos al doble de la cantidad de memoria física (RAM).
* 2 GB de espacio disponible en el disco duro para la instalación y el funcionamiento básico; se requiere espacio adicional en el disco para las imágenes de origen, los registros, las cachés de datos y los archivos de manifiesto.
* Tarjeta de interfaz de red Fast Ethernet.

**Linux®**

* Intel Xeon® o AMD® Opteron CPU con al menos cuatro núcleos.
* 16 GB de RAM como mínimo.
* Intercambio desactivado (recomendado).
* 2 GB de espacio disponible en el disco duro para la instalación y el funcionamiento básico; se requiere espacio adicional en el disco para las imágenes de origen, los registros, las cachés de datos y los archivos de manifiesto.
* Tarjeta de interfaz de red Fast Ethernet.

**Nota (Linux®):** El servicio de imágenes no funciona con SELinux activado. Esta opción está habilitada de forma predeterminada. Para deshabilitar SELinux, edite el archivo [!DNL /etc/selinux/config] y cambie el valor de SELinux de:

`SELINUX=enforcing`

A

`SELINUX=disabled`

**Nota (Linux®):** Asegúrese de que el nombre de host del servidor se puede resolver en una dirección IP. Si no es posible, agregue el nombre de host completo y la dirección IP a [!DNL /etc/hosts], como en el ejemplo siguiente.

`<ip address> <fully qualified hostname>`

## Software de servidor {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

El servicio de imágenes de Dynamic Media requiere el siguiente software de servidor.

**Windows**

* Microsoft® Windows Server 2008.
* Sistema operativo de 64 bits.

**Linux®**

* Red Hat® Enterprise 5 o CentOS 5.5 y versiones posteriores, con los parches de correcciones más recientes.
* Sistema operativo de 64 bits.

**Nota:** Para usar el servicio de imágenes en Windows, debe instalar Microsoft® Visual Studio 2010.
