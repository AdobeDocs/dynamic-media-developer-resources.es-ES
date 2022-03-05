---
title: Ejemplos
description: En este ejemplo se utiliza Image Serving para colorear un objeto y aplicar un calco que contenga texto personalizado en uno de los conjuntos de viñetas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# Ejemplos{#examples}

En este ejemplo se utiliza Image Serving para colorear un objeto y aplicar un calco que contenga texto personalizado en uno de los conjuntos de viñetas.

Las variables IR se utilizan para identificar la viñeta, la imagen del logotipo y el texto personalizado.

La variable `vignette::Modifier` en el registro denominado *plantilla* en el mapa de viñetas del catálogo de materiales `myCat` contiene lo siguiente:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Todas las viñetas usadas aparecen en el mapa de viñetas del catálogo de materiales `myCat`.

El cliente ahora puede realizar la siguiente solicitud para recuperar la imagen predeterminada (utiliza las variables definidas al principio de la plantilla):

[!DNL `https://server/myCat/template`]

La siguiente solicitud especifica cierto contenido para procesar:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Consulte la documentación del servicio de imágenes para obtener más información sobre el servicio de imágenes `text=` comando.
