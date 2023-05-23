---
description: Utilice esta configuración del servidor para depurar el registro de seguimiento.
solution: Experience Manager
title: Registro Debug_trace
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---

# Registro Debug_trace{#debug-trace-logging}

Utilice esta configuración del servidor para depurar el registro de seguimiento.

>[!NOTE]
>
>Se recomienda configurar todos los archivos de registro para que se escriban en la misma carpeta que `TC::directory`. Esto garantiza que todos los archivos de registro del servicio de imágenes participen en la rotación automática de archivos de registro configurada con `TC::maxDays`, que evitará la posible inestabilidad del servidor debido a condiciones de falta de espacio en disco.

## SV::log: ruta del archivo de registro de seguimiento del supervisor del servidor {#section-3697bc480ff646e79cacc2812c55ef26}

Carpeta y nombre de archivo base para los archivos de registro del Supervisor del servidor. La ruta puede ser absoluta o relativa a *[!DNL install_folder]*. El Supervisor de servidor adjuntará un guión y la fecha actual ( *[!DNL -yyyy-mm-dd]*) al nombre del archivo (antes del sufijo del archivo, si lo hay). Se recomienda enviar todos los archivos de registro a la misma carpeta que [!DNL Platform Server] archivos de registro ( `PS::LogFolder`) para aprovechar la administración de archivos de registro implementada por [!DNL Platform Server] ( `PS::LogDays`). El valor predeterminado es [!DNL logs/Supervisor.log].

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que los permisos de acceso estén configurados de modo que el Supervisor del servidor tenga los privilegios necesarios de creación, lectura y escritura.

## SV::tracelevel - Nivel de registro de seguimiento del supervisor del servidor {#section-36f8634741da4c618d67aa628b5fe474}

El nivel de registro puede ser 1, 2, 3 o 4. El valor predeterminado es 2.

## IS::Log: Ruta del archivo de registro de depuración del servidor de imágenes {#section-73a3f09b77f2446c9f82207b7d8aec39}

Carpeta y nombre de archivo base para los archivos de registro de seguimiento de Image Server. La ruta puede ser absoluta o relativa a *[!DNL install_folder]*. ImageServer adjuntará un guión y la fecha actual ( *[!DNL -yyyy-mm-dd]*) al nombre del archivo (antes del sufijo del archivo, si lo hay). Se recomienda enviar los archivos de registro del servidor de imágenes a la misma carpeta que [!DNL Platform Server] archivos de registro ( `PS::LogFolder`) para aprovechar la administración de archivos de registro implementada por [!DNL Platform Server] (consulte `PS::LogDays`).

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que los permisos de acceso estén configurados de modo que el servicio de imágenes tenga los privilegios necesarios de creación, lectura y escritura.

## IS:TraceClient: nivel de registro de depuración del servidor de imágenes {#section-3851f1f68e404430985c629ac80534db}

El nivel de registro puede ser 1, 2, 3 o 4 (el valor predeterminado es 2)

El nivel 1 registra eventos relacionados con el inicio, el cierre y la [!DNL Platform Server] conexiones.

El nivel 2 también registra la conexión y desconexión de las imágenes de origen.

El nivel 3 agrega el registro de solicitudes de datos de píxeles y la entrega de los mismos a la [!DNL Platform Server].

El nivel 4 registra todos los mensajes recibidos del [!DNL Platform Server].

Los niveles 3 y 4 deben utilizarse únicamente con fines de depuración, ya que los archivos de registro pueden llegar a ser muy grandes.

## IS::TraceStatsInterval: intervalo de registro de estadísticas del servidor de imágenes {#section-1d8df96d61044e33a5b2b2b0309c2d59}

El servidor de imágenes escribe estadísticas de memoria en su archivo de registro de seguimiento en el intervalo especificado por esta configuración. El intervalo válido es de 5 a 86 400 segundos.
