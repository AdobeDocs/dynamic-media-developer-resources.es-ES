---
description: Utilice esta configuración del servidor para depurar el registro de seguimiento.
seo-description: Utilice esta configuración del servidor para depurar el registro de seguimiento.
seo-title: Registro de Debug_trace
solution: Experience Manager
title: Registro de Debug_trace
uuid: 33f1d093-007d-453b-965a-9d701a845954
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---


# Registro de Debug_trace{#debug-trace-logging}

Utilice esta configuración del servidor para depurar el registro de seguimiento.

>[!NOTE]
>
>Se recomienda configurar todos los archivos de registro para que se escriban en la misma carpeta que `TC::directory`. Esto garantiza que todos los archivos de registro de Image Serving participen en la rotación automática de archivos de registro configurada con `TC::maxDays`, lo que evitará la inestabilidad potencial del servidor debido a condiciones de espacio fuera de disco.

## SV::log - Ruta del archivo de registro de seguimiento del supervisor del servidor {#section-3697bc480ff646e79cacc2812c55ef26}

Nombre de carpeta y archivo base para los archivos de registro del Supervisor del servidor. La ruta puede ser absoluta o relativa a *[!DNL install_folder]*. El Supervisor del servidor adjuntará un guión y la fecha actual ( *[!DNL -yyyy-mm-dd]*) al nombre del archivo (antes del sufijo del archivo, si lo hubiera). Se recomienda enviar todos los archivos de registro a la misma carpeta que los archivos de registro de Platform Server ( `PS::LogFolder`) para aprovechar la administración de archivos de registro implementada por Platform Server ( `PS::LogDays`). El valor predeterminado es [!DNL logs/Supervisor.log].

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que los permisos de acceso estén configurados para que el Supervisor del servidor tenga los privilegios de creación, lectura y escritura necesarios.

## SV::tracelevel - Nivel de registro de seguimiento del supervisor del servidor {#section-36f8634741da4c618d67aa628b5fe474}

El nivel de registro puede ser 1, 2, 3 o 4. El valor predeterminado es 2.

## IS::Log - Ruta del archivo de registro de depuración del servidor de imágenes {#section-73a3f09b77f2446c9f82207b7d8aec39}

Carpeta y nombre de archivo base para los archivos de registro de seguimiento del servidor de imágenes. La ruta puede ser absoluta o relativa a *[!DNL install_folder]*. ImageServer adjuntará un guión y la fecha actual ( *[!DNL -yyyy-mm-dd]*) al nombre del archivo (antes del sufijo del archivo, si lo hubiera). Se recomienda enviar los archivos de registro del servidor de imágenes a la misma carpeta que los archivos de registro del servidor de plataforma ( `PS::LogFolder`) para aprovechar la administración de archivos de registro implementada por el servidor de plataforma (consulte `PS::LogDays`).

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que los permisos de acceso estén establecidos para que Image Serving tenga los privilegios de creación, lectura y escritura necesarios.

## IS:TraceClient - Nivel de registro de depuración del servidor de imágenes {#section-3851f1f68e404430985c629ac80534db}

El nivel de registro puede ser 1, 2, 3 o 4 (el valor predeterminado es 2)

El nivel 1 registra eventos relacionados con conexiones de inicio, cierre y servidor de plataforma.

El nivel 2 también registra los registros que se conectan a las imágenes de origen y que se desconectan de ellas.

El Nivel 3 añade el registro de solicitudes de datos de píxeles y el envío de los mismos al Servidor de Platform.

Level 4 registra todos los mensajes recibidos del Servidor de plataforma.

Los niveles 3 y 4 solo deben utilizarse con fines de depuración, ya que los archivos de registro pueden llegar a ser muy grandes.

## IS::TraceStatsInterval - Intervalo de registro de estadísticas del servidor de imágenes {#section-1d8df96d61044e33a5b2b2b0309c2d59}

El servidor de imágenes escribe estadísticas de memoria en su archivo de registro de seguimiento en el intervalo especificado por esta configuración. El intervalo válido es de 5 a 86 400 segundos.
