---
description: La utilidad playlog se puede utilizar para generar previamente contenido para la caché de respuesta HTTP.
seo-description: La utilidad playlog se puede utilizar para generar previamente contenido para la caché de respuesta HTTP.
seo-title: La utilidad 'playlog'
solution: Experience Manager
title: La utilidad 'playlog'
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9044515e-7cfb-4e86-9ac4-e071b60f38d1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 1%

---


# La utilidad &#39;playlog&#39;{#the-playlog-utility}

La utilidad playlog se puede utilizar para generar previamente contenido para la caché de respuesta HTTP.

La caché de respuesta HTTP del servicio de imágenes existente no está garantizada para su uso después de una actualización de versión principal (cuando se cambió el primer o segundo dígito del número de versión). Si se va a activar el servidor en condiciones de carga completa después de la actualización, es posible que el servidor esté sobrecargado entregando las primeras horas de solicitudes de pérdida de memoria caché hasta que la memoria caché se rellene razonablemente y la velocidad de visitas de la memoria caché aumente.

Para evitar este pico de carga inicial, la utilidad `playlog` puede utilizarse para generar previamente contenido para la caché de respuesta HTTP. `playlog` extrae solicitudes HTTP de un archivo de registro de acceso existente y las envía al servidor para generar entradas de caché. En escenarios de uso típicos, basta con reproducir un único archivo de registro de acceso que contenga el tráfico de un día completo.

Además de purgar la caché de respuesta HTTP después de la instalación de la actualización, la utilidad también se utiliza para generar previamente el contenido de la caché al agregar un nuevo servidor a un entorno de equilibrio de carga; simplemente reproduzca un archivo de registro reciente de uno de los otros servidores.

`playlog` se puede configurar para admitir la mayoría de los archivos de registro de acceso generados por versiones anteriores de servicio de imágenes.

## Uso {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p  <span class="varname"> prefijo  </span> </span> </p> </td> 
  <td class="stentry"> <p>Dirección URL raíz para anteponer a las solicitudes extraídas del archivo de registro. </p> <p>Predeterminado: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de campo (columna) que contiene la solicitud en el registro de registro; Basado en 1. </p> <p>Predeterminado: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s  <span class="varname"> separador  </span> </span> </p> </td> 
  <td class="stentry"> <p>Separador de campo; patrón de expresión regular. </p> <p>Predeterminado: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m  <span class="varname"> marcador  </span> </span> </p> </td> 
  <td class="stentry"> <p>Marcador de solicitud; identifica las solicitudes del archivo de registro que deben reproducirse; patrón de expresión regular. </p> <p>Predeterminado: <span class="codeph"> Solicitud: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x  <span class="varname"> sufijo  </span> </span> </p> </td> 
  <td class="stentry"> <p>Sufijo que se anexará a la solicitud extraída del archivo de registro; se puede utilizar para separar las solicitudes reproducidas de las solicitudes activas en los archivos de registro; a '?' o el separador '&amp;' se inserta automáticamente; puede hacer referencia a cualquier campo de registro por su posición entre llaves; el valor predeterminado corresponde al campo de firma md5. </p> <p>Predeterminado: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v  </span> </p> </td> 
  <td class="stentry"> <p>El modo detallado imprime las direcciones URL de solicitud generadas en <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p>Imprima una sinopsis a <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method - Método de solicitud HTTP que se va a utilizar ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Predeterminado: <span class="codeph"> inteligente </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos: coloque en el archivo de registro para capturar el método original. </p> <p>Predeterminado: 15 </p> </td> 
 </tr> 
</table>

Para Windows, el nombre de archivo es [!DNL playlog.bat] y en Linux es [!DNL playlog.sh].

## Ejemplos {#section-716e5c35e9fa4ee3a4b0687381fcea40}

El siguiente ejemplo reproduce todas las solicitudes de un archivo de registro de acceso creado por el servicio de imágenes en Linux:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

El siguiente comando reproduce todas las solicitudes encontradas en un archivo de registro de seguimiento creado por el servicio de imágenes en Windows:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
