---
description: Contiene los ajustes de configuración del servidor de imágenes.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Contiene los ajustes de configuración del servidor de imágenes.

Al modificar este archivo XML, se debe tener cuidado de mantener una sintaxis XML válida; de lo contrario, el servidor de imágenes puede no iniciarse.

Para que los cambios surtan efecto, reinicie Image Server después de editar este archivo. Solo se admiten para modificación los valores de elemento enumerados a continuación. Edite cualquier otro contenido de este archivo solo cuando el soporte técnico de Dynamic Media lo aconseje.

>[!NOTE]
>
>No cambie la estructura de `<imageserverregistry>`, incluido el orden de los elementos. Tenga cuidado al editar este archivo; de lo contrario, el servidor de imágenes podría no iniciarse.

El siguiente ejemplo ilustra qué elementos se pueden cambiar. Hay otros elementos presentes que no deben cambiarse. El orden de los elementos siguientes no refleja el orden en que deben estar presentes en el archivo.

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

Pueden estar presentes varios elementos `<RootPath>` (uno para cada carpeta de archivo de datos de origen). Image Server busca las rutas raíz en el orden especificado para encontrar un archivo de origen concreto.
