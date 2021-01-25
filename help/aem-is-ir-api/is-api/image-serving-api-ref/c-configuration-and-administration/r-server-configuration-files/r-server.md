---
description: Contiene la configuración del servidor de la plataforma.
seo-description: Contiene la configuración del servidor de la plataforma.
seo-title: server.xml
solution: Experience Manager
title: server.xml
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---


# server.xml{#server-xml}

Contiene la configuración del servidor de la plataforma.

Al modificar este archivo XML, se debe tener cuidado de mantener una sintaxis XML válida; de lo contrario, puede que el servidor de plataforma no pueda realizar el inicio.

Para que los cambios surtan efecto, se debe reiniciar el servidor de plataforma después de editar este archivo.

El diagrama siguiente ilustra qué configuración se puede cambiar en este archivo. Consulte las secciones correspondientes anteriores de este documento para obtener una descripción de esta configuración. Tenga en cuenta que este diagrama no es una representación completa de [!DNL server.xml].

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```

