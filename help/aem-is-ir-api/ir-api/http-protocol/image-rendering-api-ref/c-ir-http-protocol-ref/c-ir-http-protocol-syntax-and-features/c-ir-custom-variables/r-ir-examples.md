---
description: En este ejemplo se utiliza Image Serving para colorear un objeto y aplicar un calco que contenga texto personalizado en uno de los conjuntos de viñetas.
solution: Experience Manager
title: Ejemplos
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---


# Ejemplos{#examples}

En este ejemplo se utiliza Image Serving para colorear un objeto y aplicar un calco que contenga texto personalizado en uno de los conjuntos de viñetas.

Las variables IR se utilizan para identificar la viñeta, la imagen del logotipo y el texto personalizado.

El campo `vignette::Modifier` del registro denominado *template* en el mapa de viñetas del catálogo de materiales `myCat` contiene lo siguiente:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Todas las viñetas que se vayan a utilizar se enumeran en el mapa de viñetas del catálogo de materiales `myCat`.

El cliente ahora puede realizar la siguiente solicitud para recuperar la imagen predeterminada (esto utiliza las variables definidas al principio de la plantilla):

[!DNL `https://server/myCat/template`]

La siguiente solicitud especifica cierto contenido para procesar:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Consulte la documentación de Image Serving para obtener más información sobre el comando Image Serving `text=`.
