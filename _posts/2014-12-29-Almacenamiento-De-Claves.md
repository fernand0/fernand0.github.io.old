---
layout: post
title: "Consejos para almacenar las claves"
date: "Wed Dec 29 20:55:01 +0100 2014"
category: seguridad
tags: seguridad claves contraseñas almacenamiento   
---

En [Do any security experts recommend bcrypt for password storage?](http://security.stackexchange.com/questions/4781/do-any-security-experts-recommend-bcrypt-for-password-storage) y, en particular, en la primera respuesta un buen texto sobre el almacenamiento de claves y los algoritmos adecuados para hacerlo. Se discute [Bcrypt](http://en.wikipedia.org/wiki/Bcrypt), [PBKDF2](http://en.wikipedia.org/wiki/PBKDF2).

Para este tipo de almacenamiento hoy en día hay que tener en cuenta ataques bastante esotéricos con [GPU](http://en.wikipedia.org/wiki/Graphics_processing_unit) (procesadores gráficos) y [FPGA](http://en.wikipedia.org/wiki/Field-programmable_gate_array) como herramientas de cálculo masivo de manera muy eficiente. Los nuevos algoritmos tienen que tener en cuenta no sólo la velocidad de cálculo, sino también la cantidad de RAM utilizada y otros parámetros.
