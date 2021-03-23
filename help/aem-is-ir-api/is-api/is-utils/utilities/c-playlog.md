---
description: La utilidad playlog se puede utilizar para generar previamente contenido para la caché de respuestas HTTP.
seo-description: La utilidad playlog se puede utilizar para generar previamente contenido para la caché de respuestas HTTP.
seo-title: La utilidad "playlog"
solution: Experience Manager
title: La utilidad "playlog"
uuid: 9044515e-7cfb-4e86-9ac4-e071b60f38d1
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 1%

---


# La utilidad &quot;playlog&quot;{#the-playlog-utility}

La utilidad playlog se puede utilizar para generar previamente contenido para la caché de respuestas HTTP.

La caché de respuestas HTTP del servicio de imágenes existente no está garantizada y se puede utilizar después de una actualización de versión principal (cuando ha cambiado el primer o el segundo dígito del número de versión). Si se va a tomar el servidor en vivo en condiciones de carga completa después de la actualización, el servidor puede estar sobrecargado entregando las primeras horas de solicitudes de pérdida de caché hasta que la caché se rellene razonablemente y la tasa de visitas de la caché aumente.

Para evitar este pico de carga inicial, la utilidad `playlog` puede usarse para generar previamente contenido para la caché de respuestas HTTP. `playlog` extrae solicitudes HTTP de un archivo de registro de acceso existente y las envía al servidor para generar entradas de caché. En los casos de uso habituales, basta con reproducir un solo archivo de registro de acceso que contenga el tráfico de un día completo.

Además de purgar la caché de respuesta HTTP después de la instalación de la actualización, la utilidad también se utiliza para generar previamente el contenido de la caché al añadir un nuevo servidor a un entorno de carga equilibrada; simplemente reproduzca un archivo de registro reciente de uno de los demás servidores.

`playlog` se puede configurar para admitir la mayoría de los archivos de registro de acceso generados por versiones anteriores de Image Serving.

## Uso {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p  <span class="varname"> prefix  </span> </span> </p> </td> 
  <td class="stentry"> <p>URL raíz para anteponer a las solicitudes extraídas del archivo de registro. </p> <p>Predeterminado: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de campo (columna) que contiene la solicitud en el registro de registro; Basado en 1. </p> <p>Predeterminado: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s  <span class="varname"> separador  </span> </span> </p> </td> 
  <td class="stentry"> <p>Separador de campos; patrón de expresión regular. </p> <p>Predeterminado: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m  <span class="varname"> marcador  </span> </span> </p> </td> 
  <td class="stentry"> <p>Marcador de solicitud; identifica las solicitudes del archivo de registro que deben reproducirse; patrón de expresión regular. </p> <p>Predeterminado: <span class="codeph"> Solicitud: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x  <span class="varname"> sufijo  </span> </span> </p> </td> 
  <td class="stentry"> <p>Sufijo para anexar a la solicitud extraída del archivo de registro; se puede utilizar para separar las solicitudes de reproducción de las solicitudes en directo en los archivos de registro; a '?' o el separador "&amp;" se inserta automáticamente; puede hacer referencia a cualquier campo de registro por posición entre llaves; el valor predeterminado corresponde al campo de firma md5. </p> <p>Predeterminado: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v  </span> </p> </td> 
  <td class="stentry"> <p>En el modo detallado, imprime las direcciones URL de solicitud generadas en <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p>Imprima una sinopsis a <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method: método de solicitud HTTP para usar ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Predeterminado: <span class="codeph"> inteligente </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos en el archivo de registro para obtener el método original. </p> <p>Predeterminado: 15 </p> </td> 
 </tr> 
</table>

Para Windows, el nombre de archivo es [!DNL playlog.bat] y en Linux es [!DNL playlog.sh].

## Ejemplos {#section-716e5c35e9fa4ee3a4b0687381fcea40}

El siguiente ejemplo reproduce todas las solicitudes de un archivo de registro de acceso creado por Image Serving en Linux:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

El siguiente comando reproduce todas las solicitudes encontradas en un archivo de registro de seguimiento creado por Image Serving en Windows:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
