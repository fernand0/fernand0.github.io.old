---
layout: post
title: "Las optimizaciones del compilador y la seguridad"
date: "Fri Jan 02 17:40:01 +0100 2015"
category: seguridad
tags: seguridad optimización compilador pruebas tests
---

Un compilador no sólo genera código ejecutable a partir de nuestros programas escritos en un lenguaje de alto nivel. Tradicionalmente los compiladores han tratado de mejorar el código desarrollado por los programadores para hacerlo más eficiente (sacando partido de las características de la arquitectura en la que se va a ejecutar, los mecanimos de los procesaores, sus recursos...).


<a href="https://500px.com/photo/66381679/giteando-by-fernando-tricas" title="Giteando"><img src="https://ppcdn.500px.org/66381679/d50c5e1f55d5e1b8bc2b9f2cc3a585ceb8c9415e/4.jpg" width="240"  alt="Letras en la terminal" style="float:left; margin:5px"></a>

>Compilers are great at taking your hand crafted human-readable program, translating it into machine code and, in the process, optimizing it so it runs as efficiently as possible

Los investigadores del MIT Xi Wang, Nickolai Zeldovich, M. Frans Kaashoek y Armando Solar-Lezama han presentado un artículo donde se evalúan las consecuencias de seguridad que puede tener la eliminación de código que puede hacer el compilador por ser considerado innecesario.

>... research from MIT points out, in their zeal to optimize your code, compilers can go too far and remove code that they shouldn’t, which can make the system or application more vulnerable.

También han desarrollado una herramienta, que nos avisará del código que es susceptible de tener este tipo de problemas, para que lo podamos arreglar:

>The good news is the researchers have developed a model and a static checker for identifying unstable code. Their checker is called [STACK](http://css.csail.mit.edu/stack/), and it currently works for checking C/C++ code. The idea is that it will warn programmers about unstable code in their applications, so they can fix it, rather than have the compiler simply leave it out. They also hope it will encourage compiler writers to rethink how they can optimize code in more secure ways.
