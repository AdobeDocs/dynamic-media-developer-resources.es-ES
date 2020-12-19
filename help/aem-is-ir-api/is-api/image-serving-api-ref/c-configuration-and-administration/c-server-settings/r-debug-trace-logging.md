---
description: Utilice esta configuración del servidor para depurar el registro de seguimiento.
seo-description: Utilice esta configuración del servidor para depurar el registro de seguimiento.
seo-title: Registro de Debug_trace
solution: Experience Manager
title: Registro de Debug_trace
topic: Scene7 Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Registro de Debug_trace{#debug-trace-logging}

Utilice esta configuración del servidor para depurar el registro de seguimiento.

>[!NOTE]
>
>Se recomienda configurar todos los archivos de registro para que se escriban en la misma carpeta que `TC::directory`. Esto garantiza que todos los archivos de registro del servicio de imágenes participen en la rotación automática del archivo de registro configurada con `TC::maxDays`, lo que evitará la posible inestabilidad del servidor debido a condiciones de espacio fuera del disco.

## SV::log - Ruta del archivo de registro de seguimiento del supervisor del servidor {#section-3697bc480ff646e79cacc2812c55ef26}

Carpeta y nombre de archivo base para los archivos de registro del Supervisor del servidor. La ruta puede ser absoluta o relativa a *[!DNL install_folder]*. El Supervisor del servidor anexará un guión y la fecha actual ( *[!DNL -yyyy-mm-dd]*) al nombre del archivo (antes del sufijo del archivo, si existe). Se recomienda enviar todos los archivos de registro a la misma carpeta que los archivos de registro de Platform Server ( `PS::LogFolder`) para aprovechar la administración de archivos de registro implementada por Platform Server ( `PS::LogDays`). El valor predeterminado es [!DNL logs/Supervisor.log].

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que los permisos de acceso están establecidos para que el Supervisor del servidor tenga los privilegios de creación, lectura y escritura necesarios.

## SV::tracelel - Nivel de registro de seguimiento del supervisor del servidor {#section-36f8634741da4c618d67aa628b5fe474}

El nivel de registro puede ser 1, 2, 3 o 4. El valor predeterminado es 2.

## IS::Log - Ruta del archivo de registro de depuración del servidor de imágenes {#section-73a3f09b77f2446c9f82207b7d8aec39}

Carpeta y nombre de archivo base para los archivos de registro de seguimiento de Image Server. La ruta puede ser absoluta o relativa a *[!DNL install_folder]*. ImageServer anexará un guión y la fecha actual ( *[!DNL -yyyy-mm-dd]*) al nombre del archivo (antes del sufijo del archivo, si existe). Se recomienda enviar archivos de registro de Image Server a la misma carpeta que los archivos de registro de Platform Server ( `PS::LogFolder`) para aprovechar la administración de archivos de registro implementada por Platform Server (consulte `PS::LogDays`).

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que los permisos de acceso están establecidos para que el servicio de imágenes tenga los privilegios de creación, lectura y escritura necesarios.

## IS:TraceClient - Nivel de registro de depuración del servidor de imágenes {#section-3851f1f68e404430985c629ac80534db}

El nivel de registro puede ser 1, 2, 3 o 4 (el valor predeterminado es 2)

El nivel 1 registra eventos relacionados con las conexiones de inicio, apagado y servidor de plataforma.

El nivel 2 también registra la conexión y desconexión de las imágenes de origen.

El nivel 3 agrega el registro de solicitudes de datos de píxeles y el envío de la misma a Platform Server.

El nivel 4 registra todos los mensajes recibidos del servidor de plataformas.

Los niveles 3 y 4 deben utilizarse únicamente con fines de depuración, ya que los archivos de registro pueden llegar a ser muy grandes.

## IS::TraceStatsInterval - Intervalo de registro de estadísticas del servidor de imágenes {#section-1d8df96d61044e33a5b2b2b0309c2d59}

El servidor de imágenes escribe estadísticas de memoria en su archivo de registro de seguimiento en el intervalo especificado por esta configuración. El intervalo válido es de 5 a 86.400 segundos.
