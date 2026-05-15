---
title: Macros de comandos
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
TQID: 'https://experienceleague.adobe.com/cXLJJQ5CS-Apmq-8qYV-ew-lcvfRjoNfIbl2qyyKB6U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Macros de comandos{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.

`$ *[!DNL name]*$`

**&#x200B; *[!DNL name]* &#x200B;** nombre de macro

Las macros se definen en ficheros de definición de macros independientes, que pueden adjuntarse a catálogos de material o al catálogo predeterminado.

*[!DNL name]* no distingue entre mayúsculas y minúsculas y puede consistir en cualquier combinación de letras ASCII, números, caracteres &quot;-&quot;, &quot;_&quot; y &quot;.&quot;.

Invocar macros desde cualquier lugar de una solicitud después de &quot;?&quot; o desde cualquier lugar dentro de un campo de `vignette::Modifier`. Las macros solo pueden representar uno o más comandos de procesamiento de imágenes y deben separarse de otros comandos con separadores &quot;&amp;&quot;.

Las invocaciones a macros se sustituyen por sus cadenas de sustitución al principio del análisis. Los comandos dentro de las macros anulan los mismos comandos de la solicitud si se producen antes de la invocación de la macro en la solicitud. Este flujo de trabajo es diferente de `vignette::Modifier`, donde los comandos de la cadena de solicitud anulan los comandos de la cadena `vignette::Modifier`, independientemente de la posición en la solicitud.

Las macros de comandos no pueden tener valores de argumento, pero se pueden utilizar variables personalizadas para pasar valores de la solicitud a la macro.

Las macros no pueden estar anidadas.

**Ejemplo**

Las macros pueden resultar útiles si se van a aplicar los mismos comandos o atributos a distintas imágenes procesadas.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Puede definir una macro para los atributos comunes:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro se usaría de la siguiente manera:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Dado que `qlt=` es diferente para la tercera solicitud, el software anula el valor después de invocar la macro (especificando `qlt=` *antes* `$render$`no es eficaz).

**Ver también**

`catalog::MacroFile`, `catalog::Modifier`, referencia de definición de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
