---
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
solution: Experience Manager
title: Macros de comandos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Macros de comandos{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.

Las macros se definen en archivos de definición de macros independientes, que se pueden adjuntar a los catálogos de imágenes o al catálogo predeterminado.

Las macros pueden invocarse en cualquier lugar de una solicitud después de &quot;?&quot;, así como en cualquier lugar dentro de un `catalog::Modifier` field. Las macros solo pueden representar uno o más comandos completos del servicio de imágenes; por lo tanto, deben incluirse entre separadores &quot;&amp;&quot; (excepto cuando se encuentran al principio o al final de la cadena del modificador).

Las invocaciones a macros se sustituyen por sus cadenas de sustitución al principio del análisis. Los comandos dentro de las macros anularán los mismos comandos de la solicitud si se producen antes de la invocación de la macro en la solicitud. Esto es diferente a `catalog::Modifier`, donde los comandos de la cadena de solicitud siempre anulan los comandos de `catalog::Modifier` cadena, independientemente de la posición en la solicitud.

Las macros pueden estar anidadas, con la siguiente restricción: una macro sólo puede invocarse si ya está definida en el momento en que se analiza la definición de la macro, ya sea apareciendo anteriormente en el mismo archivo de definición de macro o colocando la definición de dicha macro incrustada en el archivo de definición de macro predeterminado.

Las macros pueden resultar útiles si se van a aplicar los mismos atributos a imágenes diferentes.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Podemos definir una macro para los atributos comunes:

`view wid=240&fmt=pdf&imageRes=300`

La macro se usaría de la siguiente manera:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Desde `wid=` es diferente para la tercera solicitud, simplemente anulamos el valor *después* se invoca la macro (especificando `wid=`*antes* `$view$` no tendría ningún efecto).

+ [nombre](r-name.md)
