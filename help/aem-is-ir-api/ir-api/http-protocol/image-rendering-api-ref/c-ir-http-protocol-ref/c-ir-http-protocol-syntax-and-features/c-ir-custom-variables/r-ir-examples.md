---
description: En este ejemplo se utiliza Image Serving para colorear un objeto y aplicar un calco que contenga texto personalizado en uno de los conjuntos de viñetas.
seo-description: En este ejemplo se utiliza Image Serving para colorear un objeto y aplicar un calco que contenga texto personalizado en uno de los conjuntos de viñetas.
seo-title: Ejemplos
solution: Experience Manager
title: Ejemplos
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
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
