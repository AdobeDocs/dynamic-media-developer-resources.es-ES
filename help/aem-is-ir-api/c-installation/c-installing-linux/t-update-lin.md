---
description: Utilice este procedimiento al actualizar Dynamic Media Image Serving en Linux.
solution: Experience Manager
title: Actualización de IS 4.7.4 o posterior
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---


# Actualización de IS 4.7.4 o posterior{#updating-from-is-or-later}

Utilice este procedimiento al actualizar Dynamic Media Image Serving en Linux.

Si está actualizando desde una versión anterior de Image Serving, póngase en contacto con el servicio de asistencia técnica para el proceso correcto.

La carpeta [!DNL webapps] se puede eliminar al actualizar. Haga una copia de seguridad de la carpeta [!DNL webapps] antes de la actualización.

1. Inicie sesión en el host del servidor con privilegios de root.
1. Descomprima y descomprima el archivo tar de distribución de Image Serving.
1. Ejecute [!DNL ./install-is] para iniciar el asistente de instalación que se encuentra en la carpeta [!DNL setup].

   El instalador de actualización comprueba la integridad y la versión del paquete instalado. Si se realiza correctamente, se muestra el Acuerdo de licencia del usuario final (&quot;EULA&quot;).
1. Lea el contrato de licencia y, a continuación, introduzca &quot;**[!UICONTROL y]**&quot; para continuar con la instalación.

   El instalador realiza una copia de seguridad de los archivos de configuración antiguos del servidor en la carpeta [!DNL BACKUP/].

   Cuando se completa la instalación, se muestra el siguiente mensaje:

   `Image Server was started successfully`

Durante una actualización, el archivo [!DNL ImageServing/conf/server.xml] se actualiza a la configuración más reciente. Si ha cambiado o agregado algún valor, debe guardar el [!DNL server.xml] existente y volver a implementar los cambios después de la actualización.

Después de una instalación de actualización, considere la posibilidad de calentar la caché de respuestas HTTP antes de activar el servidor. Consulte la descripción de la utilidad [!DNL playlog] para obtener más información.
