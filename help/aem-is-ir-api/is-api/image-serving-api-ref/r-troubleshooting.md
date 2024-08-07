---
description: Esta sección contiene soluciones a problemas que se han producido ocasionalmente con el servicio de imágenes.
solution: Experience Manager
title: Resolución de problemas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Resolución de problemas{#troubleshooting}

Esta sección contiene soluciones a problemas que se han producido ocasionalmente con el servicio de imágenes.

**General**

ImageServer ahora mantiene un registro de instalación y una carpeta de copia de seguridad de todos los archivos cambiados durante una instalación de actualización. Este archivo y esta carpeta se encuentran en la raíz del directorio de instalación del servicio de imágenes.

**Al iniciar el servidor de imágenes, el script de inicio se detiene con el mensaje &quot;inicio pendiente&quot; (solo LINUX)**

Esto puede indicar un problema con la licencia de servicio de imágenes, como la falta de un archivo de licencia o una licencia temporal caducada. Se debe encontrar un archivo de licencia válido en [!DNL /usr/local/scene7/licenses].

**El servidor de imágenes se detiene o se bloquea y el archivo de registro del servidor de imágenes indica que no hay suficiente espacio o que el &quot;recurso no está disponible temporalmente en el archivo [!DNL IgcVirtualMemory.cpp]&quot;**

El motivo de este mensaje de error es que el servidor de imágenes no ha podido asignar la cantidad de memoria que se configuró para utilizar.

* Compruebe la configuración de la memoria física en [!DNL ImageServerRegistry.xml]. No debería ser superior al 50%, menos si otras aplicaciones de memoria intensiva se ejecutan en el mismo sistema. El valor predeterminado es 20%.
* Asegúrese de que el espacio de intercambio en el servidor sea al menos el doble del tamaño de la RAM física. La configuración de espacio de intercambio baja puede causar este problema.

**El espacio en disco real utilizado por la carpeta de caché supera ` *[!DNL cache.maxSize]*`el establecido en[!DNL PlatformServer.conf]**

Esto no indica ningún problema. La sobrecarga del sistema de archivos no se incluye en la configuración de caché de disco de [!DNL Platform Server]. El importe total comunicado por el sistema puede ser sustancialmente superior a la configuración. Se recomienda reservar el doble de espacio en disco que se especifica en ` *[!DNL cache.maxSize]*`.

**Imágenes rotas en los ejemplos de is-docs**

Esto ocurre si Image Server no se está ejecutando. También se produce si la ruta raíz del catálogo o la ruta raíz de la imagen han cambiado desde la instalación predeterminada, pero las imágenes y los catálogos de ejemplo no se han movido a las nuevas ubicaciones. Compruebe el valor de Ruta de acceso raíz del servidor de imágenes en los archivos de configuración. Si es necesario, mueva la carpeta de demostración que contiene las imágenes de ejemplo a la raíz de la imagen actual y mueva [!DNL sample*.*] a la raíz del catálogo actual.

En los ejemplos también se supone que ciertas opciones de configuración de [!DNL default.ini] son estándar (por ejemplo, no se debe habilitar la ofuscación o el bloqueo).

**Demasiados errores de caché después de un tiempo de actividad considerable**

Según el uso del servidor, el rendimiento puede mejorarse si se aumenta el tamaño de la caché de disco [!DNL Platform Server] si hay espacio disponible en el disco. La configuración se puede cambiar editando manualmente los archivos de configuración. Consulte la documentación.

**Los archivos de registro ocupan demasiado espacio en disco**

El servidor de imágenes y [!DNL Platform Server] inician un nuevo archivo de registro todos los días. De forma predeterminada, se colocan en [!DNL *[!DNL install_root]*/ImageServing/logs]. Tamaño del archivo de registro, número de registros guardados y contenido de registro que se puede configurar. Consulte la documentación.

**Si tiene instalado software antivirus en el servidor**

Se recomienda desactivar el análisis de directorios del servicio de imágenes. De lo contrario, el análisis de directorios de lectura/escritura de gran volumen (como caché, imágenes, fuentes, perfiles y directorios de catálogo) puede causar problemas.

**Digimarc causa problemas de rendimiento para las imágenes de zoom**

No utilice Digimarc en imágenes con zoom ampliado. El rendimiento no es aceptable. Si es necesario, cree un catálogo independiente para las imágenes que se utilizarán para ampliar o reducir y deshabilite Digimarc para este catálogo.
