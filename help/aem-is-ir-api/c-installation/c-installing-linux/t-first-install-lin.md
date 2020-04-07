---
description: Este procedimiento muestra cómo instalar el servicio de imágenes por primera vez en Linux.
seo-description: Este procedimiento muestra cómo instalar el servicio de imágenes por primera vez en Linux.
seo-title: Instalación por primera vez
solution: Experience Manager
title: Instalación por primera vez
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: c5b68038fa5980c7051fae916520b40e17890a7f

---


# Instalación por primera vez{#installing-for-the-first-time}

Este procedimiento muestra cómo instalar el servicio de imágenes por primera vez en Linux.

1. Inicie sesión en el host del servidor con permisos de raíz.
1. Cree la carpeta [!DNL /usr/local/scene7/licenses].

   Si el archivo de clave de licencia de servicio de imágenes y/o procesamiento de imágenes (con [!DNL .sc8] sufijo de archivo) está disponible, cópielo en esta carpeta. De lo contrario, continúe con la instalación e instale la clave de licencia más tarde.
1. Descomprima y descomprima el archivo tar de distribución de servicio de imágenes.
1. Ejecute [!DNL ./install-is], ubicado en la [!DNL Setup] carpeta, para iniciar el asistente de instalación.

   Si no se encuentra ninguna clave de licencia, se muestran instrucciones que describen cómo obtener un archivo de licencia. Realice esta acción en este momento o continúe con la instalación del servicio de imágenes e instale la clave de licencia más tarde.
1. Cuando aparezca el Contrato de licencia de usuario final (EULA), lea el contrato de licencia y, a continuación, introduzca `y` para continuar.

   El programa de instalación muestra las indicaciones que se indican en la tabla siguiente.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Puerto de escucha principal [8080]:</span> </p> </td> 
   <td colname="col2"> <p>Puerto de escucha HTTP principal para el servicio de imágenes y el procesamiento de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Puerto de escucha del administrador [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Puerto de escucha del administrador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Tamaño máximo de caché HTTP (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Tamaño inicial de la caché de respuesta principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Carpeta raíz de caché [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>Carpeta de caché de PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID del propietario del servidor de imágenes [raíz]:</span> </p> </td> 
   <td colname="col2"> <p>Cuenta de usuario en la que se instalarán los servidores de servicio de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID del grupo de servidores de imágenes [raíz]:</span> </p> </td> 
   <td colname="col2"> <p>Cuenta de grupo en la que se instalarán los servidores de servicio de imágenes. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Pulse **[!UICONTROL Intro]** para aceptar el valor predeterminado o especifique otro valor.

   Asegúrese de que todos los números de puerto especificados sean únicos y de que no se utilicen de otro modo en este host.

   **Importante: **Si se especifica una cuenta que no sea la raíz, debe asegurarse de que los permisos de acceso para todos los archivos y carpetas que el servidor de imágenes necesita leer o escribir se configuran correctamente cuando estas carpetas se reconfiguran en los archivos de configuración.
>El servicio de imágenes ahora está instalado en [!DNL /usr/local/Scene7/ImageServing]. Se ha instalado cierto contenido de procesamiento de imágenes en [!DNL /usr/local/Scene7/ImageRendering].
>
>Hacia el final de la instalación, el asistente de instalación intenta realizar inicio de Image Server. Si no se encuentra ninguna clave de licencia válida, el servidor de imágenes no puede realizar inicios. Si hay una licencia válida y el servidor de imágenes aún no se está iniciando, consulte los archivos de registro.
>[!NOTE]
Si la licencia se instala después de instalar el servicio de imágenes, el servidor de imágenes debe iniciarse manualmente antes de utilizarlo.
>
>
>

