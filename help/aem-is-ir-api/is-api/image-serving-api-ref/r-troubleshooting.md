---
description: Esta sección contiene soluciones a problemas que han ocurrido ocasionalmente con el servicio de imágenes.
seo-description: Esta sección contiene soluciones a problemas que han ocurrido ocasionalmente con el servicio de imágenes.
seo-title: Resolución de problemas
solution: Experience Manager
title: Resolución de problemas
uuid: 39fdaf86-004b-4553-bde0-0367f3ef76b8
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 1%

---


# Resolución de problemas{#troubleshooting}

Esta sección contiene soluciones a problemas que han ocurrido ocasionalmente con el servicio de imágenes.

**General**

ImageServer ahora mantiene un registro de instalación y una carpeta de copia de seguridad de todos los archivos modificados durante una instalación de actualización. Este archivo y carpeta se encuentran en la raíz del directorio de instalación de Image Serving.

**Al iniciar el servidor de imágenes, el script de inicio se detiene con el mensaje &quot;inicio pendiente&quot; (solo LINUX)**

Esto puede indicar un problema con la licencia de servicio de imágenes, como la falta de un archivo de licencia o una licencia temporal caducada. Un archivo de licencia válido debe estar ubicado en [!DNL /usr/local/scene7/licenses].

**El servidor de imágenes se bloquea o se bloquea y el archivo de registro del servidor de imágenes indica que no hay espacio suficiente o que el recurso no está disponible temporalmente en el archivo  [!DNL IgcVirtualMemory.cpp]**

El motivo de este mensaje de error es que Image Server no ha podido asignar la cantidad de memoria que se configuró para usar.

* Compruebe la configuración Memoria física en [!DNL ImageServerRegistry.xml]. No debería ser más del 50%, menos si otras aplicaciones que requieren mucha memoria se están ejecutando en el mismo sistema. El valor predeterminado es 20%.
* Asegúrese de que el espacio de intercambio en el servidor sea al menos el doble del tamaño de la RAM física. La baja configuración del espacio de intercambio puede causar este problema.

**El espacio en disco real utilizado por la carpeta de caché excede el  ` *[!DNL cache.maxSize]*`establecido en[!DNL PlatformServer.conf]**

Esto no indica un problema. La sobrecarga del sistema de archivos no se incluye en la configuración de caché de disco de Platform Server. El importe total comunicado por el sistema puede ser sustancialmente superior al valor establecido. Se recomienda reservar el doble de espacio en disco que se especifica en ` *[!DNL cache.maxSize]*`.

**Imágenes rotas en los ejemplos de is-docs**

Esto ocurre si Image Server no se está ejecutando. También ocurre si la ruta raíz del catálogo o la ruta raíz de la imagen se han cambiado de la predeterminada de instalación, pero las imágenes y catálogos de ejemplo no se han movido a las nuevas ubicaciones. Compruebe el valor Ruta raíz del servidor de imágenes en los archivos de configuración. Si es necesario, mueva la carpeta de demostración que contiene las imágenes de ejemplo a la raíz de la imagen actual y mueva [!DNL sample*.*] a la raíz del catálogo actual.

En los ejemplos también se presupone que ciertas configuraciones de [!DNL default.ini] son estándar (por ejemplo, la ofuscación o el bloqueo no deben estar activados).

**Faltan demasiados errores de caché tras un tiempo de actividad sustancial**

En función del uso del servidor, el rendimiento puede mejorarse aumentando el tamaño de la caché de disco de Platform Server si hay espacio disponible en disco. La configuración se puede cambiar editando manualmente los archivos de configuración. Consulte la documentación.

**Los archivos de registro ocupan demasiado espacio en disco**

Image Server y Platform Server inician un nuevo archivo de registro todos los días. De forma predeterminada, se colocan en [!DNL *[!DNL install_root]*/ImageServing/logs]. El tamaño del archivo de registro, el número de registros guardados y el contenido de registro se pueden configurar. Consulte la documentación.

**Si tiene software antivirus instalado en su servidor**

Se recomienda desactivar el análisis de directorios de servicio de imágenes. De lo contrario, el escaneo de directorios de lectura y escritura de gran volumen (como caché, imágenes, fuentes, perfiles y directorios de catálogo) causará problemas.

**Digimarc causa problemas de rendimiento para imágenes de zoom**

No utilice Digimarc en las imágenes que se van a ampliar. El rendimiento no será aceptable. Si es necesario, cree un catálogo independiente para las imágenes que se van a usar para ampliar y deshabilitar Digimarc para este catálogo.
