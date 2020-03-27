---
description: Esta sección contiene soluciones a problemas que se han producido ocasionalmente con el servicio de imágenes.
seo-description: Esta sección contiene soluciones a problemas que se han producido ocasionalmente con el servicio de imágenes.
seo-title: Resolución de problemas
solution: Experience Manager
title: Resolución de problemas
topic: Scene7 Image Serving - Image Rendering API
uuid: 39fdaf86-004b-4553-bde0-0367f3ef76b8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Resolución de problemas{#troubleshooting}

Esta sección contiene soluciones a problemas que se han producido ocasionalmente con el servicio de imágenes.

**General**

ImageServer ahora mantiene un registro de instalación y una carpeta de copia de seguridad de todos los archivos cambiados durante una instalación de actualización. Este archivo y esta carpeta se encuentran en la raíz del directorio de instalación del servicio de imágenes.

**Al iniciar el servidor de imágenes, la secuencia de comandos de inicio se detiene con el mensaje &quot;inicio pendiente&quot; (solo LINUX)**

Esto puede indicar un problema con la licencia de servicio de imágenes, como la falta de un archivo de licencia o una licencia temporal caducada. Debe encontrarse un archivo de licencia válido en [!DNL /usr/local/scene7/licenses].

**El servidor de imágenes se detiene o bloquea y el archivo de registro del servidor de imágenes indica que no hay espacio suficiente o que el &quot;recurso no está disponible temporalmente en el archivo[!DNL IgcVirtualMemory.cpp]&quot;**

El motivo de este mensaje de error es que el servidor de imágenes no pudo asignar la cantidad de memoria que se configuró para usar.

* Compruebe la configuración de Memoria física en [!DNL ImageServerRegistry.xml]. No debería ser más del 50%, menos si otras aplicaciones con uso intensivo de memoria se ejecutan en el mismo sistema. El valor predeterminado es 20%.
* Asegúrese de que el espacio de intercambio en el servidor sea al menos el doble del tamaño de la RAM física. La configuración de espacio de intercambio bajo puede causar este problema.

**El espacio real en disco utilizado por la carpeta de caché excede el` *[!DNL cache.maxSize]*`establecido en[!DNL PlatformServer.conf]**

Esto no indica un problema. La sobrecarga del sistema de archivos no se incluye en la configuración de caché de disco del servidor de plataformas. El importe total comunicado por el sistema puede ser sustancialmente superior al valor establecido. Se recomienda reservar el doble de espacio en disco que el especificado en ` *[!DNL cache.maxSize]*`.

**Imágenes dañadas en los ejemplos de is-docs**

Esto sucede si el servidor de imágenes no se está ejecutando. También se produce si la ruta raíz del catálogo o la ruta raíz de la imagen se han cambiado de la ruta predeterminada de instalación, pero las imágenes y los catálogos de ejemplo no se han movido a las nuevas ubicaciones. Compruebe el valor de Ruta raíz del servidor de imágenes en los archivos de configuración. Si es necesario, mueva la carpeta de demostración que contiene las imágenes de ejemplo a la raíz de la imagen actual y desplácese [!DNL sample*.*] a la raíz del catálogo actual.

En los ejemplos también se da por supuesto que ciertos ajustes de [!DNL default.ini] son estándar (por ejemplo, no se debe habilitar la confusión o el bloqueo).

**Demasiados errores de caché tras un tiempo de actividad sustancial**

Según el uso del servidor, el rendimiento puede mejorarse aumentando el tamaño de la caché de disco de Platform Server si hay espacio disponible en disco. La configuración se puede cambiar editando manualmente los archivos de configuración. Consulte la documentación.

**Los archivos de registro ocupan demasiado espacio en disco**

El servidor de imágenes y el inicio del servidor de plataformas incluyen un nuevo archivo de registro todos los días. De forma predeterminada, se ubican en [!DNL *[!DNL install_root]*/ImageServing/logs]. Puede configurar el tamaño del archivo de registro, el número de registros conservados y el contenido del registro. Consulte la documentación.

**Si tiene software antivirus instalado en el servidor**

Se recomienda desactivar la exploración de directorios de servicio de imágenes. De lo contrario, la digitalización de directorios de lectura y escritura de gran volumen (como caché, imágenes, fuentes, perfiles y directorios de catálogo) causará problemas.

**Digimarc causa problemas de rendimiento en imágenes de zoom**

No utilice Digimarc en las imágenes que se van a ampliar. El rendimiento no será aceptable. Si es necesario, cree un catálogo independiente para las imágenes que se van a usar para aplicar zoom y desactive Digimarc para este catálogo.
