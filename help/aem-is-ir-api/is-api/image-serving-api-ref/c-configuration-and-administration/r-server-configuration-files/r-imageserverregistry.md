---
description: Contiene la configuración del servidor de imágenes.
seo-description: Contiene la configuración del servidor de imágenes.
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Contiene la configuración del servidor de imágenes.

Al modificar este archivo XML, se debe tener cuidado de mantener una sintaxis XML válida; de lo contrario, el servidor de imágenes podría no realizar el inicio.

Para que los cambios surtan efecto, reinicie el servidor de imágenes después de editar este archivo. Solo se admiten para la modificación los valores de elementos que se enumeran a continuación. Edite cualquier otro contenido de este archivo solo cuando el servicio de asistencia técnica de Scene7 lo aconseje.

>[!NOTE]
>
>No cambie la estructura de `<imageserverregistry>`, incluido el orden de los elementos. Tenga cuidado al editar este archivo; de lo contrario, el servidor de imágenes podría no tener inicios.

El siguiente ejemplo ilustra qué elementos se pueden cambiar. Hay otros elementos que no deben modificarse. El orden de los elementos siguientes no refleja el orden en que deben estar presentes en el archivo.

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## Notas {#section-7217f011f69f41e7af4f3983d7776d6f}

Pueden estar presentes varios `<RootPath>` elementos (uno para cada carpeta de archivo de datos de origen). El servidor de imágenes busca las rutas raíz en el orden especificado para encontrar un archivo de origen determinado.
