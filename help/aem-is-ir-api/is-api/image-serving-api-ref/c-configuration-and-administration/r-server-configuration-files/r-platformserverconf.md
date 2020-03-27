---
description: Contiene la configuración de Platform Server.
seo-description: Contiene la configuración de Platform Server.
seo-title: PlatformServer.conf
solution: Experience Manager
title: PlatformServer.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: d798762b-c9ff-4e1b-b2ac-c5e40476b375
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PlatformServer.conf{#platformserver-conf}

Contiene la configuración de Platform Server.

Este archivo es un archivo de propiedades de JAVA. Se debe velar por el cumplimiento de las convenciones pertinentes; de lo contrario, puede que el Servidor de plataformas no pueda realizar el inicio. Utilice una barra invertida de doble &#39;\\&#39; o una sola barra diagonal inversa &#39;/&#39; en lugar de una barra invertida &#39;\&#39; en las rutas de archivos de Windows. La barra invertida se utiliza como carácter de escape en este tipo de archivo.

Los cambios realizados en este archivo surtirán efecto una vez guardado el archivo.

Solo se puede cambiar la configuración que se muestra a continuación en [!DNL PlatformServer.conf]. Si no hay una configuración concreta, puede agregarla en cualquier parte del archivo. Solo puede haber una instancia de cada configuración.

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configuración general del servidor de plataformas </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000 </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824 </span> </p> <p> <span class="codeph"> isConnection.port=27345 </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequsts=true </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000 </span> </p> <p> <span class="codeph"> staticContent.rootPaths=./static-content </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configuración del clúster de caché </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;vacío&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50 </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000 </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configuración de redirección de errores </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000 </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configuración de SVG </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./imágenes </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024 </span> </p> <p> <span class="codeph"> svgProvider.port=8080 </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./imágenes </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Respuestas al conjunto de medios </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10 </span> </p> <p> <span class="codeph"> fvctx.folureLimit=20 </span> </p> </td> 
 </tr> 
</table>

