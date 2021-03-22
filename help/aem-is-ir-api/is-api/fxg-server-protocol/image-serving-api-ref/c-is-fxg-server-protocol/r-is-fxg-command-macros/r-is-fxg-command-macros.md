---
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
seo-description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
seo-title: Macros de comandos
solution: Experience Manager
title: Macros de comandos
uuid: f90d5132-aa5b-424f-a123-838723ed891a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---


# Comando macros{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.

Las macros se definen en archivos de definición de macro separados, que pueden adjuntarse a catálogos de imágenes o al catálogo predeterminado.

Las macros se pueden invocar en cualquier parte de una solicitud después de &#39;?&#39;, así como en cualquier parte dentro de un campo `catalog::Modifier`. Las macros solo pueden representar uno o más comandos completos de Image Serving, por lo que deben estar encerrados por separadores &quot;&amp;&quot; (excepto cuando se encuentra al principio o al final de la cadena modificadora).

Las invocaciones de macro se sustituyen por sus cadenas de sustitución antes de analizar. Los comandos dentro de las macros anulan los mismos comandos en la solicitud si se producen antes de la invocación de macro en la solicitud. Esto es diferente a `catalog::Modifier`, donde los comandos de la cadena de solicitud siempre anulan los comandos de la cadena `catalog::Modifier`, independientemente de la posición en la solicitud.

Las macros se pueden anidar, con la siguiente restricción: una macro solo puede invocarse si ya está definida en el momento en que se analiza la definición de la macro, ya sea al aparecer antes en el mismo archivo de definición de macro o al colocar la definición de dicha macro incrustada en el archivo de definición de macro predeterminada.

Las macros pueden resultar útiles si se van a aplicar los mismos atributos a diferentes imágenes.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Podemos definir una macro para los atributos comunes:

`view wid=240&fmt=pdf&imageRes=300`

La macro se utilizaría de la siguiente manera:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Dado que `wid=` es diferente para la tercera solicitud, simplemente anulamos el valor *después* de invocar la macro (especificar `wid=`*antes* `$view$` no tendría ningún efecto).

+ [name](r-name.md)
