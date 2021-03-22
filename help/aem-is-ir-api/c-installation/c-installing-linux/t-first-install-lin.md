---
description: Este procedimiento muestra cómo instalar Image Serving por primera vez en Linux.
seo-description: Este procedimiento muestra cómo instalar Image Serving por primera vez en Linux.
seo-title: Instalación por primera vez
solution: Experience Manager
title: Instalación por primera vez
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---


# Instalación por primera vez{#installing-for-the-first-time}

Este procedimiento muestra cómo instalar Image Serving por primera vez en Linux.

1. Inicie sesión en el host del servidor con permisos de raíz.
1. Cree la carpeta [!DNL /usr/local/scene7/licenses].

   Si el archivo de la clave de licencia de Image Serving o Image Rendering (con el sufijo [!DNL .sc8] file) está disponible, cópielo en esta carpeta. De lo contrario, proceda con la instalación e instale la clave de licencia más adelante.
1. Descomprima y descomprima el archivo tar de distribución de Image Serving.
1. Ejecute [!DNL ./install-is], ubicado en la carpeta [!DNL Setup], para iniciar el asistente de instalación.

   Si no se encuentra ninguna clave de licencia, se muestran instrucciones que describen cómo obtener un archivo de licencia. Hágalo en este punto o continúe con la instalación de Image Serving e instale la clave de licencia más tarde.
1. Cuando aparezca el Acuerdo de licencia del usuario final (EULA), lea el acuerdo de licencia y, a continuación, introduzca `y` para continuar.

   El instalador muestra las indicaciones que se enumeran en la siguiente tabla.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Puerto de escucha principal [8080]:</span> </p> </td> 
   <td colname="col2"> <p>Puerto de escucha HTTP principal para el servicio de imágenes y el procesamiento de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Puerto de escucha de administración [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Puerto de escucha del administrador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Tamaño máximo de caché HTTP (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Tamaño inicial de la caché de respuesta principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Carpeta raíz de caché [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>Carpeta de caché PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID de propietario del servidor de imágenes [raíz]:</span> </p> </td> 
   <td colname="col2"> <p>Cuenta de usuario en la que se deben instalar los servidores de servicio de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID del grupo del servidor de imágenes [raíz]:</span> </p> </td> 
   <td colname="col2"> <p>Cuenta de grupo en la que se deben instalar los servidores de servicio de imágenes. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Pulse **[!UICONTROL Enter]** para aceptar el valor predeterminado o especificar un valor diferente.

   Asegúrese de que todos los números de puerto especificados sean únicos y no se utilicen de otro modo en este host.

   >[!IMPORTANT]
   >
   >Si se especifica una cuenta que no sea la raíz, debe asegurarse de que los permisos de acceso para todos los archivos y carpetas que el servidor de imágenes necesita leer o escribir estén correctamente configurados cuando estas carpetas se reconfiguren en los archivos de configuración.
   >
   >El servicio de imágenes ahora está instalado en [!DNL /usr/local/Scene7/ImageServing]. Cierto contenido de procesamiento de imágenes está instalado en [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Hacia el final de la instalación, el asistente de instalación intenta iniciar Image Server. Si no se encuentra ninguna clave de licencia válida, Image Server no puede iniciarse. Si hay una licencia válida y Image Server aún no se está iniciando, consulte los archivos de registro.

>[!NOTE]
>
>Si la licencia se instala después de instalar Image Serving, Image Server debe iniciarse manualmente antes de utilizarse.
