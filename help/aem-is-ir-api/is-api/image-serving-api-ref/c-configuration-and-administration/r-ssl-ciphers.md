---
description: La etiqueta Connector en server.xml admite un atributo ciphers para limitar los cifrados que se pueden elegir para una conexión SSL.
seo-description: La etiqueta Connector en server.xml admite un atributo ciphers para limitar los cifrados que se pueden elegir para una conexión SSL.
seo-title: Definición de cifrados SSL
solution: Experience Manager
title: Definición de cifrados SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: 9490fb9a-5abb-4f5e-b660-b7af0a5e4b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Definición de cifrados SSL{#defining-ssl-ciphers}

La etiqueta Connector en server.xml admite un atributo ciphers para limitar los cifrados que se pueden elegir para una conexión SSL.

De forma predeterminada, todos los cifrados están disponibles. La lista está separada por comas y puede contener cualquiera de los siguientes valores:

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

Si alguno de los valores es incorrecto, Tomcat habilitará cada cifrado individual. Por lo tanto, es esencial comprobar con una herramienta externa después de la configuración qué cifrados están realmente habilitados.

A modo de ejemplo, la siguiente configuración sólo habilitará los grupos de cifrado de &quot;128 bits&quot; y superiores:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
