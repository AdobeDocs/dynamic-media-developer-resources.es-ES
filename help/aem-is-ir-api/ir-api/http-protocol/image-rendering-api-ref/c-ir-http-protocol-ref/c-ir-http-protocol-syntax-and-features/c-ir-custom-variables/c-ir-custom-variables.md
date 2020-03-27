---
description: La parte de consulta de las solicitudes y las cadenas de modificador de viñeta puede incluir variables definidas por el usuario.
seo-description: La parte de consulta de las solicitudes y las cadenas de modificador de viñeta puede incluir variables definidas por el usuario.
seo-title: Variables personalizadas
solution: Experience Manager
title: Variables personalizadas
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Custom variables{#custom-variables}

La parte de consulta de las solicitudes y las cadenas vignette::Modifier pueden incluir variables definidas por el usuario.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variable name. Puede constar de cualquier combinación de caracteres alfa, dígito y seguros, excluyendo &#39;$&#39;.

** *[!DNL value]* ** Valor al que se debe configurar la variable (cadena).

Las variables se definen de forma similar a otros comandos del servidor, utilizando la sintaxis anterior. Las variables deben definirse para poder hacer referencia a ellas. Las variables definidas en se `vignette::Modifier` pueden hacer referencia en la solicitud de URL y viceversa.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>*[!DNL value]* debe tener codificación de dirección URL de paso único para la transmisión HTTP segura. La codificación de Doble es obligatoria si *[!DNL value]* se retransmite mediante HTTP. Este es el caso cuando *[!DNL value]* se sustituye en una solicitud externa anidada.

Para hacer referencia a las variables, incruste el nombre de la variable (entre un valor inicial y un valor final de $) en cualquier lugar de los valores de comando. Por ejemplo, entre el &#39;=&#39; que sigue al nombre del comando y el subsiguiente &#39;&amp;&#39; o el final de la solicitud. El servidor sustituye cada incidencia de $ *[!DNL name]*$ por *[!DNL string]*. No se producirán sustituciones en ninguna ocurrencia de $ *[!DNL name]*$ en nombres de comando (antes del signo igual de un comando) y en la parte de ruta de la solicitud.

Es posible que las variables personalizadas no estén anidadas. No se sustituyen las ocurrencias de $ *[!DNL name]*$ dentro de *[!DNL string]* . Por ejemplo, el fragmento de solicitud `$var2=apple&$var1=my$var2$tree&text=$var1$` se resuelve en `text=my$var2$tree`.

$ no es un carácter reservado; de lo contrario, puede ocurrir en la solicitud. Por ejemplo, `src=my$texture$file.tif` es un comando válido (suponiendo que existe una entrada de catálogo de material o un archivo de textura denominado [!DNL my$texture$file.tif] ), mientras que `wid=$number$` no lo es, porque `wid=` requiere un argumento numérico.
