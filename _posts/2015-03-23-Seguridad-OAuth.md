---
layout: post
title: "OAUTH y seguridad"
date: "Mon Mar 23 13:20:01 +0100 2015"
category: seguridad
tags: seguridad oauth identidad federada autentificaci�n autenticaci�n api
---



<a href="https://www.flickr.com/photos/fernand0/6186853984://500px.com/photo/86749033/empezamos-en-15-minutos-%23icstcc-%23icstcc14-by-fernando-tricas" title="Nombres"><img src="https://drscdn.500px.org/photo/86749033/w%3D280_h%3D280/380947f119ea736c77186b8a74f3e248?v=0" width="240"  alt="Identificaci�n"></a> 
�ltimamente es raro el sitio que no permite identificarse con nuestra cuenta de Google, Facebook, Twitter u otras. La ventaja para el desarrollador est� clara: desde un punto de vista de usuarios que re-utilizan contrase�as y que no son muy fiables a la hora de gestionar correctamente sus credenciales, delegamos ese trabajo en empresas m�s pontentes y que seguramente lo har�n mejor que nosotros. Aunque puede que no sea una ventaja completa porque queramos tener un sistema de acceso para todas aquellas personas que no quieran utilizar este tipo de mezclas. 
Desde el punto de vista del usuario tambi�n est� clara la ventaja: no tenemos que andar d�ndonos de alta en montones de sitios, con contrase�as (idealmente) diferentes y cofiando en administradores de plataformas que apenas conocemos.

Del tema de delegar la gesti�n de cuentas en otros se hablaba en [Introducing the "Secure Account Management Fundamentals" course on Pluralsight](http://www.troyhunt.com/2015/01/introducing-secure-account-management.html) que enlazamos en su momento desde [Fundamentos de gesti�n de cuentas](http://fernand0.github.io/Fundamentos-De-Gestion-De-Cuentas/).

Para estas cosas se utiliza, entre otros <a href="http://oauth.net/">OAuth</a> que es un protocolo bastante completo y que permite cosas m�s sofisticadas. Nosotros lo hemos visto de pasada cuando hemos hablado de [Publicar en Facebook las entradas de este sitio usando Python](http://fernand0.github.io/Publicar-En-Facebook-Las-Entradas-De-Este-Sitio/), [Publicar en Twitter las entradas de este sitio usando Python](http://fernand0.github.io/publicar-en-twitter-las-entradas-de-este-sitio/), porque estos sitios no permiten que utilicemos la contrase�a directamente, sino que prefieren que nos identifiquemos a trav�s de OAuth.

Esencialmente se basa en que nos autentificamos una vez en el sitio proveedor (o m�s, si fuera necesario en el tiempo) y este nos proporciona unos *tokens* de acceso que permiten realizar ciertas operaciones en el propio sitio o, simplemenete nos reconoce como usuarios y eso le basta al sitio de origen como identificaci�n.

El historial de seguridad de este protocolo ha tenido sus incidentes y por eso me gust� encontrar <a href="http://www.oauthsecurity.com/">OAuth Security Cheatsheet</a> que nos da las ideas principales sobre el flujo de datos y las precacuciones que debemos tomar a la hora de implementarlo/utilizarlo.
