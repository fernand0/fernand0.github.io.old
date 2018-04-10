---
layout: post
title: "Aprender a programar con fallos de seguridad"
date: "Tue Apr 10 16:02:01 +0100 2018"
category: seguridad
tags: [seguridad, programación, ejemplos, tutoriales, código, copia, github]
imagefeature: https://c1.staticflickr.com/3/2215/1535752807_4181367fa9_m.jpg
---


<a href="https://www.slideshare.net/fernand0/seguridad-aplicaciones-web" title="La presentación"><img src="https://scontent-mad1-1.xx.fbcdn.net/v/t1.0-9/29571039_10155459524433226_7401524006947639501_n.jpg?_nc_cat=0&oh=ff4d476242c585d28a13f0932ef94abe&oe=5B3CC1D4" width="240"  alt="En clase" style="float:left; margin:5px"></a>
Lo leí en algún libro (creo que en el de John Viega y Gary McGraw, 'Building Secure Software'). Allí se decía que no sólo no se enseñaba el tema del desarrollo seguro sino que, además, los ejemplos que se podían ver en los libros de programación (en aquella época libros, fundamentalmente) eran de dudosa calidad desde el punto de vista de la seguridad. También se discutía (creo) sobre los ejemplos y sobre los ficheros de configuración.  Casi 20 años después seguimos igual: en [Top-ranked programming Web tutorials introduce vulnerabilities into software](https://www.helpnetsecurity.com/2017/04/21/programming-tutorials-vulnerabilities/) nos dicen algo muy similar. Los tutoriales más importantes de desarrollo web incluyen ejemplos y soluciones vulnerables.

La forma de obtener el dato es curiosa: navegan por el repositorio GitHub y encuentran vulnerabilidades que pueden encontrarse en algunos textos introductorios disponibles por ahí.

> Researchers from several German universities have checked the PHP  codebases of over 64,000 projects on GitHub, and found 117 vulnerabilities that they believe have been introduced through the use of code from popular but insufficiently reviewed tutorials.

Utilizan la búsqueda en el repositorio de patrones bien conocidos de fallo, que se pueden encontrar en los tutoriales. Y encuentran problemas, claro:

> Thanks to our framework, we have uncovered over 100 vulnerabilities in web application code that bear a strong resemblance to vulnerable code patterns found in popular tutorials. More alarmingly, we have confirmed that 8 instances of a SQLi vulnerability present in different web applications are an outcome of code copied from a single vulnerable tutorial,” they noted. “Our results indicate that there is a substantial, if not causal, link between insecure tutorials and web application > vulnerabilities.”

Casi nada. En un caso concreto 8 ejemplos de un fallo que proviene de uno de estos tutoriales.

Proporcionan sus herramientas [GithubSpider](https://github.com/tommiu/GithubSpider) para hacer las búsquedas, y [ccdetection](https://github.com/tommiu/ccdetection) para hacer la detección de código similar.

Si haces cursos y tutoriales, o si ya tienes algunos publicados, tienes una responsabilidad.

También tengo que decir que hace años propuse algo así (cuando pensábamos en temas de propagación de información) relacionado con la propagación de errores en los programas a través de ejemplos, copia, etc. en una presentación que nunca llegué a publicar, así que pueden creerme o no sobre el tema.
